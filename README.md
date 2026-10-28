<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1A1A1A,100:E07B39&height=180&section=header&text=Hamza%20ELAZAAR&fontSize=44&fontColor=ffffff&fontAlignY=38&desc=AI%20%C2%B7%20Deep%20Learning%20%C2%B7%20Data%20Systems&descSize=16&descAlignY=58" alt="Hamza ELAZAAR banner" />

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=19&duration=3200&pause=900&color=E07B39&center=true&vCenter=true&width=780&lines=MSc+student+in+AI+%26+Digital+Computing;Audio+%C2%B7+Vision+%C2%B7+Transformers+%C2%B7+Federated+Learning;Real-time+pipelines+%C2%B7+Search+%C2%B7+Edge+AI;Open+to+a+PFE+internship+in+AI+%26+Data+%E2%80%94+2027" alt="Typing animation" />

<br/>

<a href="https://linkedin.com/in/hamzaelazaar"><img src="https://img.shields.io/badge/LinkedIn-hamzaelazaar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
<a href="mailto:elazaarhamza5@gmail.com"><img src="https://img.shields.io/badge/Email-elazaarhamza5@gmail.com-E07B39?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
<img src="https://img.shields.io/badge/B%C3%A9ni_Mellal-Morocco-2E7D32?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location"/>

</div>

---

## 👋 About

MSc student in **Artificial Intelligence & Digital Computing** at FST Béni Mellal. I work across the full ML lifecycle: **designing, training and rigorously evaluating models** (CNN, LSTM, XGBoost, Transformer fine-tuning), building the **data pipelines** around them, and wrapping them in **working demos** (Flask, Gradio, React dashboards, embedded hardware).

Areas I work in: `Audio` · `Computer Vision` · `Transformers` · `Federated Learning` · `Information Retrieval` · `Real-time Data` · `Edge / IoT`

> 🎯 **Looking for:** a PFE end-of-studies internship in AI & Data (2027).

---

## 🚀 Projects

### 🎙️ Speech Emotion Recognition — Wav2Vec2 vs CNN vs LSTM
Comparative study of deep-learning architectures for emotion classification on the **RAVDESS** audio corpus.

| Approach | Input representation |
|---|---|
| 2D CNN | Mel spectrograms |
| LSTM | MFCC sequences |
| **Wav2Vec2 fine-tuning** | Raw waveform |

- Feature-extraction pipeline with **Librosa** (Mel spectrograms, MFCC)
- Strict experimental protocol: **stratified split**, same data for every model
- Interactive **Gradio** demo for real-time inference

`PyTorch` `TensorFlow/Keras` `HuggingFace Transformers` `Librosa` `Gradio`

---

### 🌐 NIDS-FL — Federated Learning Network Intrusion Detection
Distributed intrusion-detection system combining **Apache Kafka** and **Federated Learning**: models are trained where the data lives.

<details>
<summary><b>📐 Architecture</b></summary>

```mermaid
flowchart LR
    A[Network capture] --> B[FastAPI]
    B --> C[(Apache Kafka 4.1<br/>KRaft mode)]
    C --> D[Edge: federated MLP<br/>FedAvg · 3 nodes]
    C --> E[Cloud: XGBoost<br/>tuned with Optuna]
    D --> F[(Neo4j<br/>attack graph)]
    E --> F
    D --> G[React dashboard<br/>WebSocket]
    E --> G
```

</details>

- Real-time architecture on **Kafka 4.1 (KRaft)** with fully decoupled services (FastAPI, capture, pipeline)
- **FedAvg** training across 3 distributed nodes through Kafka; binary classification with a federated MLP
- **XGBoost** optimised with **Optuna**; hybrid **Edge/Cloud** pipeline (MLP + XGBoost) to save bandwidth
- **Neo4j** attack-graph visualisation and a real-time **React** supervision dashboard

`Apache Kafka` `Federated Learning` `XGBoost` `Optuna` `Neo4j` `FastAPI` `React` `Docker`

---

### 🫁 COVID-19 & Pneumonia Detection — Chest X-rays
Deep-learning classification of medical images (3 classes) for diagnostic support.

- Preprocessing and ingestion pipeline for a large chest X-ray dataset, **stratified train/val/test split**
- Two architectures compared: **EfficientNetB0** (ImageNet transfer learning + fine-tuning) vs a **custom sequential CNN**
- Evaluation with **confusion matrices** and classification reports (precision, recall, F1)
- 💡 **Takeaway:** a simple, domain-adapted architecture outperformed the complex pre-trained model

`TensorFlow/Keras` `EfficientNetB0` `OpenCV` `scikit-learn`

