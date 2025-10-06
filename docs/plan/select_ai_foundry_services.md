# Select the Appropriate Azure AI Foundry Services

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers identifying and selecting the right **Azure AI Foundry services** for various solution domains. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts.

---

## :material-lightbulb-on: Select the Appropriate Service for a Generative AI Solution

📖 **Docs:** [Architecture Center: Choose an Azure AI services technology](https://learn.microsoft.com/azure/ai-services/openai/overview)

**Overview**

- Generative AI solutions require **large language models (LLMs)** or other generative models (image, text, code).
- Primary service: **Azure OpenAI Service** (models like GPT-4, GPT-3.5, DALL·E, Whisper)
- Managed through **Azure AI Foundry hubs/projects**

**Key Points**

- Use **Azure OpenAI** for text generation, summarization, translation, code generation, chatbots
- Model catalog in Azure AI Foundry provides additional generative models (e.g., Phi, Mistral)
- Responsible AI must be applied (content filters, monitoring)

!!! tip "Exam Tip"
    If the scenario involves **text, chat, or image generation**, Azure OpenAI is the service.

---

## :material-lightbulb-on: Select the Appropriate Service for a Computer Vision Solution

📖 **Docs:** [Architecture Center: Choose an Azure AI services technology](https://learn.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/ai-services#categories-of-ai-services)

**Overview**

- Computer Vision solutions process and analyze images or video
- Primary service: **Azure AI Vision**
- Capabilities:
    - Object detection, classification
    - OCR (Optical Character Recognition)
    - Spatial analysis
    - Face detection/recognition (legacy)

**Key Points**

- For OCR → **Read API** in AI Vision
- For custom models → **Custom Vision** (training image classification or object detection models)
- Video Indexer can analyze video/audio at scale

!!! warning "Limits"
    Some features (e.g., facial recognition) have restricted access due to Responsible AI concerns.

---

## :material-lightbulb-on: Select the Appropriate Service for a Natural Language Processing Solution

📖 **Docs:** [Architecture Center: Choose an Azure AI services technology](https://learn.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/ai-services#categories-of-ai-services)

**Overview**

- Natural Language Processing (NLP) = understanding and extracting meaning from text
- Primary service: **Azure AI Language**
- Capabilities:
    - Key phrase extraction
    - Sentiment analysis
    - Named entity recognition
    - Text summarization
    - Language detection

**Key Points**

- Use **Custom Text Classification** for domain-specific models
- Supports multilingual processing
- Integrates with AI Foundry workflows

!!! tip "Exam Tip"
    If the scenario asks for **sentiment, classification, or entity recognition**, select **AI Language**.

---

## :material-lightbulb-on: Select the Appropriate Service for a Speech Solution

📖 **Docs:** [Architecture Center: Choose an Azure AI services technology](https://learn.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/ai-services#categories-of-ai-services)

**Overview**

- Speech solutions convert between spoken audio and text
- Primary service: **Azure AI Speech**
- Capabilities:
    - Speech-to-text (STT)
    - Text-to-speech (TTS)
    - Speech translation
    - Speaker recognition

**Key Points**

- Supports custom voice models
- Real-time and batch transcription supported
- Can integrate with call centers, IVR, accessibility tools

!!! example "Use Case"
    - Call center transcription
    - Voice-enabled chatbots

---

## :material-lightbulb-on: Select the Appropriate Service for an Information Extraction Solution

📖 **Docs:** [Architecture Center: Choose an Azure AI services technology](https://learn.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/ai-services#categories-of-ai-services)

**Overview**

- Extracts structured information from documents
- Primary service: **Azure AI Document Intelligence** (formerly Form Recognizer)
- Capabilities:
    - Prebuilt models (invoices, receipts, IDs, business cards)
    - Custom document extraction models
    - Layout extraction

**Key Points**

- Best for semi-structured or unstructured documents (PDFs, images)
- Custom models require training with sample documents
- Works with both forms and free-text documents

!!! tip "Exam Tip"
    Look for keywords: **invoices, receipts, IDs, forms → Document Intelligence**.

---

## :material-lightbulb-on: Select the Appropriate Service for a Knowledge Mining Solution

📖 **Docs:** [Architecture Center: Choose an Azure AI services technology](https://learn.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/ai-services#categories-of-ai-services)

**Overview**

- Knowledge mining = extracting insights from large document/data collections
- Primary service: **Azure AI Search**
- Works with:
    - Cognitive skills (OCR, entity recognition)
    - Indexes and vector search
    - Integration with RAG for generative AI

**Key Points**

- Can enrich data using **AI enrichment pipeline**
- Integrates with Azure OpenAI for **retrieval-augmented generation (RAG)**
- Ideal for enterprise search portals

!!! example "Use Case"
    - Corporate knowledge base search.
    - Document repository exploration.

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 **Generative AI** → **Azure OpenAI**
- 📌 **Computer Vision** → **AI Vision** (Custom Vision for custom models)  
- 📌 **NLP** → **AI Language**
- 📌 **Speech** → **AI Speech** 
- 📌 **Information Extraction** → **Document Intelligence** (Form Recognizer)  
- 📌 **Knowledge Mining** → **AI Search**
