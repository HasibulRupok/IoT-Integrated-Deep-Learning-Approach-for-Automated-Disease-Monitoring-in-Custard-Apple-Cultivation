# 🌱 IoT-Integrated Deep Learning Approach for Automated Disease Monitoring in Custard Apple Cultivation

This repository contains the implementation and supporting materials for the research paper:

> **IoT-Integrated Deep Learning Approach for Automated Disease Monitoring in Custard Apple Cultivation**  
> *Published at the ITSS-IoE 2025 Conference*  
> 🔗 Conference link: https://ritechs.org/conferences/ITSS-IoE2025

---

## 📄 Overview

Custard apple (*Annona squamosa*) is highly susceptible to multiple fungal and pest-related diseases that significantly reduce yield and crop quality. Early and accurate disease detection is critical for sustainable cultivation.

This project proposes a **hybrid deep learning architecture integrated with an IoT-enabled smart agriculture framework** to automatically detect custard apple diseases from fruit and leaf images. The system combines multiple pretrained CNN models with channel-wise attention and is designed to be deployable in **edge–cloud IoT environments**.

---

## 🚀 Key Contributions

- ✅ Hybrid CNN architecture combining:
  - MobileNetV2  
  - ResNet152V2  
  - ConvNeXt-Tiny  
- ✅ Squeeze-and-Excitation (SE) attention mechanism for feature recalibration  
- ✅ Six-class disease classification with **99.15% accuracy**
- ✅ IoT-enabled smart agriculture framework for real-time disease monitoring
- ✅ Designed for edge devices (ESP32-CAM, Raspberry Pi) and cloud-based inference

---

## 🧠 Model Architecture

The proposed model:
1. Extracts features independently using three pretrained CNNs  
2. Applies **SENet** modules for channel-wise attention  
3. Concatenates features into a unified representation  
4. Performs final classification using a fully connected network  

This stacked architecture improves robustness and generalization compared to single-model approaches.

Below is the architecture diagram used in our proposed model:

![Model Architecture](https://raw.githubusercontent.com/HasibulRupok/IoT-Integrated-Deep-Learning-Approach-for-Automated-Disease-Monitoring-in-Custard-Apple-Cultivation/main/architecture.png)

---

## 🦠 Disease Classes

The system classifies the following **six custard apple diseases**:

1. Anthracnose  
2. Black Canker  
3. Diplodia Rot  
4. Cylindrocladium Leaf Spot (Fruit)  
5. Cylindrocladium Leaf Spot (Leaf)  
6. Mealy Bug  

---

## 📊 Dataset

- **Source:** Publicly available dataset collected from Nimgaon-Bhogi, Pune, India  
- **Total images:** 8,226  
- **Image type:** JPG (resized to 1024 × 768)  
- **Data includes:** Fruit and leaf images under real-world conditions  

📌 Dataset reference:  
*Thite et al., Data in Brief, 2024*

---
---

## ⚙️ Training Details

- **Loss function:** Categorical Cross-Entropy  
- **Optimizer:** Adam  
- **Learning rate:** 0.0001  
- **Regularization:** Batch Normalization & Dropout  
- **Evaluation metrics:** Accuracy, Precision, Recall, F1-score  

---

## 🧪 Results

| Model | Accuracy |
|------|---------|
| VGG19 | 68% |
| ResNet152V2 | 71% |
| MobileNetV2 | 79% |
| ConvNeXt-Tiny | 84% |
| **Proposed Hybrid Model** | **99.15%** |

The model achieved **precision, recall, and F1-score ≈ 0.99** across all disease classes.

---

## 🌐 IoT-Enabled Framework

The proposed system extends beyond image classification into a **real-world smart agriculture solution**:

### Architecture Layers

- **Edge Layer:** ESP32-CAM / Raspberry Pi for image capture & lightweight inference  
- **Communication Layer:** MQTT, LoRaWAN, or NB-IoT  
- **Processing Layer:** Hybrid edge–cloud deep learning inference  
- **Application Layer:** Mobile/Web dashboard for farmer alerts and recommendations  

This design enables **real-time monitoring**, **scalable deployment**, and **precision farming**.

---

## 🔮 Future Work

- Field-level IoT deployment and validation
- Expansion to other crop species
- Federated learning for privacy-preserving model updates
- Automated actuation (smart irrigation, drone spraying)

---

## 🤝 Authors

Hasibul Hasan Rupok
> 🌐 hasibul-rupok.com

and co-authors

---

## 📜 License

This project is licensed under the **MIT License**.

You are free to:
- Use the code for research, academic, and commercial purposes
- Modify and adapt the code
- Distribute and sublicense the code

Under the following conditions:
- Proper attribution must be given to the original authors
- The license notice must be included in all copies or substantial portions of the software

📄 See the [LICENSE](LICENSE) file for full license details.

