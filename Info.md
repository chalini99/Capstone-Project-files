# AI-Powered Crop Disease Detection and Smart Agrochemical Recommendation System

## 1. Project Title

**AI-Powered Crop Disease Detection and Smart Agrochemical Recommendation System**

---

## 2. Project Overview

Agricultural productivity is strongly affected by crop diseases, pest infestations, and inappropriate agricultural-input usage. Early identification of crop diseases is important because delayed diagnosis can allow diseases to spread and can lead to reduced crop yield and quality.

Traditional disease identification commonly depends on manual visual inspection, farmer experience, agricultural experts, or laboratory diagnosis. These approaches may be slow, expensive, or unavailable when a farmer needs an immediate decision.

The proposed project develops an **AI-powered decision-support system** that analyzes crop leaf images, identifies the most likely crop disease, and then provides a **smart agrochemical recommendation** associated with the detected disease.

The central idea is:

```text
Crop Leaf Image
       ↓
Image Preprocessing
       ↓
AI-Based Disease Detection
       ↓
Disease + Confidence
       ↓
Smart Agrochemical Recommendation
       ↓
Treatment Information
       ↓
Farmer/User
```

The project is therefore more than a disease-classification model. Its objective is to connect **diagnosis with an actionable treatment recommendation** through one user-oriented system.

---

# 3. Problem Statement

Crop diseases caused by fungi, bacteria, viruses, and pests can significantly affect agricultural yield and crop quality. Farmers may find it difficult to identify diseases accurately from visual symptoms, particularly when symptoms are similar across diseases.

Existing approaches can suffer from:

- Dependence on manual inspection
- Requirement for agricultural experts
- Delayed diagnosis
- Difficulty identifying visually similar diseases
- Limited access to laboratory diagnosis
- Unnecessary or inappropriate agrochemical application
- Lack of direct connection between disease diagnosis and treatment recommendation

Many AI-based agricultural systems focus primarily on **disease classification**, while recommendation systems often work independently using soil, crop, nutrient, or environmental information.

### Problem to be addressed

> **How can an AI-based system automatically identify crop diseases from leaf images and provide an appropriate, disease-aware agrochemical recommendation through a single, user-friendly application?**

---

# 4. Motivation

## 4.1 Early Disease Detection

Early detection can help farmers identify potentially harmful diseases before they spread extensively.

## 4.2 Reduction of Manual Diagnosis

Computer vision and deep learning can assist with visual disease identification and reduce dependence on manual inspection.

## 4.3 Actionable Diagnosis

A disease label alone may not be sufficient for a farmer. The system should connect:

```text
Disease Identified
        ↓
What should be done?
```

The recommendation component addresses this requirement.

## 4.4 More Targeted Agrochemical Use

Disease-aware recommendations can support more targeted agricultural-input selection instead of indiscriminate chemical use.

## 4.5 Farmer-Oriented Decision Support

The system is intended to provide a simple workflow:

```text
Upload Image → Get Diagnosis → Get Recommendation
```

---

# 5. Aim

> **To develop an AI-powered agricultural decision-support system that detects crop diseases from leaf images and generates smart agrochemical recommendations based on the detected disease and relevant agricultural context.**

---

# 6. Objectives

### Objective 1 — Image-Based Disease Detection

Develop and evaluate an AI/deep-learning model for detecting crop diseases from leaf images.

### Objective 2 — Disease Classification

Classify an input crop image into the appropriate healthy/disease category supported by the selected dataset.

### Objective 3 — Smart Agrochemical Recommendation

Develop a recommendation component that maps the detected disease and relevant crop/context information to appropriate agrochemical treatment information.

### Objective 4 — Integration

Integrate disease detection and agrochemical recommendation into a single application.

### Objective 5 — User-Friendly Interface

Provide a simple web/mobile interface for image upload and presentation of the results.

### Objective 6 — Performance Evaluation

Evaluate the disease-detection model using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Inference time where relevant

Evaluate the recommendation component using suitable measures such as:

- Recommendation accuracy
- Top-k recommendation accuracy
- Precision/recall where applicable
- Coverage
- Expert/agronomic validation

