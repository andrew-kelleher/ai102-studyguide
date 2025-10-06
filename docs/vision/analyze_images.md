# Analyze Images

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers analyzing images with **Azure AI Vision**. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Select Visual Features to Meet Image Processing Requirements

📖 **Docs:** [Azure AI Vision features](https://learn.microsoft.com/azure/ai-services/computer-vision/overview)

**Overview**

- Azure AI Vision can extract a variety of features from images
- Features include:
    - Tags
    - Objects
    - Categories
    - Descriptions
    - OCR (printed and handwritten text)
    - Spatial analysis

**Key Points**

- Select features based on requirements
- Multiple features can be combined in a single request
- Feature choice affects cost and performance

!!! tip "Exam Tip"
    Watch for scenario questions mapping **requirements → correct feature**

---

## :material-lightbulb-on: Detect Objects in Images and Generate Image Tags

📖 **Docs:** [Object detection](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/concept-object-detection)

**Overview**

- Object detection identifies entities within an image
- Image tagging generates a set of descriptive labels

**Key Points**

- Tags include confidence scores
- Object detection provides bounding boxes
- Can identify thousands of common objects

!!! example "Use Case"
    Retail solution detecting products on shelves with bounding boxes

---

## :material-lightbulb-on: Include Image Analysis Features in an Image Processing Request

📖 **Docs:** [What is Image Analysis?](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/overview-image-analysis)

**Overview**

- Image processing requests specify which features to analyze
- Request payload includes:
    - Image source (URL or binary data)
    - List of features

**Key Points**

- REST API and SDKs available (Python, C#, Java, JavaScript)
- Features requested determine output fields
- Can batch multiple images in one request

!!! tip "Exam Tip"
    Remember that **URL or binary data** can be used as inputs

---

## :material-lightbulb-on: Interpret Image Processing Responses

📖 **Docs:** [Image descriptions](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/concept-describing-images)

**Overview**

- Responses contain structured JSON results
- Includes:
    - Tags with confidence
    - Object bounding boxes
    - Category hierarchy
    - Text regions for OCR

**Key Points**

- Always check confidence thresholds
- Low-confidence results may need filtering
- Can integrate results with downstream apps (search, indexing, etc.)

!!! info "Best Practices"
    Filter out results below a set confidence threshold for production apps

---

## :material-lightbulb-on: Extract Text from Images Using Azure AI Vision

📖 **Docs:** [OCR - Optical Character Recognition](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/overview-ocr)

**Overview**

- OCR extracts printed text from images and documents
- Works with multiple languages
- Provides text lines and bounding box coordinates

**Key Points**

- OCR is asynchronous for large documents
- Text can be returned in plain text or structured format
- Often combined with Document Intelligence for advanced extraction

!!! example "Use Case"
    Digitizing scanned contracts into searchable text

---

## :material-lightbulb-on: Convert Handwritten Text Using Azure AI Vision

📖 **Docs:** [Vision Portal demo](https://portal.vision.cognitive.azure.com/demo/extract-text-from-images)

**Overview**

- Recognizes handwritten text in images and documents
- Supports cursive and block-style handwriting
- Returns extracted text and bounding boxes

**Key Points**

- Accuracy depends on handwriting quality
- Works best with clear, high-resolution scans
- Can be used in note-taking or form digitization apps

!!! tip "Exam Tip"
    Keywords like *handwriting* or *forms with writing* → Azure AI Vision handwriting OCR

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 **Visual features**: tags, objects, categories, descriptions, OCR  
- 📌 **Object detection** → bounding boxes, tagging → descriptive labels  
- 📌 Requests can use **URL** or **binary input**, features specified per request  
- 📌 Responses contain **confidence** **scores**, **bounding boxes**, **structured JSON**  
- 📌 OCR extracts **printed text**, Handwriting OCR extracts **cursive/block text**