# Analyze Videos

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers analyzing videos with **Azure AI Video Indexer** and **Azure AI Vision Spatial Analysis**. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Use Azure AI Video Indexer to Extract Insights from a Video or Live Stream

📖 **Docs:** [Azure AI Video Indexer overview](https://learn.microsoft.com/azure/azure-video-indexer/video-indexer-overview)

**Overview**

- Video Indexer extracts insights from recorded or live video streams
- Capabilities:
    - Speech-to-text transcription
    - Face detection and recognition
    - Object detection
    - Scene segmentation
    - Sentiment analysis from audio
    - OCR from video frames
    - Translation and subtitling

**Key Points**

- Can process uploaded videos or connect to live streams
- Integrates with Azure Media Services
- Outputs JSON with structured insights for search and analytics

!!! example "Use Case"
    Generating transcripts, detecting people and keywords in training videos, enabling video search

---

## :material-lightbulb-on: Use Azure AI Vision Spatial Analysis to Detect Presence and Movement of People in Video

📖 **Docs:** [Azure Computer Vision - Spatial Analysis Tutorial](https://github.com/tsmatz/azure-spatial-analysis)

**Overview**

- Spatial Analysis processes video feeds from cameras to understand movement and presence of people
- Capabilities:
    - Person detection and counting
    - Line crossing detection
    - Dwell time analysis
    - Social distancing monitoring

**Key Points**

- Runs on edge devices using containers
- Requires GPU-enabled infrastructure
- Privacy features such as anonymization (blurring faces/bodies) are included
- Integrates with IoT and video analytics platforms

!!! tip "Exam Tip"
    Keywords like *detecting people, movement, dwell time, or occupancy* → **Spatial Analysis**

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 **Video Indexer** = speech-to-text, OCR, sentiment, face/object detection, scene segmentation  
- 📌 Supports both **uploaded video** and **live streams**  
- 📌 Outputs structured insights for indexing and search  
- 📌 **Spatial Analysis** = detects presence, movement, dwell time of people  
- 📌 Runs in **containers on edge devices**, requires GPU  
- 📌 Includes **privacy features** (blurring, anonymization)  