---

# 7. Scope of the Project

## Included

- Crop leaf image acquisition
- Image preprocessing
- AI/deep-learning-based disease detection
- Disease classification
- Confidence-score generation
- Agrochemical recommendation
- Agricultural knowledge/recommendation database
- Web or mobile application
- Model evaluation
- Recommendation evaluation

## Optional Enhancements

Depending on time and available data:

- Disease severity estimation
- Soil information
- Weather information
- Crop growth stage
- Pest information
- Explainable AI
- Recommendation ranking
- Multicrop support
- Multilingual farmer interface

## Not Required by the Updated Project Title

The following are **not part of the current project scope**:

- Post-Quantum Cryptography
- ML-KEM
- ML-DSA
- PQ-TLS
- Quantum-resistant cloud communication

These belonged to the previous project version and should not be included in the current Review 1 presentation unless the project scope is changed again.

---

# 8. Target Users

## Primary Users

- Farmers
- Small and medium-scale agricultural users

## Secondary Users

- Agricultural consultants
- Agricultural extension workers
- Agronomists
- Researchers
- Smart-farming organizations

The intended interaction is through a web/mobile application where the user uploads or captures a crop leaf image.

---

# 9. Proposed System Architecture

```text
                         USER / FARMER
                              │
                              ▼
                    ┌───────────────────┐
                    │ Web / Mobile UI   │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Image Acquisition │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Image Preprocessing│
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ AI Disease Model  │
                    │ CNN / Transformer │
                    │ / YOLO etc.       │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Disease +         │
                    │ Confidence Score  │
                    └─────────┬─────────┘
                              │
                              ▼
              ┌────────────────────────────────┐
              │ Smart Recommendation Engine    │
              └───────────────┬────────────────┘
                              │
                  ┌───────────┴───────────┐
                  ▼                       ▼
           Disease/Crop Data       Agricultural Knowledge
                  │                       │
                  └───────────┬───────────┘
                              ▼
                    ┌───────────────────┐
                    │ Agrochemical      │
                    │ Recommendation    │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Result Presentation│
                    └─────────┬─────────┘
                              ▼
                         USER / FARMER
```

---

# 10. End-to-End Workflow

```text
START
  │
  ▼
User uploads/captures leaf image
  │
  ▼
Validate image
  │
  ▼
Preprocess image
  │
  ▼
AI disease detection
  │
  ▼
Predicted disease + confidence
  │
  ▼
Confidence acceptable?
  │
 ┌┴──────────────┐
 │               │
NO              YES
 │               │
 ▼               ▼
Ask user for    Recommendation
better image     engine
                 │
                 ▼
       Disease + Crop + Context
                 │
                 ▼
       Agricultural knowledge base
                 │
                 ▼
       Ranked treatment options
                 │
                 ▼
       Display recommendation
                 │
                 ▼
                END
```

---

# 11. Module 1 — Crop Disease Detection

## Input

A crop/plant leaf image.

## Processing

1. Image acquisition
2. Image validation
3. Resizing
4. Normalization
5. Data augmentation during training
6. Feature extraction
7. Disease classification
8. Confidence calculation

## Output

Example:

```text
Crop: Tomato

Predicted Disease:
Early Blight

Confidence:
95.4%
```

The exact crops and disease classes must be determined by the dataset selected for the implementation.

---

# 12. Image Preprocessing

## 12.1 Image Acquisition

The user uploads an image or captures one using a camera.

## 12.2 Image Validation

The application should check whether the uploaded image is likely to contain the relevant crop/leaf rather than accepting every arbitrary image.

## 12.3 Resizing

Resize the image to the input dimensions required by the selected model.

Examples may include:

- 224 × 224
- 256 × 256
- 416 × 416
- 640 × 640

The final size depends on the selected architecture.

## 12.4 Normalization

Pixel values are normalized according to the preprocessing requirements of the selected model.

## 12.5 Data Augmentation

Training data may be augmented using:

- Rotation
- Horizontal/vertical flipping where agronomically appropriate
- Zoom
- Cropping
- Translation
- Brightness variation
- Contrast variation

