# Extract Information with Azure AI Content Understanding

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers extracting structured information with **Azure AI Content Understanding**. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Create an OCR Pipeline to Extract Text from Images and Documents

📖 **Docs:** [OCR in Azure AI](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-ocr)

**Overview**

- OCR (Optical Character Recognition) extracts printed or handwritten text
- Can be applied to:
    - Images
    - PDFs
    - Scanned documents

**Key Points**

- OCR pipeline = ingest → detect regions → extract text → output structured format
- Supports multiple languages
- Can be combined with Document Intelligence for advanced parsing

!!! tip "Exam Tip"
    OCR extracts **text only**, not structure or semantics

---

## :material-lightbulb-on: Summarize, Classify, and Detect Attributes of Documents

📖 **Docs:** [What is Azure AI Content Understanding](https://learn.microsoft.com/en-us/azure/ai-services/content-understanding/overview)

**Overview**

- Azure AI Content Understanding applies NLP to documents
- Capabilities:
    - **Summarization** (extractive and abstractive)
    - **Classification** (categorize documents by type)
    - **Attribute detection** (metadata, topics, sentiment)

**Key Points**

- Uses Azure AI Language models
- Custom classification available for domain-specific needs
- Summarization reduces large documents into key points

!!! example "Use Case"
    Summarizing legal contracts into executive briefs

---

## :material-lightbulb-on: Extract Entities, Tables, and Images from Documents

📖 **Docs:** [Use Document Intelligence models](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/how-to-guides/use-sdk-rest-api)

**Overview**

- Beyond OCR, advanced extraction retrieves:
    - **Entities** (names, organizations, dates)
    - **Tables** (rows, columns, cell values)
    - **Embedded images**

**Key Points**

- Structured outputs in JSON or tables
- Requires Document Intelligence models
- Entities align with AI Language recognition

!!! warning "Exam Tip"
    If scenario requires **table or entity extraction** → Document Intelligence, not OCR

---

## :material-lightbulb-on: Process and Ingest Documents, Images, Videos, and Audio with Azure AI Content Understanding

📖 **Docs:** [Quickstart: Use Content Understanding with a single file](https://learn.microsoft.com/en-us/azure/ai-services/content-understanding/quickstart/use-ai-foundry)

**Overview**

- Azure AI Content Understanding = multimodal ingestion and enrichment
- Supports:
    - Documents
    - Images
    - Video
    - Audio

**Key Points**

- Provides a unified pipeline for enrichment
- Can integrate OCR, NLP, entity extraction, summarization
- Outputs structured insights for downstream apps or AI Search

!!! example "Use Case"
    Processing compliance documents, extracting entities, and storing enriched data in Azure AI Search

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 OCR extracts printed/handwritten text from images/docs  
- 📌 **Summarization** + **classification** provide condensed insights  
- 📌 **Entities**, **tables**, and **images** extracted via **Document Intelligence**  
- 📌 Content Understanding ingests **docs, images, video, audio**  
- 📌 Outputs structured data for search and AI pipelines  
