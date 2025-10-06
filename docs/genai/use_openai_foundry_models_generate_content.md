# Use Azure OpenAI in Foundry Models to Generate Content

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers using **Azure OpenAI models in Foundry** to generate text, code, and images. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Provision an Azure OpenAI in Foundry Models Resource

📖 **Docs:** [Provision Azure OpenAI resources](https://learn.microsoft.com/azure/ai-services/openai/how-to/create-resource)

**Overview**

- To use Azure OpenAI in Foundry, you must provision a resource in the **Azure portal**
- Requires approval from Microsoft due to responsible AI usage guidelines
- Must be linked into a **Foundry hub/project**

**Key Points**

- Choose the right **region** (not all regions support OpenAI)
- Requires **quota approval**
- Controlled with **RBAC** and subscription limits

!!! warning "Limits"
    Azure OpenAI is not available in all regions and requires Microsoft approval

---

## :material-lightbulb-on: Select and Deploy an Azure OpenAI Model

📖 **Docs:** [Foundry Models sold directly by Azure](https://learn.microsoft.com/en-us/azure/ai-foundry/foundry-models/concepts/models-sold-directly-by-azure)

**Overview**

- Models must be **deployed** to a resource before use
- Supported models:
    - GPT-4 Turbo (text + multimodal)
    - GPT-3.5 Turbo
    - Embeddings models
    - DALL·E (image generation)
    - Whisper (speech-to-text)

**Key Points**

- Choose the correct model based on use case
- Deployment includes selecting **capacity** and **model version**
- Endpoint and key are created for API access

!!! tip "Exam Tip"
    Be ready to match **task → model choice** in questions

---

## :material-lightbulb-on: Submit Prompts to Generate Code and Natural Language Responses

📖 **Docs:** [Completions API](https://learn.microsoft.com/azure/ai-services/openai/how-to/completions)

**Overview**

- Prompts submitted to deployed models using REST API or SDK
- Supports tasks such as:
    - Summarization
    - Code generation
    - Question answering
    - Chat completion

**Key Points**

- Token usage = input + output tokens
- System messages help define assistant behavior
- Can implement **temperature** and **top_p** to control creativity

!!! example "Code Snippet"
```python
from openai import AzureOpenAI

client = AzureOpenAI(api_key="KEY", api_version="2023-07-01-preview")
resp = client.chat.completions.create(
    model="gpt-35-turbo",
    messages=[{"role":"system","content":"You are a helpful assistant"},
              {"role":"user","content":"Write Python code for Fibonacci"}]
)
print(resp.choices[0].message["content"])
```

---

## :material-lightbulb-on: Use the DALL-E Model to Generate Images

📖 **Docs:** [Generate images with Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/dall-e-quickstart)

**Overview**

- **DALL·E** generates images from natural language prompts
- Supports:
    - New images
    - Image edits
    - Variations

**Key Points**

- Output formats: PNG, JPEG
- Size options: 256×256, 512×512, 1024×1024
- Counts tokens separately from text models

!!! tip "Exam Tip"
    Keywords like *generate images* or *create visuals* → DALL·E

---

## :material-lightbulb-on: Integrate Azure OpenAI into Your Own Application

📖 **Docs:** [Integrate Azure OpenAI](https://learn.microsoft.com/azure/ai-services/openai/quickstart)

**Overview**

- Applications integrate via:
    - REST APIs
    - Azure OpenAI SDKs
    - Foundry SDK for orchestration
- Authentication with API keys or Azure AD

**Key Points**

- Endpoints are region-specific
- Secure keys in **Azure Key Vault**
- Common integrations:
    - Chatbots
    - Copilot-style apps
    - Knowledge-grounded solutions

!!! example "Use Case"
    Integrating GPT with a customer support portal

---

## :material-lightbulb-on: Use Large Multimodal Models in Azure OpenAI

📖 **Docs:** [GPT-4o or GPT-4o Mini with Microsoft Fabric for Image Data](https://medium.com/@meetalpa/how-to-integrate-multi-modal-azure-ai-gpt-4o-or-gpt-4o-mini-with-microsoft-fabric-for-image-data-bd1df5b95560)

**Overview**

- GPT-4 Turbo supports **multimodal input** (text + images)
- Enables use cases such as:
    - Image captioning
    - Visual reasoning
    - Analyzing diagrams or screenshots

**Key Points**

- Images are sent as part of the prompt
- Output is still text
- Token usage can increase with multimodal prompts

!!! tip "Exam Tip"
    If the question involves **reasoning over images**, the answer is **GPT-4 Turbo with vision**

---

## :material-lightbulb-on: Implement an Azure OpenAI Assistant

📖 **Docs:** [Getting started with Azure OpenAI Assistants](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/how-to/assistant)

**Overview**

- Assistants API enables **long-running AI agents**
- Features:
    - Tool integration (code interpreter, retrieval)
    - Persistent threads and memory
    - Multi-turn conversations

**Key Points**

- Assistants differ from single-shot prompts
- Useful for copilots and interactive apps
- Configured in Foundry or via SDK

!!! example "Use Case"
    A coding assistant that maintains state across multiple prompts

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 Must **provision Azure OpenAI** resource with Microsoft approval  
- 📌 Models must be **deployed before use**  
- 📌 GPT models → text/code, DALL·E → images, Whisper → speech  
- 📌 Token usage = input + output tokens  
- 📌 GPT-4 Turbo supports **multimodal inputs**  
- 📌 Assistants API = stateful, tool-augmented AI agents