Augmentation should reflect realistic field variations rather than creating unrealistic images.

---

# 13. Disease Detection Model Options

Potential models include:

## CNN-Based Models

- Custom CNN
- VGG16
- ResNet
- MobileNet
- EfficientNet

## Object Detection

- YOLO-based models

Useful when the task requires locating disease regions/objects rather than only classifying the complete image.

## Transformer-Based Models

- Vision Transformer
- Lightweight Vision Transformers

## Transfer Learning

For a capstone project, transfer learning can be useful when the available labeled dataset is limited.

Example:

```text
Pretrained Model
      ↓
Replace Classification Head
      ↓
Train on Crop Dataset
      ↓
Fine-Tune
      ↓
Evaluate
```

---

# 14. Model Selection Strategy

Do not select a model only because it has the highest accuracy in a published paper.

Evaluate candidate models using:

| Factor                | Why Important                        |
| --------------------- | ------------------------------------ |
| Accuracy              | Correct classification               |
| Precision             | False-positive control               |
| Recall                | Disease detection sensitivity        |
| F1-score              | Balance between precision and recall |
| Model size            | Deployment feasibility               |
| Inference time        | User response speed                  |
| Dataset compatibility | Fair comparison                      |
| Generalization        | Field applicability                  |
| Explainability        | User/researcher trust                |

A useful experimental comparison could be:

```text
VGG16
   vs
ResNet50
   vs
MobileNetV3
   vs
EfficientNet
   ↓
Compare performance
   ↓
Select final model
```

The exact comparison should depend on the team's computational resources and dataset.

---

# 15. Disease Detection Evaluation

## Accuracy

```text
Accuracy = (TP + TN) / (TP + TN + FP + FN)
```

Measures the overall proportion of correct predictions.

## Precision

```text
Precision = TP / (TP + FP)
```

Measures how many predicted positive cases are actually positive.

## Recall

```text
Recall = TP / (TP + FN)
```

Measures how many actual positive cases are detected.

## F1-Score

```text
F1 = 2 × (Precision × Recall) / (Precision + Recall)
```

Useful when both precision and recall are important.

## Confusion Matrix

A confusion matrix shows:

- Correct disease predictions
- Incorrect disease predictions
- Healthy/disease confusion
- Confusion between similar diseases

---

# 16. Dataset Strategy

The project requires a clearly defined dataset strategy.

## Dataset A — Disease Detection

A disease dataset should contain:

```text
Image
Crop
Disease/Class
```

Example:

| Image        | Crop   | Class        |
| ------------ | ------ | ------------ |
| image001.jpg | Tomato | Healthy      |
| image002.jpg | Tomato | Early Blight |
| image003.jpg | Tomato | Late Blight  |
| image004.jpg | Potato | Healthy      |

### Candidate public datasets

- PlantVillage
- PlantDoc
- Crop-specific disease datasets
- Other openly licensed agricultural image datasets

### Important

Do not claim that a model works for crops/diseases that are not represented in its training/evaluation data.

---

# 17. Dataset Splitting

A typical experimental split can be:

```text
Dataset
   │
   ├── Training Set
   ├── Validation Set
   └── Test Set
```

For example:

```text
70% Training
15% Validation
15% Testing
```

or another justified split.

The exact split should be selected based on dataset size and class distribution.

Avoid data leakage by ensuring near-duplicate images or images from the same source are not unintentionally distributed across training and test sets.

---

# 18. Recommendation Module

The recommendation module is the second major contribution.

## Basic Concept

```text
Detected Disease
       ↓
Crop Information
       ↓
Disease Knowledge Base
       ↓
Treatment Matching
       ↓
Agrochemical Recommendation
```

The recommendation system can consider:

- Crop
- Detected disease
- Disease severity
- Crop growth stage
- Pest/pathogen information
- Environmental conditions
- Soil information where relevant
- Agricultural recommendations
- Approved product information

---

# 19. Recommendation Approaches

## Approach 1 — Rule-Based Recommendation

Example:

```text
IF crop = Tomato
AND disease = Early Blight
THEN retrieve validated treatment options
```

