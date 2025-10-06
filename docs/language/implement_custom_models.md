# Implement Custom Language Models

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers building and deploying **custom language models** with Azure AI Language and related services. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Create Intents, Entities, and Add Utterances

📖 **Docs:** [Language Understanding (LUIS) migration to Conversational Language Understanding](https://learn.microsoft.com/azure/ai-services/language-service/conversational-language-understanding/overview)

**Overview**

- **Intents** = user goals (e.g., "BookFlight")
- **Entities** = data extracted (e.g., "Paris" as destination)
- **Utterances** = example phrases to train model

**Key Points**

- Provide diverse utterances to improve accuracy
- Entities can be prebuilt (dates, numbers) or custom
- Used in chatbots, assistants, and task automation

---

## :material-lightbulb-on: Train, Evaluate, Deploy, and Test a Language Understanding Model

📖 **Docs:** [Quickstart: Conversational language understanding](https://learn.microsoft.com/azure/ai-services/language-service/conversational-language-understanding/quickstart)

**Overview**

- Training uses labeled intents and entities
- Evaluation ensures performance
- Deployment makes model available via endpoint

**Key Points**

- Metrics: precision, recall, F1 score
- Deploy models to staging or production slots
- Test with new utterances for real-world accuracy

!!! tip "Exam Tip"
    Staging slot for testing, production slot for live apps

---

## :material-lightbulb-on: Optimize, Backup, and Recover Language Understanding Model

📖 **Docs:** [Back up and recover your conversational language understanding models](https://learn.microsoft.com/en-us/azure/ai-services/language-service/conversational-language-understanding/how-to/fail-over)

**Overview**

- Optimization involves retraining with new utterances
- Backup ensures models can be restored
- Recovery allows rollback after errors

**Key Points**

- Export/import projects for portability
- Regular retraining improves accuracy
- Versioning helps track model changes

---

## :material-lightbulb-on: Consume a Language Model from a Client Application

📖 **Docs:** [Quickstart: Conversational language understanding](https://learn.microsoft.com/en-us/azure/ai-services/language-service/conversational-language-understanding/quickstart?pivots=rest-api)

**Overview**

- Applications call deployed models via REST API or SDKs
- Input: user utterance
- Output: intent + entities + confidence score

**Key Points**

- Requires endpoint URL and key
- Supports real-time integration into bots and apps
- JSON response can trigger business logic

!!! example "Use Case"
    Chatbot calling CLU to extract intent and act on it

---

## :material-lightbulb-on: Create a Custom Question Answering Project

📖 **Docs:** [Custom Question Answering overview](https://learn.microsoft.com/azure/ai-services/language-service/question-answering/overview)

**Overview**

- Custom QnA project enables building a knowledge base
- Uses semi-structured or unstructured data as input

**Key Points**

- Sources: FAQ docs, URLs, PDFs
- Knowledge base provides structured Q&A pairs
- Supports conversational interaction

---

## :material-lightbulb-on: Add Question-and-Answer Pairs and Import Sources

📖 **Docs:** [What is custom question answering?](https://learn.microsoft.com/en-us/azure/ai-services/language-service/question-answering/overview)

**Overview**

- Add manual Q&A pairs
- Import FAQs from documents or URLs
- Supports multiple sources per knowledge base

**Key Points**

- Automatic extraction generates suggested Q&A pairs
- Manual editing improves accuracy

---

## :material-lightbulb-on: Train, Test, and Publish a Knowledge Base

📖 **Docs:** [Create, test, and deploy: CQA knowledge base](https://learn.microsoft.com/en-us/azure/ai-services/language-service/question-answering/how-to/create-test-deploy)

**Overview**

- Training refines extracted Q&A pairs
- Testing validates accuracy
- Publishing exposes an endpoint

**Key Points**

- Knowledge base must be published to be consumed
- Endpoint integrates with client applications
- Supports iterative improvement

---

## :material-lightbulb-on: Create a Multi-Turn Conversation

📖 **Docs:** [Add guided conversations with multi-turn prompts](https://learn.microsoft.com/en-us/azure/ai-services/language-service/question-answering/tutorials/guided-conversations)

**Overview**

- Multi-turn = follow-up questions within context
- Supports contextual conversations

**Key Points**

- Requires linking related Q&A pairs
- Improves chatbot interactivity
- Maintains conversation state

---

## :material-lightbulb-on: Add Alternate Phrasing and Chit-Chat to a Knowledge Base

📖 **Docs:** [Improve quality of response with synonyms](https://learn.microsoft.com/en-us/azure/ai-services/language-service/question-answering/tutorials/adding-synonyms)

**Overview**

- Alternate phrasing improves recognition of user queries
- Chit-chat adds casual responses to non-task queries

**Key Points**

- Reduces fallback to “no answer”
- Improves conversational flow
- Prebuilt chit-chat sets available

---

## :material-lightbulb-on: Export a Knowledge Base

📖 **Docs:** [Create, test, and deploy: CQA knowledge base](https://learn.microsoft.com/en-us/azure/ai-services/language-service/question-answering/how-to/create-test-deploy)

**Overview**

- Knowledge bases can be exported to JSON
- Supports backup, migration, and versioning

**Key Points**

- Importing restores or replicates KBs
- Useful for moving between environments

---

## :material-lightbulb-on: Create a Multi-Language Question Answering Solution

📖 **Docs:** [Create projects in multiple languages](https://learn.microsoft.com/en-us/azure/ai-services/language-service/question-answering/tutorials/multiple-languages)

**Overview**

- Projects can contain multilingual content

**Key Points**

- Detect language first, then route query
- Translator can pre-process inputs
- Requires maintaining localized KBs

---

## :material-lightbulb-on: Implement Custom Translation

📖 **Docs:** [Custom Translator](https://learn.microsoft.com/azure/ai-services/translator/custom-translator/overview)

**Overview**

- Custom Translator allows domain-specific translations
- Supports training with parallel text corpora

**Key Points**

- Improves accuracy for industry terms
- Custom models must be trained and published
- Integrated with Azure Translator API

!!! warning "Exam Tip"
    *Translator* = general use, *Custom Translator* = domain-specific

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 **Intents** = goals, **Entities** = extracted data, **Utterances** = examples  
- 📌 CLU models trained, evaluated, deployed to endpoints
- 📌 **Metrics:** precision, recall, F1
- 📌 Custom QnA builds KBs from docs/FAQs
- 📌 **Multi-turn conversations** = contextual Q&A 
- 📌 Alternate phrasing + chit-chat improve coverage
- 📌 **Export KB** = backup/migration
- 📌 Multi-language QnA + Custom Translator for global solutions