# 🌿 HerbalNet.AI — Neural Vision for Indigenous Medicinal Flora

[![GitHub Pages](https://img.shields.io/badge/Live_Demo-GitHub_Pages-10b981?style=for-the-badge&logo=github)](https://herbalnet-ai.github.io/)
[![Python](https://img.shields.io/badge/Python-3.9%20%7C%203.10%20%7C%203.11-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.12+-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://tensorflow.org)
[![Accuracy](https://img.shields.io/badge/Classification_Accuracy-98.4%25-brightgreen?style=for-the-badge)](https://github.com/herbalnet-ai/herbalnet-ai.github.io)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)

> **HerbalNet AI** bridges traditional Ayurvedic and Siddha botanical knowledge with cutting-edge computer vision. Utilizing fine-tuned **MobileNetV2** with **Neural Architecture Search (NAS)** optimization and **Shannon Entropy Out-Of-Distribution (OOD)** rejection, HerbalNet provides rapid, clinical-grade identification of 10 indigenous medicinal plant species.

---

## 🌐 Live Interactive Website
Experience the live botanical scanner, interactive herbal encyclopedia, and clinical reports directly in your browser:
👉 **[https://herbalnet-ai.github.io/](https://herbalnet-ai.github.io/)**

---

## 🔬 Core Innovations

1. **MobileNetV2 + NAS Backbone**: Lightweight depthwise separable convolutions optimized for high-speed edge and browser inference (&lt; 35ms latency).
2. **Shannon Entropy OOD Filter**: Evaluates prediction entropy ($H = -\sum p_i \ln p_i$). Rejects non-plant images and wild invasive weeds exceeding $H > 2.10$.
3. **Bilingual Clinical Diagnostics**: Outputs actionable pharmacological profiles and preparations in both **English** and classical **Tamil (தமிழ்)** for traditional healers and modern researchers.
4. **Robust Model Checkpoints**: Includes trained `nas_model_robust.keras` (11 MB) and `nas_model_robust.h5` (26 MB) ready for instant deployment.

---

## 📋 The 10 Indigenous Medicinal Species

| Class ID | Common Name | Botanical Binomial | Classical Tamil Name | Primary Clinical Indication |
|:---:|:---|:---|:---|:---|
| **0** | **Brahmi** | *Bacopa monnieri* | பிராமி (நீர் பிராமி) | Enhances memory, cognitive synaptic transmission & reduces anxiety |
| **1** | **Kallurukki** | *Aerva lanata* | கல்லுருக்கி (சிறுபீளை) | Lithotriptic diuretic, dissolves calcium oxalate kidney stones |
| **2** | **Karisalankanni** | *Eclipta prostrata* | கரிசலாங்கண்ணி | Hepatoprotective, stimulates liver bile & revitalizes hair follicles |
| **3** | **Keezhanelli** | *Phyllanthus niruri* | கீழாநெல்லி | Primary Siddha treatment for acute jaundice & Hepatitis B inhibition |
| **4** | **Kuthiraiveli** | *Cleome gynandra* | குதிரைவாலி / நல்வேளை | Anti-inflammatory & analgesic for rheumatic joint swelling |
| **5** | **Mudakathan** | *Cardiospermum halicacabum* | முடக்கத்தான் | Amavata remedy for rheumatoid arthritis & synovial joint stiffness |
| **6** | **Nilavembu** | *Andrographis paniculata* | நிலவேம்பு (சிறியாநங்கை) | Antiviral antipyretic immune stimulant (King of Bitters) |
| **7** | **Pirandai** | *Cissus quadrangularis* | பிரண்டை (வஜ்ரவல்லி) | Accelerates bone fracture healing & osteoblastogenesis |
| **8** | **Sirukurinjan** | *Gymnema sylvestre* | சிறுகுறிஞ்சான் | 'Sugar Destroyer', regulates HbA1c & regenerates pancreatic beta cells |
| **9** | **Vallarai** | *Centella asiatica* | வல்லாரை | Neuroprotective brain tonic, enhances microcirculation & wound repair |

---

## 📊 Performance & Validation Metrics

| Metric | Score | Note |
|:---|:---:|:---|
| **Macro Average Accuracy** | **98.4%** | Evaluated on 10 balanced botanical classes |
| **Macro Precision** | **0.981** | Minimized false positives across similar leaf shapes |
| **Macro Recall** | **0.981** | Comprehensive recognition under varied illumination |
| **Macro F1-Score** | **0.981** | Harmonic mean across test partitions |
| **Validation Loss** | **0.082** | Converged with categorical cross-entropy |
| **Inference Latency** | **~24ms** | Benchmark on standard CPU / edge hardware |

---

## 🚀 Quickstart & Local Flask Execution

### Prerequisites
- Python 3.9, 3.10, or 3.11
- Git

### 1. Clone the Repository
```bash
git clone https://github.com/herbalnet-ai/herbalnet-ai.github.io.git
cd herbalnet-ai.github.io
```

### 2. Set Up Virtual Environment
```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Flask Web Server
```bash
python app.py
```
Open your browser and navigate to `http://localhost:5000`.

---

## 📁 Repository Structure

```
herbalnet.ai/
├── assets/                       # Botanical specimen photography & sample leaves
│   ├── plants/                   # High-resolution species photos
│   └── samples/                  # Leaf test samples for live scanner
├── templates/                    # Flask server Jinja2 HTML templates
│   ├── predict.html              # Main analysis portal
│   ├── result.html               # Diagnostic report layout
│   └── unknown.html              # OOD Rejection layout
├── static/                       # Static web assets & uploads
├── app.py                        # Flask REST API & model inference pipeline
├── augment_and_train.py          # Data augmentation & model training script
├── confusion_report.py           # Confusion matrix & performance evaluation
├── nas_model_robust.keras        # Trained Keras 3 neural network model (11 MB)
├── nas_model_robust.h5           # HDF5 model checkpoint (26 MB)
├── index.html                    # GitHub Pages interactive web application
├── style.css                     # Botanical glassmorphic design system
├── app.js                        # Client-side scanner & encyclopedia logic
├── requirements.txt              # Python runtime dependencies
├── HerbalNet_AI_Final_Report_Expanded.docx  # Comprehensive academic research report
├── HerbalNet_AI_Presentation.pptx          # Defense presentation slide deck
└── README.md                     # Project documentation & specs
```

---

## 👨‍💻 Author & Research Inquiries

**Daniel Raaj**
- **GitHub**: [@DANIELRAAJ](https://github.com/DANIELRAAJ)
- **Email**: [raajdaniel14@gmail.com](mailto:raajdaniel14@gmail.com)

---

## 📄 License
This project is open-source under the [MIT License](LICENSE).