### Advantages

- Easy to implement
- Easy to explain
- Easy to validate
- Suitable for an initial capstone prototype

### Limitations

- Less adaptive
- Requires maintaining agricultural rules
- Does not automatically learn from new data

---

# 20. Machine-Learning Recommendation

The system can learn from historical agricultural data.

Possible inputs:

```text
Crop
Disease
Severity
Soil
Weather
Growth Stage
N/P/K
Past Treatment
       ↓
ML Recommendation Model
       ↓
Ranked Treatment Options
```

Potential models:

- Random Forest
- Decision Tree
- XGBoost
- SVM
- KNN

The recommendation model should only be trained if a sufficiently reliable and appropriately labeled dataset is available.

---

# 21. Hybrid Recommendation — Recommended Direction

A hybrid approach can combine:

```text
AI Disease Prediction
          +
Agricultural Rules
          +
Validated Treatment Database
          +
Optional ML Ranking
          ↓
Smart Agrochemical Recommendation
```

This is preferable to allowing a machine-learning model to generate completely unconstrained chemical recommendations.

The system should retrieve/rank treatments from a **validated knowledge base**, rather than inventing chemical names, active ingredients, or dosages.

---

# 22. Agrochemical Knowledge Base

A possible database structure:

## Crop Table

```text
crop_id
crop_name
```

## Disease Table

```text
disease_id
crop_id
disease_name
symptoms
pathogen_type
```

## Agrochemical Table

```text
chemical_id
product_name
chemical_type
active_ingredient
target_disease
```

## Recommendation Table

```text
recommendation_id
disease_id
chemical_id
crop
conditions
source
validation_status
```

The exact chemical/product information should come from reliable agricultural sources and applicable product labels/regulations.

---

# 23. Safe Recommendation Design

Because the system gives agricultural treatment information, the recommendation layer should be designed carefully.

The application should:

- Prefer validated agricultural sources.
- Avoid unsupported chemical recommendations.
- Avoid fabricating product names or active ingredients.
- Avoid providing unsupported dosage instructions.
- Display label/regulatory guidance where appropriate.
- Consider crop-specific registration.
- Distinguish between disease identification confidence and treatment certainty.
- Provide an option to consult an agricultural expert for uncertain cases.

A useful result format is:

```text
Detected Disease:
[ Disease Name ]

Confidence:
[ XX% ]

Recommended Treatment Category:
[ Fungicide / Insecticide / Pesticide ]

Validated Treatment Option(s):
[ Retrieved from knowledge base ]

Important:
Follow the approved product label and local
agricultural/regulatory guidance.
```

---

# 24. Recommendation Ranking

If several validated treatment options are available, the system can rank them using:

```text
Disease Match
      +
Crop Match
      +
Growth Stage
      +
Environmental Conditions
      +
Severity
      +
Knowledge-Base Reliability
      ↓
Recommendation Score
```

This is more meaningful than simply returning the first chemical stored in the database.

---

# 25. Explainability

Explainability can improve trust.

For disease detection, possible techniques include:

- Grad-CAM
- Grad-CAM++
- Saliency maps
- Attention visualization

Example:

```text
Leaf Image
    ↓
Disease Prediction
    ↓
Grad-CAM
    ↓
Highlighted Symptom Region
```

The user can see which part of the leaf influenced the model prediction.

For recommendations, provide a short reason:

```text
Disease detected: Early Blight
Crop: Tomato
Recommendation selected because:
- It is associated with the detected disease.
- It is listed for the crop in the validated knowledge base.
```

---

# 26. Confidence Handling

A critical part of the system is handling uncertain predictions.

Example:

```text
Confidence ≥ Threshold
        ↓
Show disease + recommendation

Confidence < Threshold
        ↓
Ask user for another image
        OR
Show "Low-confidence prediction"
        OR
Recommend expert verification
```

Do not present an uncertain AI prediction as a confirmed diagnosis.

---

# 27. User Interface

## Home Screen

```text
---------------------------------
 AI Crop Doctor
---------------------------------

Upload Leaf Image

[ Choose Image ]

[ Capture Image ]

          [ Analyze ]

---------------------------------
```

