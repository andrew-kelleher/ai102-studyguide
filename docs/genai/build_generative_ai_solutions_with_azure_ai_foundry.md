# Build Generative AI Solutions with Azure AI Foundry

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers building and deploying **generative AI solutions** using Azure AI Foundry. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts.

---

## :material-lightbulb-on: Plan and Prepare for a Generative AI Solution

📖 **Docs:** [Plan a generative AI solution](https://azure.microsoft.com/en-in/products/machine-learning/generative-ai)

**Overview**

- Assess business needs and map them to Azure AI Foundry capabilities
- Decide between **prebuilt models** (e.g., GPT, Claude, Mistral) and **fine-tuned/custom models**
- Plan for **Responsible AI** principles: fairness, reliability, safety, privacy, inclusiveness, transparency

**Key Points**

- Ensure data compliance with **Azure’s region availability**
- Define KPIs: latency, cost, accuracy
- Choose the right model size (smaller for cost efficiency, larger for complex reasoning)

!!! tip "Exam Tip"
    Expect scenario-based questions asking you to match a use case to the correct model type or service.

---

## :material-lightbulb-on: Deploy a Hub, Project, and Necessary Resources with Azure AI Foundry

📖 **Docs:** [Azure AI Foundry hubs and projects](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)

**Overview**

- **Hub**: Central workspace for managing multiple AI projects
- **Project**: Contains assets (data, models, prompt flows)
- Requires linked **Azure AI Search**, **Azure Storage**, and sometimes **Azure OpenAI** resources

**Key Facts**

- A hub can support multiple projects
- Projects inherit security and networking from the hub
- Role-based access control (RBAC) applies at both hub and project levels

!!! warning "Limits"
    - Regional availability: Azure OpenAI is not available in all regions.
    - Resource quotas: per-subscription and per-region.

---

## :material-lightbulb-on: Deploy the Appropriate Generative AI Model for Your Use Case

📖 **Docs:** [Model catalog](https://azure.microsoft.com/en-us/products/ai-foundry/models#Models)

**Overview**

- Choose models from the **model catalog** (e.g., GPT-4, GPT-35-Turbo, Phi-3, Mistral)
- Match task to model:
    - Text generation → GPT series
    - Code completion → Codex-like models
    - Small footprint → Phi-3-mini

**Key Points**

- Pay attention to **token limits** (e.g., GPT-4 Turbo supports 128K context length)
- Pricing is per 1,000 tokens (input + output)

!!! tip "Exam Tip"
    Know model **max context size** and **capabilities**. Microsoft often tests model suitability.

---

## :material-lightbulb-on: Implement a Prompt Flow Solution

📖 **Docs:** [Prompt flow in Azure AI Foundry](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/prompt-flow)

**Overview**

- **Prompt flow** = orchestration tool to design, test, evaluate, and deploy prompts
- Supports chaining prompts, grounding, and evaluation
- Includes **visual editor** and SDK integration

**Key Facts**

- Flows can include LLM calls, Python code, and external API calls
- Enables tracking, versioning, and collaboration

!!! example "Use Case"
    Customer service bot with multi-turn reasoning.

---

## :material-lightbulb-on: Implement a RAG Pattern by Grounding a Model in Your Data

📖 **Docs:** [Grounding and RAG in Azure AI](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/concepts/groundedness)

**Overview**

- **RAG (Retrieval Augmented Generation):** Combines LLM with enterprise data sources
- Steps:
    1. Ingest and chunk documents
    2. Embed using Azure OpenAI Embeddings
    3. Store in **Azure AI Search**
    4. Retrieve relevant chunks and pass to LLM

**Key Points**

- Improves factual accuracy and reduces hallucinations
- Embedding models: `text-embedding-ada-002`, `text-embedding-3-large`
- Vector store = **Azure AI Search** (supports hybrid search)

!!! tip "Exam Tip"
    Watch for scenarios: *When to use fine-tuning vs. RAG?* → RAG is better for dynamic/factual grounding.

---

## :material-lightbulb-on: Evaluate Models and Flows

📖 **Docs:** [Evaluate models and flows](https://learn.microsoft.com/en-us/azure/ai-foundry/how-to/evaluate-generative-ai-app)

**Overview**

- Evaluate prompts and flows based on **quality, reliability, safety**
- Use human feedback + automated metrics (e.g., BLEU, ROUGE, perplexity)

**Key Points**

- **Evaluation harness** in Foundry helps test against sample datasets
- Supports A/B testing for prompts

!!! info "Metrics"
    - **Groundedness**: factual correctness.
    - **Coherence**: logical flow.
    - **Relevance**: matches user intent.

---

## :material-lightbulb-on: Integrate Your Project into an Application with Azure AI Foundry SDK

📖 **Docs:** [Azure AI Foundry SDK](https://learn.microsoft.com/en-us/azure/ai-foundry/how-to/develop/sdk-overview?pivots=programming-language-python)

**Overview**

- Python SDK enables programmatic control of projects, models, and flows
- Common tasks:
  - Deploying prompt flows
  - Running evaluations
  - Accessing endpoints

**Example**

```python
from azure.ai.foundry import FoundryClient
client = FoundryClient()
response = client.run_prompt_flow(flow_name="myflow", inputs={"question": "What is Azure AI Foundry?"})
print(response.output)
```

**Key Points**

- SDK integrates with CI/CD pipelines
- Supports endpoint management for integration with apps

---

## :material-lightbulb-on: Utilize Prompt Templates in Your Generative AI Solution

📖 **Docs:** [Prompt templates](https://learn.microsoft.com/en-us/azure/ai-foundry/how-to/prompt-flow-tools/prompt-tool)

**Overview**

- Templates standardize prompts with placeholders
- Example:
  ```
  You are a helpful assistant. Answer the following:
  {{user_question}}
  ```

**Key Facts**

- Reduces prompt injection risks
- Improves consistency and reusability
- Supports variables, loops, and conditional logic

!!! tip "Exam Tip"
    Microsoft may test knowledge of **prompt injection mitigation** – templates are one safeguard.

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 Know the difference between **fine-tuning** and **RAG**
- 📌 Memorize **model context limits** and **token pricing basics**
- 📌 Understand how **hubs/projects/resources** are structured
- 📌 Be prepared for **scenario-based questions** on Responsible AI
- 📌 Familiarize with **evaluation metrics** and when to apply them
