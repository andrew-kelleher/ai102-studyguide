# Plan, Create and Deploy an Azure AI Foundry Service

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers planning, creating, and deploying **Azure AI Foundry services**. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Plan for a Solution that Meets Responsible AI Principles

📖 **Docs:** [What is Responsible AI?](https://learn.microsoft.com/en-us/azure/machine-learning/concept-responsible-ai)

**Overview**

- Responsible AI ensures AI systems are ethical, fair, and reliable
- Microsoft defines 6 core principles:
    - Fairness
    - Reliability and safety
    - Privacy and security
    - Inclusiveness
    - Transparency
    - Accountability

**Key Points**

- Must comply with data governance and regulatory standards
- Azure provides tools such as **content filters** and **Azure AI Content Safety**
- Responsible AI checks should be built into design, training, and deployment phases

!!! tip "Exam Tip"
    Be prepared for scenario questions on **choosing controls to mitigate bias or risks**

---

## :material-lightbulb-on: Create an Azure AI Resource

📖 **Docs:** [Quickstart: Create your first AI Foundry resource](https://learn.microsoft.com/azure/ai-services/multi-service-resource)

**Overview**

- AI resources are provisioned in the **Azure portal** or via CLI/ARM templates
- Services like Azure OpenAI, Vision, Language, or Speech require dedicated resources
- Resource creation includes selecting region, pricing tier, and enabling authentication (keys or Azure AD)

**Key Points**

- Some services have regional restrictions (e.g., Azure OpenAI)
- Quotas apply per subscription and region
- Access controlled with **RBAC**

!!! warning "Limits"
    Creating AI resources often requires **quota approval** from Microsoft

---

## :material-lightbulb-on: Choose the Appropriate AI Models for Your Solution

📖 **Docs:** [Azure AI Foundry model catalog](https://ai.azure.com/catalog)

**Overview**

- The **model catalog** provides foundation models for text, vision, speech, and embeddings
- Choice depends on task:
    - GPT series for text, summarization, code
    - Phi/Mistral for lightweight generative tasks
    - Embeddings for semantic search
    - Vision models for image classification/detection

**Key Points**

- Consider latency, cost, accuracy, and context length
- Prebuilt models reduce training effort, while fine-tuning allows customization

!!! tip "Exam Tip"
    Expect questions comparing **fine-tuning vs RAG vs prebuilt models**

---

## :material-lightbulb-on: Deploy AI Models Using the Appropriate Deployment Options

📖 **Docs:** [Deployment overview for Azure AI Foundry Models](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/deployments-overview)

**Overview**

- Deployment options include:
    - **Managed endpoints** (real-time inference, batch)
    - **Serverless APIs** (low-code usage)
    - **Containerized deployments** (custom runtime environments)

**Key Points**

- Managed endpoints provide scaling and monitoring
- Batch endpoints are suitable for asynchronous tasks
- Container deployments support offline or hybrid scenarios

!!! example "Use Case"
    - Real-time chatbot → managed endpoint
    - Offline document processing → container deployment

---

## :material-lightbulb-on: Install and Utilize the Appropriate SDKs and APIs

📖 **Docs:** [Azure AI Foundry SDK client libraries](https://learn.microsoft.com/en-us/azure/ai-foundry/how-to/develop/sdk-overview)

**Overview**

- SDKs provide programmatic access to AI services (Python, C#, Java, JavaScript)
- REST APIs are available for all services
- Common tasks:
    - Submitting inference requests
    - Managing deployments
    - Retrieving evaluation metrics

**Key Points**

- SDKs simplify authentication, retries, and error handling
- APIs are versioned and may have feature restrictions per region

!!! tip "Exam Tip"
    Memorize which SDK applies to which service (e.g., `azure-ai-language`, `azure-ai-vision`)

---

## :material-lightbulb-on: Determine a Default Endpoint for a Service

📖 **Docs:** [Endpoints for Azure AI Foundry Models](https://learn.microsoft.com/en-us/azure/ai-foundry/foundry-models/concepts/endpoints)

**Overview**

- Each Azure AI resource has a **default endpoint**
- Endpoint = base URL used for API calls
- Example format: `https://<resource-name>.services.ai.azure.com/models`
- Example format: `https://<resource-name>.openai.azure.com`

**Key Points**

- Keys or Azure AD tokens required for authentication
- Default endpoints can be overridden by custom deployments

!!! info "Best Practices"
    Use **Azure Key Vault** to manage keys and avoid hardcoding credentials

---

## :material-lightbulb-on: Integrate Azure AI Foundry Services into a CI/CD Pipeline

📖 **Docs:** [CI/CD for Azure AI Foundry "AI Agent Service" Agents](https://learn.microsoft.com/en-us/answers/questions/2279558/ci-cd-for-azure-ai-foundry-ai-agent-service-agents)

**Overview**

- CI/CD automates testing, deployment, and monitoring of AI services
- Tools:
    - **GitHub Actions**
    - **Azure DevOps Pipelines**
    - **ARM/Bicep templates** for infra-as-code

**Key Points**

- Enables version control for models and prompts
- Supports automated testing and rollback
- Integration with monitoring tools ensures reliability

!!! example "Use Case"
    Auto-deploy updated prompt flows after approval in a GitHub repo

---

## :material-lightbulb-on: Plan and Implement a Container Deployment

📖 **Docs:** [What are Azure AI containers?](https://learn.microsoft.com/azure/ai-services/cognitive-services-container-support)

**Overview**

- Azure AI services can run in **Docker containers** for edge, hybrid, or disconnected environments
- Supports services like Vision, Language, Speech, and Document Intelligence

**Key Points**

- Container deployments require billing info to connect back to Azure
- Useful for compliance (data stays local)
- Can integrate with **AKS** or other orchestrators

!!! warning "Limits"
    Not all services support container deployment

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 Responsible AI = fairness, reliability, privacy, inclusiveness, transparency, accountability
- 📌 AI resources created in portal/CLI, with **quotas** and **region** limits
- 📌 Choose models from **model catalog** based on use case
- 📌 Deployment: **managed endpoints**, **batch**, or **containers**
- 📌 SDKs available in Python, C#, Java, JS
- 📌 CI/CD supported via **GitHub Actions** and **Azure DevOps**
- 📌 Containers useful for **hybrid** or **disconnected** scenarios