## Result Screen

```text
---------------------------------
 Disease Detection Result
---------------------------------

Crop:
Tomato

Disease:
Early Blight

Confidence:
95.4%

[ View Explanation ]

---------------------------------

Smart Agrochemical Recommendation

Treatment Category:
Fungicide

Validated Options:
...

[ Safety / Label Information ]

---------------------------------
```

---

# 28. Proposed Technology Stack

## AI/ML

- Python
- TensorFlow/Keras or PyTorch
- Scikit-learn
- OpenCV

## Backend

Possible:

- Flask
- FastAPI

## Frontend

Possible:

- React
- HTML/CSS/JavaScript
- Flutter

## Database

Possible:

- MySQL
- PostgreSQL
- MongoDB
- Firebase

## Deployment

Possible:

- Local prototype
- Cloud-hosted backend
- Web application
- Mobile application

The final stack should be selected based on what the team can implement and demonstrate reliably.

---

# 29. Functional Requirements

### FR1 — Image Upload

The user shall be able to upload a crop leaf image.

### FR2 — Image Validation

The system shall validate the input before analysis.

### FR3 — Disease Prediction

The system shall predict the crop disease using the trained AI model.

### FR4 — Confidence Score

The system shall provide the prediction confidence.

### FR5 — Recommendation

The system shall retrieve/generate a suitable agrochemical recommendation for a valid disease prediction.

### FR6 — Result Display

The system shall display the disease and recommendation in an understandable format.

### FR7 — Database Management

The system shall store disease and recommendation information.

### FR8 — Error Handling

The system shall handle unsupported, unclear, or low-quality images.

---

# 30. Non-Functional Requirements

## Accuracy

The model should achieve an acceptable classification performance on unseen test data.

## Performance

Prediction should be sufficiently fast for practical application use.

## Usability

The interface should be simple enough for non-technical users.

## Reliability

The system should avoid presenting low-confidence predictions as certain diagnoses.

## Maintainability

Disease and treatment information should be updateable without rebuilding the complete application.

## Scalability

The architecture should allow additional crops/diseases to be added later.

---

# 31. Database / Backend Architecture

```text
                  FRONTEND
                     │
                     ▼
                BACKEND API
                     │
          ┌──────────┴───────────┐
          ▼                      ▼
     AI MODEL               DATABASE
          │                      │
          ▼                      ▼
 Disease Prediction       Disease Information
          │                Agrochemical Data
          │                Recommendation Rules
          └──────────┬───────────┘
                     ▼
              Recommendation
                     │
                     ▼
                  FRONTEND
```

---

# 32. Security and Privacy — Current Scope

Although post-quantum cryptography is no longer part of the project title, normal application security should still be considered.

Basic measures can include:

- Input validation
- Authentication if user accounts are implemented
- Secure API configuration
- Access control
- Safe database queries
- Secure storage of user data
- Avoiding unnecessary personal information collection

Security should remain a **normal software-engineering requirement**, not a separate PQC research component.

---

# 33. Testing Strategy

## Unit Testing

Test individual components:

- Image preprocessing
- Prediction function
- Recommendation lookup
- Database operations

## Integration Testing

Test:

```text
Upload
 → Preprocess
 → Predict
 → Recommend
 → Display
```

## Model Testing

Use an unseen test dataset.

Measure:

- Accuracy
- Precision
- Recall
- F1
- Confusion matrix

## Recommendation Testing

Create test cases such as:

```text
Input Disease A
→ Expected valid treatment set

Input Disease B
→ Expected valid treatment set
```

## User Acceptance Testing

Evaluate whether users can:

1. Upload an image.
2. Understand the prediction.
3. Understand the recommendation.
4. Navigate the application.

---

# 34. Experimental Plan

## Experiment 1 — Baseline

Train a baseline CNN.

## Experiment 2 — Transfer Learning

Evaluate pretrained architectures.

## Experiment 3 — Data Augmentation

Compare performance with and without augmentation.

## Experiment 4 — Model Comparison

Compare selected models using the same train/validation/test protocol.