---

### 🧴 SmartSkinAnalyzer — IoT & AI skin analysis
Embedded prototype combining IoT sensors and computer vision.

<details>
<summary><b>📐 Architecture</b></summary>

```mermaid
flowchart LR
    S1[DHT22<br/>humidity] --> AR[Arduino Uno]
    S2[MLX90614<br/>temperature] --> AR
    S3[Sharp sensor] --> AR
    AR --> PI[Raspberry Pi 4]
    CAM[Camera] --> PI
    PI --> Y[YOLO11s · ONNX<br/>acne detection]
    PI --> U[U-Net + ResNet-50<br/>wrinkle segmentation]
    PI --> O[OpenCV<br/>spots & pores]
    PI --> R[Rule-based<br/>skin-type estimation]
```

</details>

- **Acne detection:** YOLO11s trained on ACNE04, exported to **ONNX** for optimised embedded inference
- **Wrinkle segmentation:** U-Net with a ResNet-50 encoder on FFHQ-Wrinkle
- **Spots / pores:** OpenCV image processing; skin type estimated by a rule-based system on temperature and humidity

`PyTorch` `YOLO11s` `U-Net` `ONNX Runtime` `OpenCV` `Arduino` `Raspberry Pi 4`

---

### 🔎 ResearchWatch — Scientific Search Engine
Complete scientific search system on the **Elastic stack**, with an ingestion pipeline and an analytics dashboard.

- **Ingestion:** collection and indexing of arXiv articles with Python, containerised with Docker
- **Custom bilingual (EN/FR) analyzer** with synonym handling (AI, ML, NLP) and asciifolding filters
- **8 types of DSL queries** (full-text, function score, autocomplete, aggregations) and an interactive **Kibana** dashboard
- Automated **pytest** suite covering analyzers and aggregations

`Elasticsearch` `Kibana` `Python` `Docker` `arXiv API`

---

## 💼 Experience

**Web Developer Intern — Scientific research application** · *Ménara Préfa* · 2 months, 2025

- Web application for searching indexed scientific publications
- **Scopus** and **SCImago** API integration for bibliometric search
- Automated **PDF and Excel** report generation · Flask backend, scientific data processing

`Python` `Flask` `HTML/CSS` `JavaScript`

---

## 🛠️ Tech stack

| | |
|---|---|
| **Languages** | Python · Java · C · C# · JavaScript · SQL (T-SQL, PL/SQL) |
| **ML & Deep Learning** | PyTorch · TensorFlow/Keras · HuggingFace Transformers · scikit-learn · XGBoost · Federated Learning · Reinforcement Learning |
| **Audio & Vision** | Wav2Vec2 · Librosa · OpenCV · CNN · LSTM · EfficientNet |
| **Data & Search** | Elasticsearch · Kibana · Apache Kafka · Neo4j · SQL · NoSQL |
| **Web & Desktop** | Flask · Gradio · Java EE · .NET (ADO.NET) · HTML · CSS |
| **IoT & Edge** | Raspberry Pi · Arduino |
| **Tools** | Git/GitHub · Docker · Google Colab · TensorBoard |

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch"/>
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow"/>
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn"/>
  <img src="https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV"/>
  <img src="https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white" alt="Kafka"/>
  <img src="https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white" alt="Elasticsearch"/>
  <img src="https://img.shields.io/badge/Neo4j-4581C3?style=for-the-badge&logo=neo4j&logoColor=white" alt="Neo4j"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask"/>
  <img src="https://img.shields.io/badge/Raspberry_Pi-A22846?style=for-the-badge&logo=raspberrypi&logoColor=white" alt="Raspberry Pi"/>
</p>

---

## 🎓 Education

| Degree | Institution | Period |
|---|---|---|
| **MSc — Artificial Intelligence & Digital Computing (AIDC)** | FST Béni Mellal | Since Sept. 2025 |
| **BSc — Science & Technology (Computer Science)** | FST Béni Mellal | 2024 – 2025 |
| **DEUST — Mathematics, Computer Science, Physics** | FST Béni Mellal | 2022 – 2024 |

**Languages:** Arabic (native) · French (good) · English (intermediate, technical)

**Interests:** Artificial Intelligence · Generative AI (LLMs, RAG) · Data Science · Web Development

---

<div align="center">

**Open to a PFE internship in AI & Data — 2027**

📧 [elazaarhamza5@gmail.com](mailto:elazaarhamza5@gmail.com) · 💼 [LinkedIn](https://linkedin.com/in/hamzaelazaar)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:E07B39,100:1A1A1A&height=90&section=footer" alt="footer" />

</div>
