# Literature Review — AI-Powered Crop Disease Detection and Smart Agrochemical Recommendation System

## Project Title

**AI-Powered Crop Disease Detection and Smart Agrochemical Recommendation System**

---

## THEME 1: AI-Based Crop Disease Detection

### Papers 1–5

| S.No | Author Name, Journal, Year                                          | Research / Methodology                                                                              | Dataset Used                                                                              | Performance Metrics                                                                                           | Advantages                                                                                         | Disadvantages                                                                           |
| ---- | ------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| 1    | **S. K. Mahmudul Hassan, A. K. Maji**, *IEEE Access*, 2022  | Novel CNN using Inception + residual connections and depthwise-separable convolution                | **PlantVillage, Rice Disease, Cassava Disease**                                     | **99.39%** PlantVillage; **99.66%** Rice; **76.59%** Cassava accuracy                       | High accuracy with fewer parameters; suitable for efficient deployment                             | Performance drops considerably on cassava; field-condition generalization not addressed |
| 2    | **C. J. Xan et al.**, *IEEE Access*, 2024                   | MobileNet V1/V2, FD-MobileNet, ResNet and SqueezeNet optimized for ARM-M microcontroller deployment | **5,932 rice-leaf images**, 4 diseases: bacterial blight, blast, brown spot, tungro | FD-MobileNet:**98.44% accuracy**                                                                        | Lightweight and suitable for real-time edge deployment                                             | Limited to rice diseases and resource-constrained hardware                              |
| 3    | **R. Maurya, L. Rajput, S. Mahapatra**, *IEEE Access*, 2025 | **RAI-Net:** ResNet18 + channel attention + Inception; Grad-CAM for explainability            | **22,930 tomato-leaf images**, 10 classes                                           | **97.88% accuracy** on 4,595 test images                                                                | Multi-scale feature extraction + explainability; strong tomato disease classification              | Dataset lacks real-world field testing                                                  |
| 4    | **W. Xiao et al.**, *IEEE Access*, 2025                     | Class-agnostic contrastive localization + supervised classification + sparse orthogonal mapping     | **5,763 citrus-leaf images**, 6 categories                                          | **97.1% accuracy**                                                                                      | Designed for complex field conditions; handles illumination, occlusion and background interference | Focused on citrus; larger-scale validation still needed                                 |
| 5    | **T.-C. Pham et al.**, *IEEE Access*, 2025                  | Iterative active learning with diverse sample selection for reducing annotation requirements        | **VIECOLD and BRACOL coffee-leaf datasets**                                         | F1 improvement**1.7% / 0.9%**; only **35% / 50%** labelled data can outperform full-data baseline | Reduces expensive manual annotation; improves data efficiency                                      | Requires iterative labeling and carefully selected samples                              |

### Paper Links