## Experiment 5 — Field Robustness

If field images are available, evaluate the final model on images different from the training dataset.

## Experiment 6 — Recommendation Evaluation

Evaluate disease-to-treatment recommendations against the validated knowledge base and, where possible, agricultural/expert validation.

---

# 35. Expected Results

The expected system should:

1. Detect supported crop diseases from leaf images.
2. Produce a disease confidence score.
3. Provide a relevant agrochemical recommendation.
4. Present the result through a simple interface.
5. Reduce the number of separate steps required by a farmer.
6. Demonstrate measurable AI performance using standard metrics.
7. Provide an explainable/traceable basis for recommendations where implemented.

---

# 36. Literature-Based Research Gap

Existing literature shows strong progress in AI-based crop disease detection using CNNs, transfer learning, object detection and Transformer-based models. Other research has demonstrated the feasibility of using machine learning, IoT, soil parameters, nutrient information and agricultural knowledge for fertilizer and crop-management recommendations. However, these capabilities are frequently developed as separate systems. Disease-detection models commonly stop at producing a disease label, while agricultural recommendation systems often depend on soil, crop, weather or nutrient information without directly using image-based disease diagnosis. In addition, many studies are crop-specific, dataset-dependent, or evaluated under controlled conditions. Therefore, there is a need for an integrated and farmer-oriented system that connects **image-based crop disease detection with validated, disease-aware smart agrochemical recommendation**.

---

# 37. Research Gaps — Bullet Form

- Limited integration of AI disease detection and agrochemical recommendation.
- Many disease-classification systems stop after identifying the disease.
- Existing fertilizer/recommendation systems often operate independently from image-based disease diagnosis.
- Many datasets are collected under controlled conditions and may not represent field variability.
- Crop-specific datasets limit generalization to additional crops.
- Similar visual symptoms can create classification challenges.
- Disease severity is not consistently incorporated into recommendation systems.
- Agricultural recommendation quality depends strongly on the quality and reliability of the knowledge/data source.
- Many ML systems provide limited explanation for their recommendations.
- Recommendation systems need crop-, region- and condition-specific validation.
- A farmer-oriented end-to-end workflow remains an important practical requirement.
- There is a need to connect **diagnosis → treatment decision** within one application.

---

# 38. Proposed Novelty

The project should **not** claim to invent a completely new CNN architecture or a new agrochemical.

The defensible novelty is:

> **Integration of AI-based crop disease detection with disease-aware smart agrochemical recommendation in a unified farmer-oriented decision-support system.**

### Core contribution

```text
AI Diagnosis
     +
Disease-Aware Recommendation
     +
Agricultural Knowledge
     ↓
Integrated Smart Agriculture Application
```

---

# 39. Existing System vs Proposed System

| Feature                          | Typical Existing Disease System | Typical Recommendation System | Proposed System                      |
| -------------------------------- | ------------------------------- | ----------------------------- | ------------------------------------ |
| Leaf image input                 | ✓                              | Usually no                    | ✓                                   |
| Disease detection                | ✓                              | Usually no                    | ✓                                   |
| Disease classification           | ✓                              | No                            | ✓                                   |
| Crop/soil/context information    | Sometimes                       | ✓                            | Optional/✓                          |
| Fertilizer recommendation        | Usually no                      | ✓                            | Optional depending on implementation |
| Agrochemical recommendation      | Limited                         | Sometimes                     | ✓                                   |
| Disease-aware recommendation     | Limited                         | Limited                       | ✓                                   |
| Explainable prediction           | Some systems                    | Some systems                  | Planned/optional                     |
| Farmer-oriented UI               | Some systems                    | Some systems                  | ✓                                   |
| Integrated diagnosis + treatment | Limited                         | Limited                       | ✓                                   |

---

# 40. Proposed System Differentiation

```text
Existing Study 1
      ↓
Disease Detection

Existing Study 2
      ↓
Disease Detection + XAI

Existing Study 3
      ↓
Fertilizer Recommendation

Existing Study 4
      ↓
Agricultural Decision Support

                 ↓

             PROPOSED
               SYSTEM
                 │
        ┌────────┴────────┐
        ▼                 ▼
 Disease Detection   Agrochemical
                     Recommendation
        │                 │
        └────────┬────────┘
                 ▼
        Unified Application
```

