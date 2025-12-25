# 🧠🏥 Neuro-ICU Early Deterioration Prediction  
### Multimodal Temporal Modeling for Early Ventilation Risk

This project implements a specialized deep-learning framework to **predict early clinical deterioration in Neuro-ICU patients**, specifically the need for **invasive mechanical ventilation within 12 hours of admission**. Unlike generic early-warning systems, the model captures **neurology-specific physiological and documentation patterns** to support timely, targeted clinical intervention.

---

## 🚀 Overview
Early detection of deterioration in the Neuro-ICU is critical, as subtle changes in consciousness or respiration can signal severe complications. This repository presents a **gated multimodal deep-learning approach** that integrates diverse data sources collected during the **first 6 hours of admission**.

---

## 🧠 Key Methodology
- **Specialized Cohort:** Neuro-ICU patient subset from the **MIMIC-IV** database.
- **Multimodal Fusion:** Gated Multimodal Unit (GMU) dynamically fuses static, temporal, and textual features.
- **Clinical Calibration:** **Isotonic Regression** improves probability reliability and clinical trust.
- **Interpretability:** **SHAP** provides transparent global and patient-level explanations.

---

## 🛠️ Project Modules

### 1️⃣ Data Preprocessing (`preprocessing.ipynb`)
- Extracts and cleans MIMIC-IV data  
- Processes static demographics, vitals, and lab results  
- Prepares clinical text for embedding  

### 2️⃣ Temporal Encoder (`Temporal_encoder_module.ipynb`)
- Models first-6-hour vitals and labs  
- Captures early physiological trends using deep sequence modeling  

### 3️⃣ Textual Embeddings (`BIO+CLINICALBERT.ipynb`)
- Uses **Bio+ClinicalBERT** for clinical notes and radiology reports  
- Captures semantic clinical context absent in structured data  

### 4️⃣ Gated Multimodal Fusion (`fusion_model.ipynb`)
- Integrates static, temporal, and textual representations  
- Gating mechanism prioritizes patient-specific risk signals  

### 5️⃣ Metrics & Interpretability (`Outputs/`)
- **Evaluation:** ROC-AUC, Precision-Recall, Brier Score  
- **Calibration:** Isotonic regression plots  
- **Explainability:** SHAP global and local explanations (top 30 features)

---

## 📊 Key Findings
- **Feature Importance:** Early respiratory trends, radiology documentation, and neuro-specific static features dominate risk prediction.
- **Reliability:** Post-hoc calibration significantly improves probability accuracy for real-time clinical use.

---

## 👥 Contributors
- **Dhatri P Sriram**  
- **Namratha A**  
- **Bhumika L**  
- **Harshini H**  

Developed as part of the **Advanced Foundations for Machine Learning** course at **PES University**.
