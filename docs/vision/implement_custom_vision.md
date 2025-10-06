# Implement Custom Vision Models

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers building, training, and deploying **custom vision models**. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts

---

## :material-lightbulb-on: Choose Between Image Classification and Object Detection Models

📖 **Docs:** [What is Custom Vision?](https://learn.microsoft.com/azure/cognitive-services/custom-vision-service/overview)

**Overview**

- **Image classification**: predicts the overall category of an image
- **Object detection**: identifies and locates multiple objects within an image using bounding boxes

**Key Points**

- Use classification when one label per image is enough
- Use object detection when multiple items need identifying
- Both require labeled training data

!!! tip "Exam Tip"
    Scenario question: *“Identify multiple items in a photo”* → **Object detection**

---

## :material-lightbulb-on: Label Images

📖 **Docs:** [Tag and label images](https://learn.microsoft.com/azure/cognitive-services/custom-vision-service/get-started-build-detector)

**Overview**

- Labeled images are required for supervised learning
- Images must be uploaded and tagged with the correct category

**Key Points**

- Tags must be consistent across training set
- At least **15–30 images per tag** recommended
- Balanced datasets improve accuracy

!!! info "Best Practices"
    Use diverse images (lighting, angle, resolution) for robust models

---

## :material-lightbulb-on: Train a Custom Image Model

📖 **Docs:** [Train custom models](https://learn.microsoft.com/azure/cognitive-services/custom-vision-service/getting-started-build-a-classifier)

**Overview**

- Training uses the uploaded and labeled dataset
- Types:
    - **Image classification**
    - **Object detection**

**Key Points**

- Quick Training → faster, less accurate
- Advanced Training → slower, more accurate
- Requires multiple iterations for tuning

!!! tip "Exam Tip"
    Training type and dataset size impact **accuracy and cost**

---

## :material-lightbulb-on: Evaluate Custom Vision Model Metrics

📖 **Docs:** [Evaluate model performance](https://learn.microsoft.com/azure/cognitive-services/custom-vision-service/getting-started-build-a-classifier#train-the-project)

**Overview**

- Evaluation metrics help measure model quality
- Metrics:
    - **Precision** = true positives ÷ (true positives + false positives)
    - **Recall** = true positives ÷ (true positives + false negatives)
    - **mAP** (mean average precision) for object detection

**Key Points**

- Tradeoff: precision vs recall
- High recall = fewer missed detections
- High precision = fewer false positives

!!! warning "Exam Tip"
    Expect formula-style questions on **precision vs recall**

---

## :material-lightbulb-on: Publish a Custom Vision Model

📖 **Docs:** [Train a Computer Vision Model with Azure Custom Vision](https://blog.roboflow.com/train-azure-custom-vision-model/)

**Overview**

- After training, models must be published to an endpoint
- Published models can be accessed via API calls

**Key Points**

- Each project can have multiple iterations
- Must publish the correct iteration for inference
- Endpoint includes prediction URL and key

---

## :material-lightbulb-on: Consume a Custom Vision Model

📖 **Docs:** [Call the Prediction API](https://learn.microsoft.com/azure/cognitive-services/custom-vision-service/use-prediction-api)

**Overview**

- Use REST API or SDKs to submit images for prediction
- Input formats: URL or binary image data

**Key Points**

- Predictions include label + confidence score
- Results returned in JSON format
- Supports batch processing

!!! example "Use Case"
```python
import requests

url = "https://<endpoint>/customvision/v3.0/Prediction/<project-id>/classify/iterations/<iteration>/image"
headers = {"Prediction-Key": "KEY", "Content-Type": "application/octet-stream"}

with open("test.jpg", "rb") as f:
    resp = requests.post(url, headers=headers, data=f)
print(resp.json())
```

---

## :material-lightbulb-on: Build a Custom Vision Model Code First

📖 **Docs:** [Quickstart: Custom Vision SDK](https://learn.microsoft.com/azure/cognitive-services/custom-vision-service/quickstarts/image-classification)

**Overview**

- Custom Vision models can be built programmatically
- SDKs available for Python, C#, Java, JavaScript

**Key Points**

- Code-first approach automates image upload, labeling, training, and publishing
- Useful for MLOps pipelines
- Enables integration with CI/CD workflows

!!! info "Best Practices"
    Use code-first when automating retraining or scaling projects

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 **Classification** = one label per image, **Detection** = multiple objects with bounding boxes  
- 📌 Label images consistently, minimum ~15–30 per tag  
- 📌 **Training**: Quick = fast, Advanced = accurate  
- 📌 **Metrics**: Precision, Recall, mAP  
- 📌 Models must be **published** to be consumed  
- 📌 Predictions return **JSON with confidence scores**  
- 📌 Code-first approach enables automation and CI/CD integration