---

# 41. Base Paper Direction

For the disease-detection component, a strong base/reference should preferably come from an **IEEE Transactions** journal or a high-quality Elsevier agricultural AI journal and should cover image-based plant disease detection, computer vision, deep learning and dataset/generalization challenges.

For the recommendation component, an appropriate base/reference should preferably be an **Elsevier Computers and Electronics in Agriculture / Agricultural Systems** paper dealing directly with fertilizer, nutrient or agricultural decision support.

The final base papers should be selected only after checking:

- Exact journal status
- DOI
- Publication year
- Dataset
- Methodology
- Relevance to the exact implementation
- Whether the paper can genuinely serve as a technical foundation

Do not label a conference paper as a journal paper.

---

# 42. Recommended Base-Paper Strategy for This Project

## Base Paper A — Disease Detection

Use a high-quality paper focused on:

- Computer vision for plant disease detection
- Deep learning
- Crop/leaf image datasets
- Disease classification/detection
- Generalization and field conditions

### Why?

It provides the technical foundation for:

```text
Leaf Image
   ↓
Preprocessing
   ↓
Deep Learning
   ↓
Disease Detection
```

## Base Paper B — Agrochemical Recommendation

Use a paper focused on:

- Fertilizer/nutrient recommendation
- Agricultural decision support
- Knowledge-based recommendation
- ML-based agricultural recommendation

### Why?

It provides the foundation for:

```text
Disease/Crop/Context
        ↓
Recommendation Engine
        ↓
Treatment Recommendation
```

---

# 43. Limitations of the Proposed Project

The project should acknowledge realistic limitations.

### Dataset limitation

The AI model can only recognize diseases represented adequately in its training data.

### Field-condition limitation

Performance may decrease for poor-quality images or conditions not represented in training data.

### Recommendation limitation

A recommendation system is only as reliable as its agricultural knowledge base and validation sources.

### Regional limitation

Agrochemical availability, registration, usage restrictions and recommendations can differ by region.

### Expert-validation limitation

A capstone prototype may not replace professional agronomic diagnosis or official product-label guidance.

### Model limitation

A high test accuracy does not guarantee perfect real-world performance.

---

# 44. Future Enhancements

Possible future work includes:

- More crop species
- More disease classes
- Field-image datasets
- Disease severity estimation
- Pest detection
- Weather integration
- Soil sensor integration
- Personalized recommendations
- Multilingual support
- Voice-based farmer interaction
- Explainable AI
- Mobile deployment
- Offline inference
- Continuous knowledge-base updates
- Expert feedback integration

---

# 45. Project Deliverables

## Deliverable 1

Curated/preprocessed crop-disease dataset.

## Deliverable 2

Trained AI disease-detection model.

## Deliverable 3

Disease-detection evaluation report.

## Deliverable 4

Agrochemical recommendation knowledge base.

## Deliverable 5

Recommendation engine.

## Deliverable 6

Integrated backend.

## Deliverable 7

Web/mobile user interface.

## Deliverable 8

Integrated working prototype.

## Deliverable 9

Testing and performance report.

## Deliverable 10

Final documentation and presentation.

---

# 46. Suggested Development Phases

## Phase 1 — Requirement Analysis

- Finalize supported crops.
- Finalize supported diseases.
- Define recommendation scope.
- Identify datasets.
- Identify reliable agricultural information sources.

## Phase 2 — Dataset Preparation

- Collect/download permitted datasets.
- Remove corrupt images.
- Check class balance.
- Preprocess images.
- Split data correctly.

## Phase 3 — Disease Model

- Establish baseline.
- Train candidate models.
- Compare metrics.
- Select final model.

## Phase 4 — Recommendation System

- Design disease-treatment knowledge base.
- Define recommendation rules/features.
- Implement recommendation engine.
- Validate outputs.

## Phase 5 — Application

- Build frontend.
- Build backend API.
- Connect AI model.
- Connect recommendation database.

