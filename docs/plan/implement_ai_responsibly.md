# Implement AI Solutions Responsibly

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers implementing **responsible AI practices** in Azure AI Foundry solutions. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Implement Content Moderation Solutions

📖 **Docs:** [Azure AI Content Safety overview](https://learn.microsoft.com/azure/ai-services/content-safety/overview)

**Overview**

- Content moderation ensures AI solutions do not produce harmful or unsafe outputs
- Azure AI Content Safety detects and classifies:
    - Hate
    - Violence
    - Sexual content
    - Self-harm

**Key Points**

- Supports both **text** and **image** moderation
- Categories are scored on severity levels
- Can block, review, or log flagged content

!!! tip "Exam Tip"
    If the scenario involves **filtering harmful content**, use **Azure AI Content Safety**

---

## :material-lightbulb-on: Configure Responsible AI Insights, Including Content Safety

📖 **Docs:** [Responsible AI dashboard](https://learn.microsoft.com/azure/machine-learning/concept-responsible-ai-dashboard)

**Overview**

- Responsible AI Insights provide tools to evaluate fairness, explainability, and safety
- Content Safety integration provides monitoring and reporting
- Helps track risks and compliance with Responsible AI standards

**Key Points**

- Dashboards show model performance across sensitive attributes
- Identify and mitigate bias during testing
- Can integrate with CI/CD for continuous monitoring

!!! info "Best Practices"
    Use Responsible AI dashboards during both **training** and **deployment**

---

## :material-lightbulb-on: Implement Responsible AI, Including Content Filters and Blocklists

📖 **Docs:** [Content filtering in Azure OpenAI](https://learn.microsoft.com/azure/ai-services/openai/concepts/content-filter)

**Overview**

- Azure OpenAI includes **content filters** for harmful outputs
- Custom **blocklists** can be applied to prevent specific terms or topics

**Key Points**

- Filters cover categories like sexual, violent, self-harm, hate speech
- Filters are configurable to allow stricter enforcement
- Blocklists help align outputs with organizational policies

!!! tip "Exam Tip"
    Remember the difference:
    - **Content filters** = built-in moderation
    - **Blocklists** = custom word/phrase restrictions

---

## :material-lightbulb-on: Prevent Harmful Behavior, Including Prompt Shields and Harm Detection

📖 **Docs:** [Prompt engineering and safety](https://learn.microsoft.com/azure/ai-services/openai/concepts/prompt-engineering)

**Overview**

- Harmful behaviors include **prompt injection** and **jailbreaking**
- Mitigation strategies:
    - **Prompt shields**: predefined templates that reduce manipulation risks
    - **Harm detection**: automatic monitoring of inputs and outputs

**Key Points**

- Validate and sanitize user inputs
- Avoid exposing raw system prompts
- Monitor logs for malicious usage attempts

!!! warning "Exam Tip"
    Watch for scenarios describing **prompt injection attacks** — answer with **prompt shields or harm detection**

---

## :material-lightbulb-on: Design a Responsible AI Governance Framework

📖 **Docs:** [Cloud Adoption Framework: Govern AI](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/ai/govern)

**Overview**

- Governance ensures Responsible AI is part of the **lifecycle** of AI projects
- Includes:
    - Policies
    - Processes
    - Tools for oversight

**Key Points**

- Aligns with Microsoft’s 6 principles: fairness, reliability, privacy, inclusiveness, transparency, accountability
- Requires collaboration between technical and compliance teams
- Governance includes monitoring, incident response, and audits

!!! example "Use Case"
    Enterprise deploying AI copilots with oversight committees and auditing tools

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 Use **Azure AI Content Safety** for text/image moderation
- 📌 Responsible AI Insights = dashboards for fairness and safety
- 📌 **Content filters** = built-in moderation, **blocklists** = custom restrictions
- 📌 **Prompt shields + harm detection** defend against malicious inputs
- 📌 Governance framework aligns with Microsoft’s 6 Responsible AI principles
