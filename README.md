Multimodal AI Framework for Employability Skill, Emotion and Physiological State Detection
> Accepted at **ICTEST 2026** (International Conference on Testing and Evaluation of Software and Systems)
---
About
Traditional hiring processes rely on grades and resume screening — missing critical indicators like communication skills, emotional stability, confidence, and stress resilience that actually predict job performance.

This project builds a multimodal deep learning framework that evaluates employability by analyzing:

📄 Resume text
🎙️ Interview speech
😊 Facial expressions
🧠 Physiological signals (EEG + ECG)

The system integrates all four modalities using deep learning and graph neural networks to generate a comprehensive employability score and job recommendation — achieving 92.5% accuracy.

---
Results
| Metric | Value |
|---|---|
| Accuracy | **92.5%** |
| Precision | 91.0% |
| Recall | 93.0% |
| F1 Score | 92.0% |
| AUC-ROC | **95.0%** |
| Specificity | 94.0% |

### Model Comparison
| Model | Accuracy | AUC-ROC |
|---|---|---|
| Text Only | 88.4% | 90.1% |
| Signal Based | 89.0% | 91.2% |
| **Proposed Multimodal** | **93.1%** | **94.2%** |
---
System Architecture
The framework processes four input modalities independently, extracts features using modality-specific deep learning models, fuses them, and maps the result to employability skill clusters via a Graph Neural Network (GNN).
```
Resume Text     → BERT (Transformer)          ─┐
Interview Audio → Whisper AI + RNN            ─┤
Facial Images   → CNN (224×224)               ─┼→ Multimodal Fusion → GNN Skill Graph → Job Recommendation
ECG/EEG Signals → CNN-LSTM (Bandpass Filter)  ─┘
```
---
Dataset
Modality	Data Type	Source	Purpose
Text	Resume profiles	Public dataset (2,400 entries)	Skill extraction
Speech	Interview audio	Public dataset (300+ speakers)	Communication analysis
Facial Image	Facial expressions	Public dataset (35,000+ samples)	Emotion detection
ECG	Physiological signals	Public biomedical dataset (32 participants)	Stress estimation
EEG	Physiological signals	62-channel corpus (256 Hz)	Cognitive state assessment
---
Methodology
A. Data Preprocessing
Text: Tokenization, stop-word removal, sentence-level normalization for BERT input
Speech: Noise reduction → ASR (Whisper AI) → filler-word removal → transcript normalization
Facial Images: Face detection → cropping → resize to 224×224 → pixel normalization
ECG/EEG: Bandpass filtering → fixed-length window segmentation → z-score normalization
B. Feature Extraction
Modality	Model	Purpose
Text	Transformer (BERT)	Contextual skill representation
Speech	Recurrent Neural Network	Temporal speech analysis
Image	CNN	Facial feature extraction
ECG/EEG	Convolutional Neural Network	Signal pattern extraction
C. Skill Relationship Modeling
A Graph Neural Network (GNN) models relationships between detected skills. Each node = one skill, each edge = co-occurrence strength derived from multimodal features. This produces a weighted skill graph for employability inference.
D. Skill Inference & Job Recommendation
The GNN output maps skill combinations to relevant career roles, ranking recommendations by skill-profile alignment.
---
Skill Distribution (Detected)
Skill Category	Percentage
Technical Skills	35%
Communication Skills	20%
Problem Solving Skills	18%
Leadership Skills	15%
Emotional & Cognitive Readiness	12%
---
Tech Stack
Python
BERT — resume and text skill extraction
Whisper AI — automatic speech recognition
CNN / CNN-LSTM — facial and physiological signal processing
RNN — speech feature extraction
Graph Neural Network (GNN) — skill relationship modeling
PyPDF2 — resume parsing
Gradio — interactive demo interface
Kaggle — model training environment
---
Repository Structure
```
Employabilityskilldetection/
├── employabilityskilldetection.ipynb  → main model notebook
├── Employabilityskilldetectioncode    → Kaggle version
├── README.md                          → this file
└── LICENSE                            → all rights reserved
```
---
Key Contributions
First framework to simultaneously integrate text, speech, facial, and physiological data for employability assessment
Hybrid CNN-LSTM architecture for non-stationary EEG signal processing
Graph-based skill relationship modeling for structured competency inference
93.1% multimodal accuracy vs 88.4% text-only baseline — 4.7% improvement
---
Citation
If you reference this work, please cite:
```
P. Harini, S. Harshini, C. Hari Varshini, V. Gayathri, S. Jalaja,
"Multimodal AI Framework for Employability Skill, Emotion and Physiological State Detection,"
International Conference on Testing and Evaluation of Software and Systems (ICTEST), 2026.
```
---
License
All rights reserved. This code is shared for portfolio and academic reference only.
See LICENSE for details.
Contact: harininithya16@gmail.com  
LinkedIn: linkedin.com/in/harini-palanisamy-85b703340