## Phase 6 — Integration

```text
Frontend
   ↓
Backend
   ↓
AI Model
   ↓
Disease Result
   ↓
Recommendation Engine
   ↓
Database
   ↓
Final Result
```

## Phase 7 — Testing

- Functional testing
- Model testing
- Integration testing
- Recommendation validation
- User testing

## Phase 8 — Documentation

- Literature review
- Methodology
- Results
- Research gap
- Discussion
- Limitations
- Future work

---

# 47. Suggested Team Work Distribution

If the project has multiple team members, work can be divided into:

### Member 1 — Disease Detection

- Dataset
- Preprocessing
- CNN/DL models
- Evaluation

### Member 2 — Recommendation

- Agricultural data
- Treatment knowledge base
- Recommendation logic/model
- Validation

### Member 3 — Application

- Frontend
- Backend
- API integration
- Database

### Member 4 — Integration/Research

- System integration
- Testing
- Literature review
- Documentation
- Presentation

All members should understand the complete workflow for the final review/viva.

---

# 48. What the Panel Should Understand

The project is not:

> "We trained a CNN to classify leaves."

It is:

> **"We are building an integrated agricultural decision-support system where AI first identifies the crop disease and the resulting diagnosis is used to provide a validated, disease-aware agrochemical recommendation."**

This distinction is important for demonstrating the project's contribution.

---

# 49. One-Line Project Explanation

> **An AI-powered system that detects crop diseases from leaf images and provides smart, disease-aware agrochemical recommendations to support timely agricultural decision-making.**

---

# 50. 30-Second Viva Explanation

> "Our project focuses on AI-powered crop disease detection and smart agrochemical recommendation. The user provides a crop leaf image, which is preprocessed and analyzed using a deep-learning model to identify the disease and its confidence. The detected disease is then passed to a recommendation engine that uses a validated agricultural knowledge base, and where available relevant crop or environmental information, to provide suitable treatment options. The final result is presented through a simple web or mobile interface. Our main research gap is the limited integration of image-based disease diagnosis and disease-aware agrochemical recommendation in a single farmer-oriented system."

---

# 51. Final Project Flow for PPT

```text
             ┌───────────────────┐
             │   CROP LEAF IMAGE │
             └─────────┬─────────┘
                       ↓
             ┌───────────────────┐
             │ IMAGE PREPROCESSING│
             └─────────┬─────────┘
                       ↓
             ┌───────────────────┐
             │ AI DISEASE        │
             │ DETECTION         │
             └─────────┬─────────┘
                       ↓
             ┌───────────────────┐
             │ DISEASE +         │
             │ CONFIDENCE        │
             └─────────┬─────────┘
                       ↓
             ┌───────────────────┐
             │ SMART             │
             │ RECOMMENDATION    │
             └─────────┬─────────┘
                       ↓
             ┌───────────────────┐
             │ VALIDATED         │
             │ AGROCHEMICAL      │
             │ OPTIONS           │
             └─────────┬─────────┘
                       ↓
             ┌───────────────────┐
             │ WEB / MOBILE APP  │
             └───────────────────┘
```

---

# 52. Final Summary

The proposed **AI-Powered Crop Disease Detection and Smart Agrochemical Recommendation System** aims to address an important agricultural decision-making problem by connecting automated crop disease diagnosis with treatment recommendation.

The system receives a crop leaf image, preprocesses the image, applies a trained AI model to identify the disease, and uses the detected disease together with relevant agricultural information to retrieve or rank appropriate agrochemical treatment options from a validated knowledge base.

The key contribution is the **integration of diagnosis and recommendation**, rather than developing another standalone disease-classification model.

The project can therefore be represented as:

```text
             INPUT
          Leaf Image
              │
              ▼
      AI Disease Detection
              │
              ▼
       Disease Diagnosis
              │
              ▼
    Smart Recommendation
              │
              ▼
   Validated Treatment Options
              │
              ▼
        Farmer/User
```

> **Core Contribution = AI Disease Detection + Disease-Aware Agrochemical Recommendation + Farmer-Oriented Decision Support**
