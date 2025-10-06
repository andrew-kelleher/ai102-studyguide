# Analyze and Translate Text

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers analyzing and translating text with **Azure AI Language** and **Azure AI Translator**. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Extract Key Phrases and Entities

📖 **Docs:** [Key phrase extraction](https://learn.microsoft.com/azure/ai-services/language-service/key-phrase-extraction/overview) | [Entity recognition](https://learn.microsoft.com/en-us/ai-builder/entity-extraction-overview)

**Overview**

- Azure AI Language can extract important information from text
- **Key phrase extraction** identifies the main points
- **Entity recognition** identifies people, places, organizations, dates, and more

**Key Points**

- Supports multiple languages
- Custom Named Entity Recognition (NER) available for domain-specific terms
- Outputs structured JSON with identified entities and categories

!!! tip "Exam Tip"
    Watch for use cases: *summarizing topics → key phrases, identifying people/places → entities*

---

## :material-lightbulb-on: Determine Sentiment of Text

📖 **Docs:** [Sentiment analysis](https://learn.microsoft.com/azure/ai-services/language-service/sentiment-opinion-mining/overview)

**Overview**

- Sentiment analysis detects **positive, neutral, or negative** opinions in text
- Opinion mining extracts targeted sentiment about specific aspects

**Key Points**

- Returns sentiment scores for document, sentence, and aspect levels
- Supports social media, customer reviews, and survey feedback
- Multilingual support

!!! example "Use Case"
    Analyzing customer reviews to detect satisfaction levels

---

## :material-lightbulb-on: Detect the Language Used in Text

📖 **Docs:** [Language detection](https://learn.microsoft.com/azure/ai-services/language-service/language-detection/overview)

**Overview**

- Identifies the primary language of a text input
- Supports over 100 languages

**Key Points**

- Returns language name and ISO 639-1 code
- Provides confidence score
- Useful for routing text to the correct translation or processing service

!!! tip "Exam Tip"
    Keywords like *detect language before translation* → Language Detection API

---

## :material-lightbulb-on: Detect Personally Identifiable Information (PII) in Text

📖 **Docs:** [PII detection](https://learn.microsoft.com/azure/ai-services/language-service/personally-identifiable-information/overview)

**Overview**

- Detects and redacts sensitive data such as:
    - Names
    - Phone numbers
    - Credit card numbers
    - Social Security Numbers

**Key Points**

- Can return redacted text or structured PII entities
- Helps ensure compliance (GDPR, HIPAA, etc.)
- Configurable for different entity categories

!!! warning "Exam Tip"
    Questions may ask how to **mask sensitive data** in text → answer: **PII detection**

---

## :material-lightbulb-on: Translate Text and Documents by Using the Azure AI Translator Service

📖 **Docs:** [Translator service overview](https://learn.microsoft.com/azure/ai-services/translator/)

**Overview**

- Azure AI Translator provides real-time **text translation**
- Supports over 100 languages
- Modes:
    - Text-to-text
    - Document translation (PDF, Word, etc.)

**Key Points**

- Uses neural machine translation
- Can integrate with applications via REST API or SDKs
- Document translation preserves layout and formatting

!!! example "Use Case"
    Translating contracts from English to French while keeping original structure

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 **Key phrases** = main points, **Entities** = names, places, dates
- 📌 **Sentiment analysis** = positive/neutral/negative + opinion mining
- 📌 **Language detection** returns ISO code + confidence score
- 📌 **PII detection** redacts sensitive info for compliance
- 📌 **Translator** = text + document translation with formatting preserved