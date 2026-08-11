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

## 📁 Project Structure

```text
.
├── Frontend + Backend/
│   ├── hotel.py          # Flask application (main server)
│   ├── sentiment.py      # DistilBERT model loader
│   ├── Feedback.py       # (optional) feedback module – integrated into hotel.py
│   └── index.html        # single‑page UI
├── ML_and_DL/
│   ├── DL.ipynb          # DistilBERT fine‑tuning notebook
│   └── ML.ipynb          # classical ML experiments
├── DB_pipeline/          # data processing scripts
├── run.py                # entry point 
├── requirements.txt      # Python dependencies
├── Dockerfile            # build your own Docker image
├── docker-compose.yml    # run with Docker Compose
├── .env                  # environment variables
├── updated_processed_hotel_reviews.csv # dataset for RAG
├── chatbot_model_bundle.pkl # fine‑tuned DistilBERT model bundle
├── chromadb/             # Chroma index folder
└── credentials.json      # Google Sheets service account key
```

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
