# 🏨 Next‑Gen Hotel Recommendation System

> **A full‑stack hotel recommendation platform powered by LangGraph, Gemini, DistilBERT, and ChromaDB — delivering intelligent hotel insights, sentiment analysis, and interactive dashboards.**

---

## 📌 Project Overview

Designed and implemented a next‑generation hotel recommendation system combining **LLM‑powered RAG workflows**, **fine‑tuned sentiment analysis models**, and **feedback pipelines**. The platform processes customer reviews, recommends hotels based on natural‑language queries, and integrates feedback loops with automated sentiment classification and email notifications. It features a responsive dark/light mode UI, Tableau dashboard embedding, and Dockerized deployment for portability.  

---

## 🎥 Live Demo

### 📹 Project Walkthrough Video
![Pipeline Demo](assets/Hotel_demo.gif)

👉 [Watch Full Video](https://drive.google.com/uc?export=download&id=YOUR_FILE_ID)

---

### 🖼️ Tableau Dashboard Preview
![Tableau Dashboard](assets/Dashboard.png)

---

### 🌐 Tableau Public Link
View Interactive Dashboard: [Tableau/Yaggesh-Sawant](https://public.tableau.com/views/Final_Fmcg_dashboard/FMCGDashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## 🚀 Key Features

* **🔍 Sentiment Analysis:** Classify hotel reviews as good/bad with confidence scores and probability distributions.  
* **💬 Hotel Recommendation Chatbot:** Query hotels, destinations, or amenities; responses generated via **Gemini + ChromaDB** retrieval.  
* **📊 Feedback Form:** Collects user feedback, analyses sentiment, and sends:  
  - Thank‑you email to customers  
  - Alert email to hotels (negative feedback only)  
  - Logs feedback into Google Sheets  
* **🌗 Dark/Light Mode:** User preference stored locally.  
* **📈 Tableau Integration:** Embed live dashboards directly in the app.  
* **🐳 Docker Ready:** Run anywhere with a single command.  

---

## 🛠️ Tech Stack & Architecture

| Layer | Technology | Usage / Function |
| :--- | :--- | :--- |
| **Backend** | Flask | Web framework |
| | LangGraph | Workflow orchestration (RAG, feedback) |
| | LangChain + Gemini | LLM chatbot |
| | ChromaDB | Vector database for semantic retrieval |
| | Sentence‑Transformers | Embedding model (MiniLM‑L6‑v2) |
| | DistilBERT | Fine‑tuned sentiment classifier |
| | TensorFlow / Keras | Model runtime |
| | Gmail SMTP | Email notifications |
| | Google Sheets API | Feedback logging |
| **Frontend** | HTML, CSS, JavaScript | Responsive UI |
| | Marked.js | Markdown rendering |
| | Font Awesome | Icons |
| | Inter Font | Custom typography |

---

## ⚙️ System Workflow

```text
[ User Query / Feedback ] ──► [ Flask + LangGraph ]
        │
        ├──► [ ChromaDB Retrieval ] ──► [ Gemini LLM Response ]
        │
        ├──► [ DistilBERT Sentiment Analysis ]
        │
        ├──► [ Email Notifications (Gmail SMTP) ]
        │
        └──► [ Google Sheets Logging + Tableau Dashboard ]
```
