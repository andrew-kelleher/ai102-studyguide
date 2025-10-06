# Optimize and Operationalize a Generative AI Solution

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers how to **optimize, monitor, and operationalize** generative AI solutions in Azure AI Foundry. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Configure Parameters to Control Generative Behavior

📖 **Docs:** [Control completions with parameters](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/how-to/fine-tuning)

**Overview**

- Parameters influence model outputs, creativity, and response style
- Common parameters:
    - **Temperature**: randomness (0 = deterministic, 1 = creative)
    - **Top_p**: nucleus sampling to control probability mass
    - **Max_tokens**: maximum length of output
    - **Frequency_penalty**: discourages repetition
    - **Presence_penalty**: encourages introducing new topics

**Key Points**

- Low temperature = consistent answers
- High temperature = creative, diverse answers
- Token limits vary by model (e.g., GPT-4 Turbo = 128K context)

!!! tip "Exam Tip"
    Expect parameter tuning scenarios — e.g., “make responses more factual and less creative”

---

## :material-lightbulb-on: Configure Model Monitoring and Diagnostic Settings

📖 **Docs:** [Monitor models with Azure Monitor](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/how-to/monitor-openai)

**Overview**

- Monitoring ensures performance and reliability
- Tools:
    - **Azure Monitor**
    - **Application Insights**
    - **Diagnostic settings** for logging

**Key Points**

- Track metrics: latency, request counts, error rates, token consumption
- Alerts can trigger on quota limits or performance drops
- Logs help identify prompt injection or misuse

!!! warning "Exam Tip"
    Monitoring includes both **service health** and **content safety events**

---

## :material-lightbulb-on: Optimize and Manage Resources for Deployment

📖 **Docs:** [Manage Azure AI deployments](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/deployments-overview)

**Overview**

- Optimize deployments by scaling resources and updating models
- Options:
    - **Scaling**: autoscale for high-traffic apps
    - **Foundational model updates**: migrate to new versions as released
    - **Batch endpoints**: efficient for bulk processing

**Key Points**

- Keep track of model deprecation schedules
- Scale horizontally for concurrency, vertically for performance
- Cost optimization includes reducing context length and caching results

---

## :material-lightbulb-on: Enable Tracing and Collect Feedback

📖 **Docs:** [Prompt flow evaluation](https://learn.microsoft.com/en-us/azure/ai-foundry/how-to/develop/trace-production-sdk)

**Overview**

- Tracing helps analyze execution paths of prompt flows
- Feedback collection ensures continuous improvement
- Supported via **Azure Monitor**, **Application Insights**, and **Prompt flow tracing**

**Key Points**

- Collect human-in-the-loop feedback
- Use structured evaluations (groundedness, relevance, coherence)
- Store traces for debugging multi-step flows

!!! info "Best Practices"
    Always collect feedback before scaling to production

---

## :material-lightbulb-on: Implement Model Reflection

📖 **Docs:** [Model self-reflection](https://learn.microsoft.com/en-us/azure/ai-foundry/how-to/evaluate-generative-ai-app)

**Overview**

- Model reflection = model critiques its own responses and improves output
- Typically implemented using **chained prompts**
- Supports **safety checks** and **accuracy validation**

**Key Points**

- Improves groundedness and reduces hallucinations
- Works well with RAG pipelines
- May increase latency and cost

!!! tip "Exam Tip"
    If asked how to make a model **critique and refine its answers**, the answer is **model reflection**

---

## :material-lightbulb-on: Deploy Containers for Use on Local and Edge Devices

📖 **Docs:** [Deploy AI services in containers](https://learn.microsoft.com/azure/ai-services/cognitive-services-container-support)

**Overview**

- Many Azure AI services support **Docker containers**
- Enables offline, hybrid, and edge deployment scenarios

**Key Points**

- Containers require connection to Azure for billing
- Useful for data sovereignty and low-latency requirements
- Can run in **AKS, IoT Edge, or Kubernetes clusters**

!!! warning "Limits"
    Not all models are containerizable — check supported list

---

## :material-lightbulb-on: Implement Orchestration of Multiple Generative AI Models

📖 **Docs:** [Orchestrate agent behavior with generative AI](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions)

**Overview**

- Orchestration combines multiple models or services into workflows
- Examples:
    - GPT + Embeddings for RAG
    - Vision model + GPT for multimodal tasks
    - Multiple LLMs for specialization

**Key Points**

- Tools: **Prompt flow**, **Semantic Kernel**, **Autogen**
- Helps distribute tasks across specialized models
- Supports failover and redundancy

!!! example "Use Case"
    Workflow that uses GPT for text, DALL·E for images, and embeddings for retrieval

---

## :material-lightbulb-on: Apply Prompt Engineering Techniques to Improve Responses

📖 **Docs:** [Prompt engineering techniques](https://learn.microsoft.com/azure/ai-services/openai/concepts/prompt-engineering)

**Overview**

- Prompt engineering refines queries to maximize model performance
- Techniques:
    - Role assignment (“You are a helpful assistant”)
    - Few-shot learning (examples in prompt)
    - Chain-of-thought prompting
    - Output formatting instructions

**Key Points**

- Use templates for consistency
- Prevent prompt injection by sanitizing inputs
- Test prompts iteratively

!!! tip "Exam Tip"
    Know prompt engineering techniques and their use cases

---

## :material-lightbulb-on: Fine-Tune a Generative Model

📖 **Docs:** [Customize a model with fine-tuning](https://learn.microsoft.com/azure/ai-services/openai/how-to/fine-tuning)

**Overview**

- Fine-tuning customizes base models for specific domains
- Requires training data in JSONL format
- Used when:
    - RAG is not sufficient
    - Domain-specific vocabulary or style is required

**Key Points**

- Training requires large, clean datasets
- Fine-tuned models incur additional cost
- Fine-tuning applies mainly to GPT-3.5 Turbo

!!! warning "Limits"
    GPT-4 fine-tuning may have limited availability

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 **Parameters**: temperature, top_p, max_tokens, penalties control output  
- 📌 **Monitoring** = requests, latency, errors, tokens, safety events  
- 📌 Optimize deployments via **scaling**, **batching**, **model updates**  
- 📌 **Tracing** + **feedback** collection ensure quality  
- 📌 **Model reflection** = self-critique for improved groundedness  
- 📌 **Containers** = edge, hybrid, offline scenarios  
- 📌 **Orchestration** = multiple models combined in workflows  
- 📌 **Prompt engineering** = role, examples, structure, safety  
- 📌 **Fine-tuning** = domain-specific customization, requires clean data  
