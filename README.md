<div align="center">

# 🤖 CodeAlpha AI Internship — Task Portfolio

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=6C63FF&center=true&vCenter=true&width=500&lines=AI+Internship+%40+CodeAlpha;3+Tasks+Completed+%E2%9C%85;Python+%7C+Deep+Learning+%7C+NLP;Built+by+Tauseef+Alam" alt="Typing SVG" />

<br/>

![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.20-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-5.x-orange?style=for-the-badge)
![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![Status](https://img.shields.io/badge/Status-3%2F4%20Tasks%20Complete-success?style=for-the-badge)

<br/>

| 👨‍💻 Developer | 🏢 Company | 📅 Batch | 🌐 Domain |
|:---:|:---:|:---:|:---:|
| **Tauseef Alam** | **CodeAlpha** | **May 2026** | **Artificial Intelligence** |

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](YOUR_LINKEDIN_URL)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](YOUR_GITHUB_URL)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:YOUR_EMAIL)

</div>

---

## 📋 Table of Contents

- [About](#-about)
- [Tasks Overview](#-tasks-overview)
- [Task 1 — Language Translation Tool](#-task-1--language-translation-tool)
- [Task 2 — FAQ Chatbot](#-task-2--faq-chatbot-nlp)
- [Task 3 — Music Generation with AI](#-task-3--music-generation-with-ai)
- [Task 4 — Object Detection & Tracking](#-task-4--object-detection--tracking)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [How to Run](#-how-to-run)
- [What I Learned](#-what-i-learned)
- [Connect](#-connect)

---

## 🎯 About

This repository contains **3 real-world AI projects** completed during my Artificial Intelligence Internship at **CodeAlpha** (May 2026 Batch).

Every project is built from scratch in Python on Google Colab — combining machine learning, NLP, deep learning, and computer vision — with interactive web interfaces. No paid APIs, no pre-built AI platforms. Just code, logic, and curiosity.

> *"Every model in here taught me something lectures couldn't."*
> — Tauseef Alam

---

## 🗂️ Tasks Overview

<div align="center">

| # | Project | Core Tech | UI | Difficulty | Status |
|:---:|:---|:---:|:---:|:---:|:---:|
| 1 | Language Translation Tool | deep_translator · langdetect | Streamlit | ⭐ | ✅ Done |
| 2 | FAQ Chatbot (NLP) | NLTK · TF-IDF · Cosine Similarity | Gradio | ⭐⭐ | ✅ Done |
| 3 | Music Generation with AI | TF 2.20 · BiLSTM · music21 | Gradio | ⭐⭐⭐ | ✅ Done |
| 4 | Object Detection & Tracking | YOLOv8 · ByteTrack · OpenCV | Gradio | ⭐⭐⭐ | ✅ Done |

</div>

---

## 🌍 Task 1 — Language Translation Tool

<img src="https://img.shields.io/badge/Framework-Streamlit-FF4B4B?style=flat-square&logo=streamlit" />
<img src="https://img.shields.io/badge/API-Google_Translate_(Free)-4285F4?style=flat-square&logo=google" />
<img src="https://img.shields.io/badge/Languages-22+-success?style=flat-square" />

### What it does
A professional web application that translates text across 22+ languages instantly. Features automatic language detection, translation history, real-time character counter, and a beautiful custom dark UI — all without a paid API key.

### Live Demo
```
Input  :  "I am learning Artificial Intelligence."
Source :  Auto Detect  →  detected as English  🇺🇸
Target :  Urdu  🇵🇰
Output :  "میں مصنوعی ذہانت سیکھ رہا ہوں۔"
```

### Features

- 🌐 **22+ languages** — English, Urdu, Arabic, Hindi, French, Spanish, German, Chinese, Japanese and more
- 🔍 **Auto language detection** — powered by `langdetect` (no manual selection needed)
- ⇄ **Swap button** — flip source ↔ target, moves translation back to input
- 📋 **Copy to clipboard** — built-in copy expander
- 🕒 **Translation history** — last 5 translations tracked in the sidebar
- 📊 **Session stats** — live counter of translations made
- ⚡ **Character counter** — colour-coded warning near the 5,000 limit
- 🎨 **Dark glass UI** — gradient header, glass-morphism cards, flag emojis

### How It Works

```
User types text
    ↓
langdetect.detect(text)
    Statistical model (Naive Bayes + n-gram frequency profiles)
    Trained on 55 languages → returns code "en", "ur", "fr" etc.
    ↓
GoogleTranslator(source="en", target="ur").translate(text)
    Free wrapper around Google Translate — no API key needed
    ↓
Streamlit session_state stores result + history
Re-renders UI with translated text
```

### Stack

| Library | Version | Purpose |
|---------|---------|---------|
| `streamlit` | latest | Web interface + session state |
| `deep_translator` | 1.11.4 | Free Google Translate wrapper |
| `langdetect` | 1.0.9 | Language detection |

### Run

```bash
pip install streamlit deep_translator langdetect
streamlit run Task1_LanguageTranslation/Task1_Translation_Streamlit_App.py
```

---

## 🤖 Task 2 — FAQ Chatbot (NLP)

<img src="https://img.shields.io/badge/Framework-Gradio-orange?style=flat-square" />
<img src="https://img.shields.io/badge/NLP-TF--IDF_+_Cosine_Similarity-blueviolet?style=flat-square" />
<img src="https://img.shields.io/badge/FAQs-25_questions-success?style=flat-square" />

### What it does
An NLP chatbot that understands the **meaning** of your question — not just exact keywords. Type "tell me about ML" and it correctly matches "What is machine learning?" because it compares semantic vectors, not strings.

### Live Demo
```
Input    :  "tell me about ML"
Matched  :  "What is machine learning?"  ← 82% confidence
Output   :  Machine Learning is a type of AI where computers learn from data...
            📌 Matched: "What is machine learning?"
            🎯 Confidence: [████████░░] 82%
            📚 Related: What is deep learning? | What is TF-IDF? | ...
```

### Features

- 📚 **25 FAQs** across 5 categories (AI Fundamentals, Python, Computer Vision, CodeAlpha, Career)
- 🧮 **TF-IDF + Cosine Similarity** — matches meaning, not just words
- 🔑 **Keyword boosting** — exact keyword matches get an extra confidence boost
- 📊 **Confidence score** — shown on every answer (percentage + bar)
- 🗂️ **Category filter** — search only within one topic
- 📚 **Related questions** — suggests 3 more questions after each answer
- 💾 **Chat export** — download conversation as `.txt`
- 🗃️ **FAQ browser tab** — explore all 25 questions in a table

### NLP Pipeline

```
Input: "What IS Machine Learning?!"
    ↓  preprocess_text()
"machine learn"
(lowercase → remove punctuation → tokenize → stopwords → lemmatize)
    ↓  TfidfVectorizer.transform()
[0.0, 0.82, 0.0, 0.45, ...]   ← numeric vector
    ↓  cosine_similarity()
[0.82, 0.03, 0.15, ...]        ← one score per FAQ
    ↓  argmax() + keyword boost
FAQ #2 wins → return answer + confidence + related questions
```

### Stack

| Library | Purpose |
|---------|---------|
| `nltk` | Tokenization, stopword removal, lemmatization |
| `scikit-learn` | TF-IDF vectorizer + cosine similarity |
| `pandas` | FAQ dataset management |
| `gradio` | Chat interface with tabs |

### Run

```bash
pip install nltk scikit-learn gradio pandas numpy
python Task2_FAQChatbot/Task2_FAQ_Chatbot_FIXED.py
```

---

## 🎵 Task 3 — Music Generation with AI

<img src="https://img.shields.io/badge/Model-Bidirectional_LSTM-FF6F00?style=flat-square&logo=tensorflow" />
<img src="https://img.shields.io/badge/Dataset-Bach_Chorales_(music21)-blueviolet?style=flat-square" />
<img src="https://img.shields.io/badge/Audio-FluidSynth-success?style=flat-square" />

### What it does
A deep learning system trained on **Johann Sebastian Bach's chorales** that generates original classical-style piano music. The model learns musical patterns from real compositions and writes new pieces it has never played before.

### Live Demo
```
Training data  :  20 Bach chorales (bundled in music21 — no download!)
Model reads    :  100 consecutive notes at a time
Model predicts :  the next note (from a vocabulary of ~54 unique items)
Repeat         :  200 times → full composition (~30 seconds)
Output         :  WAV audio file via FluidSynth piano samples
```

### Features

- 🎼 **No external data download** — uses music21's built-in Bach corpus
- 🧠 **Bidirectional LSTM** — reads sequences forward AND backward
- 🌡️ **Temperature sampling** — one slider controls creativity (0.1 = Bach, 2.0 = jazz)
- 📉 **Training loss curve** — visualised after training
- 🔊 **Audio player** — listen to generated music in the browser
- 💾 **MIDI download** — open in MuseScore, GarageBand, or VLC
- ⏱️ **BPM control** — set your own tempo (60–200 BPM)
- 🎲 **Fixed seed mode** — same music every run (great for demos)

### Architecture

```
Input: sequence of 100 integer-encoded notes
    ↓
Embedding(n_vocab=54, output_dim=64)
    ↓
Bidirectional LSTM(256, return_sequences=True)
    ↓
Dropout(0.3)
    ↓
LSTM(256, return_sequences=False)
    ↓
Dropout(0.3)
    ↓
Dense(256, relu) + BatchNormalization
    ↓
Dense(n_vocab, softmax)
    ↓
Temperature sampling → next note → slide window → repeat ×200
```

### Temperature Guide

| Temperature | Character | Best for |
|-------------|-----------|----------|
| 0.1 – 0.4 | Structured, repetitive, Bach-like | Demo recordings |
| 0.5 – 0.9 | Classical, coherent | Portfolio video |
| 1.0 | Balanced creativity | General use |
| 1.1 – 1.5 | Interesting, surprising | Exploration |
| 1.6 – 2.0 | Chaotic, avant-garde | Experimentation |

### Stack

| Library | Version | Purpose |
|---------|---------|---------|
| `music21` | 9.1.0 | Parse MIDI, extract notes, create output score |
| `tensorflow` | 2.20 | Build & train Bidirectional LSTM |
| `fluidsynth` | system | Render MIDI → WAV with real piano samples |
| `gradio` | 5.x | Web interface with audio player |

### Run

```bash
# Enable GPU first in Colab: Runtime → Change Runtime Type → T4 GPU
apt-get install -y fluidsynth fluid-soundfont-gm
pip install music21==9.1.0

# ⚠️  DO NOT reinstall tensorflow, gradio, numpy or websockets
# They are already correctly installed in Colab 2026

python Task3_MusicGeneration/Task3_Music_Generation_FINAL.py
```

> **Training time:** ~15–25 minutes on T4 GPU. Run all cells top to bottom.
> Best loss achieved: **~0.016** at epoch 79.

---

## 🎯 Task 4 — Object Detection & Tracking

<img src="https://img.shields.io/badge/Model-YOLOv8n-FF6B35?style=flat-square" />
<img src="https://img.shields.io/badge/Tracking-ByteTrack-blueviolet?style=flat-square" />
<img src="https://img.shields.io/badge/Classes-80_COCO-success?style=flat-square" />

### What it does
Real-time object detection and tracking using **YOLOv8** with **ByteTrack** algorithm. Detects 80 object classes in images and videos — assigning unique, persistent tracking IDs to each detected object across all frames.

### Live Demo
```
Input  :  traffic.mp4 (240 frames)
Output :  traffic_tracked.mp4
          → Person #1 followed across 240 frames
          → Car   #2 followed across 198 frames
          → Car   #3 appeared at frame 45
Stats  :  3 unique persons | 5 unique vehicles | 30.2 FPS avg
```

### Features

- 🎯 **80 COCO classes** — person, car, dog, laptop, phone, and 75 more
- 🔢 **ByteTrack IDs** — unique persistent tracking IDs across all frames
- 📹 **Image + video modes** — upload photo for instant detection or video for tracking
- 🎚️ **Confidence threshold** — slider from 0.1 to 0.9
- 🏷️ **Class filter** — detect only selected object types
- 📊 **Stats overlay** — live FPS + object count per class on each frame
- 💾 **Annotated video download** — save processed MP4
- ⏳ **Progress bar** — shows frame-by-frame processing progress

### Pipeline

```
Video input (mp4, avi)
    ↓  cap.read() per frame
    ↓
YOLOv8 detection
    model.track(frame, conf=0.4, persist=True, tracker="bytetrack.yaml")
    Returns per object: [x1,y1,x2,y2] · class_id · confidence · track_id
    ↓
ByteTrack algorithm
    Predicts next position using velocity → matches detections to tracks
    Same object keeps same ID across all frames
    ↓
OpenCV drawing
    cv2.rectangle()  → bounding box
    cv2.putText()    → "person #3  87%"
    Stats overlay    → FPS + object counts
    ↓
VideoWriter → output.mp4 → Gradio display + download
```

### Stack

| Library | Purpose |
|---------|---------|
| `ultralytics` | YOLOv8 detection + ByteTrack tracking |
| `opencv-python-headless` | Frame-by-frame video I/O + annotation |
| `torch` | Deep learning backend (GPU acceleration) |
| `gradio` | Web interface with progress tracking |

### Run

```bash
# Enable GPU: Runtime → Change Runtime Type → T4 GPU
pip install ultralytics gradio opencv-python-headless
python Task4_ObjectDetection/Task4_Object_Detection_Tracking.py
```

---

## 🛠️ Tech Stack

<div align="center">

```
Language      Python 3.12
Platform      Google Colab (T4 GPU)

Task 1        deep_translator · langdetect · streamlit
Task 2        nltk · scikit-learn · pandas · numpy · gradio
Task 3        tensorflow 2.20 · music21 · fluidsynth · gradio
Task 4        ultralytics (YOLOv8) · opencv · torch · gradio
```

</div>

---

## 📁 Project Structure

```
codealpha_tasks/
│
├── README.md                                    ← You are here
│
├── Task1_LanguageTranslation/
│   ├── Task1_Translation_Streamlit_App.py       ← Streamlit app
│   └── Task1_Colab_Runner.py                    ← How to run in Colab
│
├── Task2_FAQChatbot/
│   └── Task2_FAQ_Chatbot_FIXED.py               ← Gradio chatbot
│
├── Task3_MusicGeneration/
│   └── Task3_Music_Generation_FINAL.py          ← TF 2.20 LSTM app
│
└── Task4_ObjectDetection/
    └── Task4_Object_Detection_Tracking.py       ← YOLOv8 app
```

---

## 🚀 How to Run

### Google Colab (Recommended for all tasks)

```
Step 1  → Open colab.google.com → New Notebook
Step 2  → For Tasks 3 & 4: Runtime → Change Runtime Type → T4 GPU
Step 3  → Paste the task file into code cells
Step 4  → Run cells top to bottom (Shift + Enter)
Step 5  → Copy the public URL from the output
```

### Task-specific install commands

```bash
# Task 1 — Language Translation
pip install streamlit deep_translator langdetect

# Task 2 — FAQ Chatbot
pip install nltk scikit-learn gradio pandas numpy

# Task 3 — Music Generation  (GPU recommended)
apt-get install -y fluidsynth fluid-soundfont-gm
pip install music21==9.1.0
# tensorflow + gradio already in Colab — DO NOT reinstall

# Task 4 — Object Detection  (GPU recommended)
pip install ultralytics gradio opencv-python-headless
```

### Requirements by task

| Requirement | Task 1 | Task 2 | Task 3 | Task 4 |
|-------------|:------:|:------:|:------:|:------:|
| GPU | — | — | ✅ | ✅ |
| Internet | ✅ | — | — | — |
| RAM (min) | 2 GB | 2 GB | 4 GB | 4 GB |
| Training time | Instant | ~30 sec | ~20 min | Instant |

---

## 📖 What I Learned

### Task 1 — Language Translation
- How translation APIs abstract language complexity behind simple function calls
- Statistical language identification using character n-gram frequency models
- Building production-quality Python web apps with Streamlit
- Custom CSS-in-Python: gradients, glass morphism, responsive dark layouts
- Streamlit session state for persistent history and UI state across reruns

### Task 2 — FAQ Chatbot
- Why "tell me about ML" and "what is machine learning" should match — and how to make it happen
- TF-IDF: why rare words score higher than common ones
- Cosine similarity: measuring the angle between text vectors (meaning), not distance (exact words)
- How real-world chatbots work without GPT or any paid AI service

### Task 3 — Music Generation
- How music can be modelled as a sequence prediction problem (next-note prediction)
- Why Bidirectional LSTM outperforms standard LSTM for sequential data
- Temperature sampling: one parameter that changes an AI's entire personality
- TF 2.20 breaking changes: `.keras` format, Keras 3 API, websockets conflicts
- Never reinstall pre-installed Colab packages — it breaks the ecosystem

### Task 4 — Object Detection & Tracking
- YOLOv8 single-pass grid detection vs. traditional sliding window methods
- Why `persist=True` is critical for stable cross-frame track IDs
- ByteTrack: motion prediction + Hungarian algorithm for detection-to-track matching
- OpenCV video pipeline: `VideoCapture` → process → `VideoWriter`
- GPU memory management: `.cpu().numpy()` for extracting tensors

---

## 🏆 Internship Benefits

Upon successful submission:

- ✅ **Completion Certificate** — QR verified
- ✅ **Unique ID Certificate**
- ✅ **Letter of Recommendation** — based on performance
- ✅ **Job Placement Support**
- ✅ **Resume Building Help**
- 🎁 **Top 10 candidates** receive exclusive goodies from CodeAlpha

---

## 👨‍💻 Connect

<div align="center">

**Tauseef Alam**

*AI Intern @ CodeAlpha | May 2026 Batch*

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Tauseef_Alam-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](YOUR_LINKEDIN_URL)
[![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?style=for-the-badge&logo=github&logoColor=white)](YOUR_GITHUB_URL)
[![Email](https://img.shields.io/badge/Email-Get_in_touch-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:YOUR_EMAIL)

<br/>

---

<sub>
Built with ❤️ during the <strong>CodeAlpha AI Internship</strong> — May 2026<br/>
Python · TensorFlow · YOLOv8 · Streamlit · Gradio · NLTK · music21 · OpenCV
</sub>

</div>
