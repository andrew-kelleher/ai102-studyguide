# Manage, Monitor, and Secure an Azure AI Foundry Service

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers monitoring, securing, and managing **Azure AI Foundry services**. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Monitor an Azure AI Resource

📖 **Docs:** [Enable diagnostic logging for Azure AI services](https://learn.microsoft.com/en-us/azure/ai-services/diagnostic-logging)

**Overview**

- Monitoring ensures service reliability, performance, and compliance
- Tools include:
    - **Azure Monitor** for metrics and logging
    - **Application Insights** for telemetry
    - **Diagnostic settings** for logs and auditing

**Key Points**

- Common metrics: requests count, latency, errors, token usage
- Alerts can be configured for quota or anomaly detection
- Logs can be exported to Log Analytics, Event Hub, or Storage

!!! tip "Exam Tip"
    Know which metrics are monitored: **requests, latency, token consumption**

---

## :material-lightbulb-on: Manage Costs for Azure AI Foundry Services

📖 **Docs:** [Plan and manage costs for Azure AI Foundry hubs](https://learn.microsoft.com/en-us/azure/ai-foundry/how-to/costs-plan-manage)

**Overview**

- Costs depend on:
    - Model type and size (e.g., GPT-4 vs GPT-3.5)
    - Number of tokens processed
    - Region and resource configuration
- Use **Azure Cost Management + Billing** to track usage

**Key Points**

- Set **budgets and alerts** to avoid overspending
- Use **reserved capacity** where available
- Optimize by:
    - Choosing smaller models for simpler tasks
    - Reducing context window size
    - Using batch endpoints for large jobs

!!! info "Best Practices"
    Regularly review **usage reports** and align with expected workloads

---

## :material-lightbulb-on: Manage and Protect Account Keys

📖 **Docs:** [Authenticate requests to Azure AI services](https://learn.microsoft.com/azure/ai-services/authentication)

**Overview**

- Each AI service resource has **two keys** and an **endpoint**
- Keys are used for API authentication
- Can be regenerated at any time

**Key Points**

- Store keys securely in **Azure Key Vault**
- Use **managed identities** instead of distributing keys where possible
- Rotate keys regularly for security compliance

!!! warning "Exam Tip"
    Questions often test on **key rotation and storage in Key Vault**

---

## :material-lightbulb-on: Manage Authentication for an Azure AI Foundry Service Resource

📖 **Docs:** [Authenticate requests to Azure AI services](https://learn.microsoft.com/azure/ai-services/authentication)

**Overview**

- Authentication methods:
    - API keys
    - **Azure Active Directory (Azure AD) tokens**
- Azure AD is preferred for enterprise and multi-user scenarios

**Key Points**

- RBAC can control access at resource or subscription level
- Use **least privilege principle**
- Keys should be fallback, not the primary method

!!! example "Use Case"
    - Enterprise integration with RBAC → Azure AD
    - Quick prototyping or testing → API keys

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 Monitor with **Azure Monitor, App Insights, Diagnostic logs**
- 📌 Costs depend on model type, tokens, and resource configuration
- 📌 Store keys in **Key Vault**, rotate regularly
- 📌 Use **Azure AD authentication** + RBAC for enterprise scenarios
