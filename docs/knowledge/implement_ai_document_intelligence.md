# Implement an Azure AI Document Intelligence Solution

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers building and managing **Azure AI Document Intelligence** solutions. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Provision a Document Intelligence Resource

📖 **Docs:** [Create a Document Intelligence resource](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/how-to-guides/create-document-intelligence-resource)

**Overview**

- Document Intelligence (formerly **Form Recognizer**) extracts structured data from documents
- Provision in the **Azure portal**, CLI, or ARM template
- Resource includes endpoint + key for API access

**Key Points**

- Regional availability varies
- Pricing based on pages processed
- RBAC controls access

!!! warning "Exam Tip"
    Always provision **Document Intelligence resource**, not generic Cognitive Services

---

## :material-lightbulb-on: Use Prebuilt Models to Extract Data from Documents

📖 **Docs:** [Document processing models](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/model-overview)

**Overview**

- Prebuilt models handle common document types:
    - Invoices
    - Receipts
    - Business cards
    - Identity documents
    - Layout (general text extraction)

**Key Points**

- Quick start without training
- Outputs structured JSON with fields + confidence scores
- Useful for automating business workflows

!!! example "Use Case"
    Extracting vendor, total, and date from an invoice

---

## :material-lightbulb-on: Implement a Custom Document Intelligence Model

📖 **Docs:** [Document Intelligence custom models](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/train/custom-model)

**Overview**

- Custom models trained on user-provided documents
- Suitable when prebuilt models don’t fit requirements

**Key Points**

- Requires labeled training data
- Labeling done via **Document Intelligence Studio**
- Handles semi-structured or unstructured forms

---

## :material-lightbulb-on: Train, Test, and Publish a Custom Document Intelligence Model

📖 **Docs:** [Build and train a custom extraction model](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/how-to-guides/build-a-custom-model)

**Overview**

- Training creates a custom model from labeled docs
- Evaluation validates accuracy
- Publishing exposes endpoint for consumption

**Key Points**

- Supports iterative retraining for improvement
- Metrics include accuracy, recall, and precision
- Must publish before calling via API

!!! tip "Exam Tip"
    “Model trained but not available to apps” → must **publish model**

---

## :material-lightbulb-on: Create a Composed Document Intelligence Model

📖 **Docs:** [Document Intelligence composed custom models](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/train/composed-models)

**Overview**

- Composed model = combines multiple custom models
- Automatically selects correct sub-model at runtime

**Key Points**

- Useful when multiple document types exist
- Reduces need to pre-sort documents
- Example: invoices + receipts + tax forms

!!! example "Use Case"
    A composed model that routes between invoice and receipt extractors

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 Provision **Document Intelligence resource**, region + pricing matter  
- 📌 **Prebuilt models** = invoices, receipts, IDs, business cards, layout  
- 📌 **Custom models** require labeled data via Studio  
- 📌 Must **train, test, publish** before API consumption  
- 📌 **Composed model** = collection of multiple models auto-selected at runtime  
