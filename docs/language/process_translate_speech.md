# Process and Translate Speech

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers working with **Azure AI Speech** for speech recognition, synthesis, and translation. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Integrate Generative AI Speaking Capabilities in an Application

📖 **Docs:** [Azure AI Speech overview](https://learn.microsoft.com/azure/ai-services/speech-service/overview)

**Overview**

- Azure AI Speech integrates with generative AI (e.g., GPT) to enable **AI-powered conversational agents with voice**
- Supports:
    - Conversational copilots
    - Voice-enabled chatbots
    - Real-time spoken interactions

**Key Points**

- Combines **text generation (Azure OpenAI)** + **speech synthesis (AI Speech)**
- Requires low latency for natural conversation
- Can run on mobile, desktop, or embedded devices

!!! example "Use Case"
    Voice-enabled customer service assistant powered by GPT + Azure Speech

---

## :material-lightbulb-on: Implement Text-to-Speech and Speech-to-Text Using Azure AI Speech

📖 **Docs:** [Speech-to-text](https://learn.microsoft.com/azure/ai-services/speech-service/speech-to-text) | [Text-to-speech](https://learn.microsoft.com/azure/ai-services/speech-service/text-to-speech)

**Overview**

- **Speech-to-Text (STT):** converts spoken audio to text
- **Text-to-Speech (TTS):** converts text to natural-sounding speech

**Key Points**

- STT supports real-time and batch transcription
- TTS supports multiple voices and languages
- Neural TTS provides high-quality, natural voices

!!! tip "Exam Tip"
    Keywords: *speech recognition* → STT, *voice synthesis* → TTS

---

## :material-lightbulb-on: Improve Text-to-Speech by Using Speech Synthesis Markup Language (SSML)

📖 **Docs:** [SSML reference](https://learn.microsoft.com/azure/ai-services/speech-service/speech-synthesis-markup)

**Overview**

- SSML customizes speech output beyond plain text
- Features:
    - Pronunciation adjustments
    - Emphasis and prosody
    - Pauses and pacing
    - Voice selection

**Key Points**

- SSML allows fine control of synthesized speech
- Supports phoneme definitions for correct pronunciation
- Can specify speaking styles (cheerful, empathetic, etc.)

!!! example "SSML Example"
```xml
<speak version="1.0" xml:lang="en-US">
  <voice name="en-US-AriaNeural">
    Hello, <break time="500ms"/> how are you today?
  </voice>
</speak>
```

---

## :material-lightbulb-on: Implement Custom Speech Solutions with Azure AI Speech

📖 **Docs:** [Custom speech](https://learn.microsoft.com/azure/ai-services/speech-service/custom-speech-overview)

**Overview**

- Custom speech improves recognition accuracy for:
    - Domain-specific vocabulary
    - Industry jargon
    - Unique accents or dialects

**Key Points**

- Requires collection of sample audio and transcripts
- Models are trained using **Custom Speech portal** or APIs
- Useful in healthcare, finance, technical industries

!!! warning "Exam Tip"
    *Custom speech* = improving accuracy for specialized vocabulary

---

## :material-lightbulb-on: Implement Intent and Keyword Recognition with Azure AI Speech

📖 **Docs:** [Keyword and intent recognition](https://learn.microsoft.com/azure/ai-services/speech-service/keyword-recognition-overview)

**Overview**

- Detects **specific keywords** or **user intents** from spoken input
- Common for wake words and command recognition

**Key Points**

- Can trigger specific actions in applications
- Works offline with precompiled keyword models
- Useful for IoT and voice-controlled devices

!!! example "Use Case"
    Detecting “Hey Contoso” to activate a smart assistant

---

## :material-lightbulb-on: Translate Speech-to-Speech and Speech-to-Text by Using the Azure AI Speech Service

📖 **Docs:** [Speech translation](https://learn.microsoft.com/azure/ai-services/speech-service/speech-translation)

**Overview**

- Azure AI Speech supports real-time **speech translation**
- Modes:
    - Speech-to-speech
    - Speech-to-text (translated output)

**Key Points**

- Supports dozens of source and target languages
- Real-time streaming for conversations
- Can integrate with chat or conferencing platforms

!!! tip "Exam Tip"
    *Translate spoken conversations* → Speech Translation API

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 **Generative AI + Speech** = voice-enabled AI copilots 
- 📌 **STT** = speech recognition, **TTS** = voice synthesis
- 📌 **SSML** customizes pronunciation, pacing, style
- 📌 **Custom speech** improves accuracy for domain-specific vocab
- 📌 **Keyword/intent recognition** → wake words, commands
- 📌 **Speech translation** = real-time multilingual communication