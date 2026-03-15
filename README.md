Multimodal Employability Skill Assessment using Deep Learning

Overview

Traditional employability evaluation methods mainly rely on academic performance and resume screening. These approaches often fail to capture important qualities such as communication ability, behavioral traits, confidence, and emotional stability that influence real workplace performance.

This project proposes a multimodal deep learning framework to evaluate employability skills by analyzing multiple data sources including resume text, interview speech, facial images, and physiological signals (ECG and EEG). By combining these modalities, the system attempts to identify hidden employability indicators that are usually missed by traditional recruitment processes.

The extracted features from different modalities are integrated using deep learning techniques and further analyzed using a graph-based learning approach to generate an overall employability score.


---

Objectives

To design a multimodal system for employability skill assessment

To analyze resume text for technical and soft-skill indicators

To evaluate communication clarity and confidence from interview speech

To capture behavioral cues from facial image analysis

To estimate stress and cognitive engagement using physiological signals

To combine all extracted features for accurate employability prediction



---

Technologies Used

Python

Deep Learning

Convolutional Neural Networks (CNN)

Long Short-Term Memory Networks (LSTM)

Graph-Based Learning

Natural Language Processing (NLP)

Speech Signal Processing

Image Processing



---

Dataset

The project uses publicly available datasets and collected sample data for different modalities.

You can access the dataset from the link below:

Dataset Link:
ECG Heartbeat Categorization Dataset
1)/kaggle/input/heartbeat/mitbih_test.csv
2)/kaggle/input/heartbeat/mitbih_train.csv
3)/kaggle/input/heartbeat/ptbdb_abnormal.csv
4)/kaggle/input/heartbeat/ptbdb_normal.csv
fer2013
/kaggle/input/fer2013

resume-dataset
/kaggle/input/resume-dataset/resume_data.csv

EEG brainwave dataset: mental state
/kaggle/input/eeg-brainwave-dataset-mental-state/mental-state.csv


---

Methodology

The proposed system follows a multimodal analysis approach:

1. Resume Text Analysis
Resume data is processed using text analysis techniques to identify technical skills and soft-skill indicators.


2. Speech Analysis
Interview speech recordings are analyzed to measure clarity, fluency, and confidence of expression.


3. Facial Image Analysis
Facial images are used to observe visible behavioral cues and expressions during interaction.


4. Physiological Signal Processing
ECG and EEG signals are used to estimate stress levels and cognitive engagement.


5. Feature Integration
Features extracted from all modalities are combined using deep learning models.


6. Employability Prediction
A graph-based learning model is used to represent relationships between skills and generate an overall employability score.




---

Results

Experimental evaluation using controlled test scenarios and publicly available datasets shows that the proposed multimodal framework achieves an employability prediction accuracy of approximately 91.2%, which performs better than traditional resume-only screening approaches.


---

Project Structure

project-folder
│
├── dataset
├── preprocessing
├── models
├── training
├── evaluation
├── results
└── README.md


---

Applications

Intelligent recruitment systems

AI-based interview assessment platforms

Human resource analytics

Candidate skill evaluation tools



---

Future Improvements

Integration with real-time interview platforms

Larger multimodal datasets for better training

Improved emotion and behavior recognition models

Real-world deployment for recruitment support systems



---

Author

Harini Palanisamy
