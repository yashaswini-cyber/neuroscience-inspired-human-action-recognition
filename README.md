#  Neuroscience-Inspired Multi-Module Deep Learning Framework for Human Action Recognition

> **Predictive Coding × Micro-Movement Encoding × Context Fusion**
> A biologically-motivated, interpretable, and robust HAR pipeline achieving **72.8% Top-1 accuracy** on UCF101.


## 📌 **Overview**

Humans understand actions by **predicting missing motion**, noticing **micro-movements**, and incorporating **scene context**.
This project brings those neuroscience ideas into a real deep-learning pipeline:

### 1) **Predictive Completion Module (PCM)**

* BiLSTM predicts **occluded or missing joints**
* Inspired by **predictive coding** in the brain

### 2) **Micro-Movement Encoder (MME)**

* Residual Conv1D blocks detect **tiny spatio-temporal differences**
* Helps classify subtle actions (dribbling vs passing)

### 3) **Context Fusion Network (CFN)**

* Fuses **pose** + **scene** features with attention
* Adds semantic context (ball, bat, water, environment)

---

## 📊 **Results (UCF101)**

| Metric              | Score     |
| ------------------- | --------- |
| **Top-1 Accuracy**  | **72.8%** |
| **Macro Precision** | **0.754** |
| **Macro Recall**    | **0.722** |
| **Macro F1 Score**  | **0.722** |

Competitive with vanilla RGB models while being **interpretable**, **modular**, and **bio-inspired**.

---

## 🧠 **Architecture Summary**

<img width="614" height="639" alt="image" src="https://github.com/user-attachments/assets/ed7f066e-31e5-401c-8a07-d4b0bb5b3d7b" />


```
Input Frames (32) 
   ├── YOLOv8-Pose → 17 keypoints/frame  
   ├── PCM (BiLSTM Reconstruction)
   ├── MME (Residual Conv1D Micro-movement Extractor)
   ├── CFN (ResNet50 Scene Encoder + Attention Fusion)
Output: Action Class (UCF101)
```


## **Key Strengths :-**

*  **Biologically inspired deep learning architecture**
*  **Interpretable** using attention maps & pose reconstructions
*  **Competitive accuracy on a major benchmark**
*  **Clear modular code** following real research pipelines
*  **End-to-end reproducible notebook** with webcam inference
*  **Perfect for ML / CV / Deep Learning roles**

---

## **Future Work :-**

* Cross-dataset validation (HMDB51, Kinetics)
* Incorporating temporal transformers
* 3D pose fusion
* Real-time deployment optimizations

---