1. [IEEE Xplore — Plant Disease Identification Using a Novel CNN](https://ieeexplore.ieee.org/document/9674894/)
2. [IEEE Xplore — Effective Edge Solution for Early Detection of Rice Disease](https://ieeexplore.ieee.org/document/10700722/)
3. [IEEE Xplore — RAI-Net: Tomato Plant Disease Classification](https://ieeexplore.ieee.org/document/10962136/)
4. [IEEE Xplore — Research on Citrus Leaf Disease Recognition](https://ieeexplore.ieee.org/document/10949146/)
5. [IEEE Xplore — Enhancing Coffee Leaf Disease Classification](https://ieeexplore.ieee.org/document/11162523/)

---

## THEME 1: AI-Based Crop Disease Detection

### Papers 6–10

| S.No | Author Name, Journal, Year                                     | Research / Methodology                                                                 | Dataset Used                                                                                     | Performance Metrics                                                                                 | Advantages                                                                         | Disadvantages                                                                                      |
| ---- | -------------------------------------------------------------- | -------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| 6    | **A. Prommakhot et al.**, *IEEE Access*, 2025          | Hybrid CNN + BiLSTM + Transformer sequential-learning architecture                     | **PlantVillage**, 38 plant-disease classes                                                 | **97.88% accuracy**, **97.93% precision**, **97.62% recall**                      | Combines CNN feature extraction with sequential/Transformer learning               | More computationally intensive than conventional CNNs                                              |
| 7    | **P. Chaisiriprasert, K. Chuiad**, *IEEE Access*, 2025 | Lightweight Color-Aware Transformer with hierarchical attention                        | **Plant Disease Classification Merged Dataset**; 21,733 images / 6 categories              | **75% accuracy**, **0.81 mAP**; 3.33G FLOPs vs 17.58G for ViT                           | Lightweight Transformer; suitable for resource-constrained deployment              | Accuracy is lower than several CNN-based approaches; limited disease categories                    |
| 8    | **K. Sathya et al.**, *IEEE Access*, 2025              | Attention-Augmented Residual Network + cGAN augmentation + Faster R-CNN                | Augmented plant-disease image dataset using GAN-generated samples                                | **98.78% classification accuracy**; Faster-RCNN effectiveness improved by **23.84%**    | Strong feature focus; augmentation improves generalization                         | Increased training/inference complexity                                                            |
| 9    | **B. Ramana Reddy et al.**, *IEEE Access*, 2025        | Lightweight custom CNN + OpenCV severity estimation + mobile application               | **PlantVillage**, >54,000 images; 38 original classes; curated healthy/diseased binary set | **92.06% test accuracy**; ~90% precision/recall/F1                                            | Practical mobile deployment; provides disease severity estimation                  | Binary healthy/diseased classification rather than detailed disease-class recommendation           |
| 10   | **T. Ozcan, E. Polat**, *IEEE Access*, 2025            | **BorB** segmentation + augmentation + VGG16/ResNet50/EfficientNetB3/MobileNetV3 | **EruCauliflowerDB**, **MangoLeafBD**, selected PlantVillage classes                 | **100%** EruCauliflowerDB; **100%** MangoLeafBD; **99.78%** selected PlantVillage | Segmentation reduces background interference; excellent classification performance | Extremely high scores on selected datasets may not translate directly to uncontrolled field images |

### Paper Links

6. [IEEE Xplore — Hybrid CNN and Transformer-Based Sequential Learning](https://ieeexplore.ieee.org/document/11072169/)
7. [IEEE Xplore — LCAT Lightweight Color-Aware Transformer](https://ieeexplore.ieee.org/document/11086594/)
8. [IEEE Access — Attention-Augmented Residual Networks + Faster R-CNN](https://ieeexplore.ieee.org/document/11007391/)
9. [IEEE Access — Deep Learning Based Mobile Application for Automated Plant Disease Detection](https://ieeexplore.ieee.org/)
10. [IEEE Access — BorB Plant Disease Classification](https://ieeexplore.ieee.org/)

---

## THEME 2: Smart Agrochemical / Fertilizer Recommendation

### Papers 11–15

| S.No | Author Name, Journal, Year                         | Research / Methodology                                                                                              | Dataset Used                                                                                                           | Performance Metrics                                                                                                    | Advantages                                                                             | Disadvantages                                                                                          |
| ---- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| 11   | **A. A. Khan et al.**, *IEEE Access*, 2022 | IoT-assisted soil fertility mapping + LR, SVM, GNB and KNN for context-aware fertilizer recommendation              | Dataset from**Islamia University Bahawalpur**, combined with fertilizer/crop/soil data; NPK, crop and soil type  | GNB:**96% training**, **94% testing accuracy**; NPK mean differences 0.34, 0.36, −0.13                    | Real-time soil context; directly addresses fertilizer recommendation                   | Dependent on soil sensing and regional data                                                            |
| 12   | **A. Khaliq et al.**, *IEEE Access*, 2025  | AI + IoT + XAI; TabNet for fertilizer recommendation, SwiFT for crop recommendation and TabNet soil-health analysis | Temperature, humidity, moisture, soil type, crop type, N/P/K and fertilizer data                                       | TabNet fertilizer recommendation ≈**99.3% accuracy**; crop recommendation **98.75%**                      | Directly combines crop and fertilizer recommendations with XAI                         | Dataset/domain dependency; fertilizer labels are limited compared with real-world agrochemical choices |
| 13   | **P. Awasthi et al.**, *IEEE Access*, 2025 | Ex-MRConv-RGAN for corn-yield prediction + Hierarchical Fuzzy Model for N/P/K fertilizer recommendations            | **ICRISAT**, NASA POWER weather data and **Fertilizer Association of India** data; **3,960 records** | ~**12% improvement** in prediction accuracy and **15% efficiency improvement** over traditional approaches | Direct fertilizer optimization; combines ML, fuzzy rules and environmental information | Focused on corn and Indian agricultural conditions                                                     |
| 14   | **J. Madhuri et al.**, *IEEE Access*, 2025 | Improved Deep Belief Network using Gaussian RBM + Ranger Optimizer for crop recommendation                          | Soil, weather and crop datasets; four Indian crops:**rice, maize, finger millet, sugarcane**                     | Proposed IDBN outperformed conventional DBN and comparison models                                                      | Uses physical + chemical soil and climate features                                     | Primarily crop recommendation rather than agrochemical recommendation                                  |
| 15   | **A. Badshah et al.**, *IEEE Access*, 2024 | ETC, LR, DT, RF, KNN, GNB and SVM with feature engineering + XAI for crop recommendation; SVR for yield prediction  | **Kaggle crop recommendation dataset** + World Bank/FAO wheat data                                               | RF:**99.7% accuracy** for crop recommendation; SVR: **99.9% R²-based performance** for wheat yield        | Strong ML comparison + XAI; useful for agricultural decision support                   | Recommendation is crop-focused rather than direct chemical recommendation                              |

### Paper Links

11. [IEEE DOI — IoT Assisted Context Aware Fertilizer Recommendation](https://doi.org/10.1109/ACCESS.2022.3228160)
12. [IEEE DOI — AI-Driven Smart Agriculture: Soil Analysis, Irrigation and Crop-Fertilizer Recommendations](https://doi.org/10.1109/ACCESS.2025.3594162)
13. [IEEE DOI — Crop Yield Estimation and Fertilizer Optimization](https://doi.org/10.1109/ACCESS.2025.3646354)
14. [IEEE DOI — Optimizing Crop Recommendations With Improved Deep Belief Networks](https://doi.org/10.1109/ACCESS.2025.3542284)
15. [IEEE DOI — Crop Classification and Yield Prediction Using Robust ML Models](https://doi.org/10.1109/ACCESS.2024.3486653)

---

## THEME 2: Smart Agriculture & Recommendation

### Papers 16–20

| S.No | Author Name, Journal, Year                                          | Research / Methodology                                                                                                          | Dataset Used                                                                            | Performance Metrics                                                                       | Advantages                                                                          | Disadvantages                                                              |
| ---- | ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| 16   | **S. I. Hassan et al.**, *IEEE Access*, 2021                | Systematic review of AI, ML, imaging, IoT, sensors and automation for smart agriculture                                         | **Not applicable — review paper**                                                | Comparative analysis of existing systems                                                  | Covers diseases, pesticides, nutrients, irrigation and agricultural automation      | No experimental recommendation model                                       |
| 17   | **WB-CPI research group**, *IEEE Access*, 2021              | MapReduce + K-means + recommender system using weather, soil, seed and crop-production information                              | Agricultural data from**Ahmednagar, Maharashtra and Andaman & Nicobar Islands**   | Clustering/recommendation evaluation; no single universal accuracy emphasized             | Combines large-scale agricultural data with recommendation                          | Regional data; crop recommendation rather than agrochemical recommendation |
| 18   | **M. N. Mowla et al.**, *IEEE Access*, 2023                 | IoT + Wireless Sensor Networks for smart agriculture, including fertilizer optimization, soil monitoring and disease management | **Not applicable — survey paper**                                                | Comparative review of IoT/WSN technologies                                                | Provides architecture for collecting real-time soil/environmental information       | No standalone recommendation algorithm                                     |
| 19   | **Smart Agriculture research group**, *IEEE Access*, 2024   | Review of AI, cloud computing, big-data analytics, IoT, sensors and agricultural decision-support technologies                  | **Not applicable — review paper**                                                | Comparative review                                                                        | Covers smart agriculture, fertilizer/pesticide optimization, datasets and security  | Review-based; no experimental recommendation accuracy                      |
| 20   | **U. Umar, T. A. Sardjono, H. Kusuma**, *IEEE Access*, 2024 | Ontology + environmental sensors + YOLOv8 + semantic recommendation framework for melon cultivation                             | **Puspalebo Orchard**, East Java; >1,000 melon images + environmental sensor data | System evaluated for recommendation accuracy/reliability and practical farming efficiency | Context-aware recommendations for seed selection, soil, irrigation and pest control | Focused on melon cultivation; ontology requires domain-specific knowledge  |

### Paper Links

16. [IEEE DOI — Systematic Review on Monitoring and Advanced Control Strategies in Smart Agriculture](https://doi.org/10.1109/ACCESS.2021.3057865)
17. [IEEE Xplore — WB-CPI: Weather Based Crop Prediction in India Using Big Data Analytics](https://ieeexplore.ieee.org/document/9557312/)
18. [IEEE Xplore — IoT and Wireless Sensor Networks for Smart Agriculture Applications](https://ieeexplore.ieee.org/document/10371307/)
19. [IEEE DOI — Smart Agriculture: Current State, Opportunities, and Challenges](https://doi.org/10.1109/ACCESS.2024.3471647)
20. [IEEE DOI — Smart Ontology-Based System for Recommending Practices in Melon Cultivation](https://doi.org/10.1109/ACCESS.2024.3487288)

---

# Research Gap

Existing studies predominantly focus on either **AI-based crop disease detection** or **agricultural recommendation systems** independently. Disease-detection approaches achieve high classification performance but generally stop at identifying the disease, while recommendation studies mainly rely on soil, crop, nutrient and environmental parameters without integrating disease-specific information. Hence, there is a need for an integrated AI system that combines **crop disease detection with disease-aware smart agrochemical recommendations** to provide actionable and personalized support to farmers.

# Proposed Work

**AI-Powered Crop Disease Detection and Smart Agrochemical Recommendation System** integrates deep-learning-based disease identification with intelligent agrochemical recommendation using disease, crop and agricultural-condition information.

## Core Contribution

- **Crop Disease Detection:** Identify crop diseases from leaf images using deep learning.
- **Disease-Aware Recommendation:** Generate appropriate agrochemical recommendations based on the detected disease and crop context.
- **Smart Decision Support:** Incorporate relevant agricultural parameters to improve recommendation quality.
- **Integrated System:** Combine disease diagnosis and recommendation in a single farmer-oriented application.
