# 🔍 JobScoutAI: Full-Stack Job Market Intelligence Platform

[![React](https://img.shields.io/badge/React-18.0%2B-61DAFB.svg)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-5.0%2B-646CFF.svg)](https://vitejs.dev/)
[![Flask](https://img.shields.io/badge/Flask-3.0%2B-000000.svg)](https://flask.palletsprojects.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.0%2B-47A248.svg)](https://www.mongodb.com/)
[![Selenium](https://img.shields.io/badge/Selenium-4.0%2B-43B02A.svg)](https://www.selenium.dev/)
[![Google Gemini AI](https://img.shields.io/badge/Gemini_AI-API-4285F4.svg)](https://ai.google.dev/)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.0%2B-38BDF8.svg)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An enterprise-grade, full-stack job market intelligence platform that automates real-time employment data extraction, aggregates market analytics across 18 key dimensions, and leverages **Google Gemini AI** for natural-language candidate career query resolution.

* **Course Project:** CS699: Software Systems Lab
* **Guide:** **Prof. Om Damani** (Department of Computer Science & Engineering, IIT Bombay)
* **Author:** **Atharv Vijay Naik** ([@atharv3903](https://github.com/atharv3903))

---

## 🌟 Executive Summary & Core Achievements

- 🕷️ **Automated Selenium & MongoDB ETL Pipeline:** Developed an automated data extraction and normalization engine using **Selenium** and **MongoDB** to scrape, parse, clean, and structure LinkedIn job postings across **10 metadata dimensions** (Role, Company, Location, Experience level, Tech stack, Work mode, Salary, Posting date, Applicant count, Job description). Multi-city duplicate listings are automatically reconciled into normalized `Jobs` and `Company` collections.
- 🚀 **Flask REST API & Analytics Engine (18 Market Metrics):** Engineered a high-performance Flask REST API exposing **4 core API modules** (`/jobs`, `/analytics`, `/companies`, `/ai-assistant`) backed by a custom MongoDB aggregation pipeline computing **18 real-time market insights** (Geographic salary heatmaps, Seniority vs. Tech-stack distribution matrices, Remote/Hybrid flexibility scores, Skill demand trends).
- 🤖 **Gemini AI Integration & Interactive Dashboard:** Integrated **Google Gemini AI API** for intelligent, context-aware resume & career advice queries. Built an ultra-responsive visual dashboard using **React, Vite, Chart.js, and TailwindCSS** for live analytics exploration.

---

## 📐 System Architecture

```
+-----------------------------------------------------------------------------------+
|                           AUTOMATED ETL SCRAPER MODULE                            |
|                          (Selenium + Python + Chromium)                           |
|   • Extractor: Scrapes job postings across 10 metadata dimensions                 |
|   • Normalizer: Deduplicates multi-city postings into Jobs & Company schemas       |
+-----------------------------------------+-----------------------------------------+
                                          |
                                          v
+-----------------------------------------------------------------------------------+
|                             MONGODB DOCUMENT DATABASE                             |
|    • Collections: `Jobs`, `Companies`, `AnalyticsCache`, `UserSessions`           |
|    • Indices: Compound index on (company_name, role_title, location)              |
+-----------------------------------------+-----------------------------------------+
                                          |
                                          v
+-----------------------------------------------------------------------------------+
|                        FLASK REST API & ANALYTICS ENGINE                          |
|                       (Flask + PyMongo + Gemini AI SDK)                           |
|   • Module 1: Job Search & Filtering Engine                                       |
|   • Module 2: Market Analytics (18 Real-time Metrics & Aggregations)             |
|   • Module 3: Enterprise Company Profile Generator                                |
|   • Module 4: Gemini AI Natural-Language Query Resolver                           |
+-----------------------------------------+-----------------------------------------+
                                          |
                                          v
+-----------------------------------------------------------------------------------+
|                     INTERACTIVE REACT & VITE DASHBOARD                            |
|                     (React 18 + Chart.js + TailwindCSS)                           |
|   • Live Salary & Skill Heatmaps, Seniority Breakdown Matrices                    |
|   • AI Career Assistant Chat Interface with Contextual Query Dispatch             |
+-----------------------------------------------------------------------------------+
```

---

## 📊 Analytics Engine Features (18 Real-Time Insights)

The backend analytics engine computes 18 key market insights powered by MongoDB aggregation pipelines:

1. **Salary Distribution by Role & Experience**
2. **Geographic Demand Heatmaps**
3. **Remote / Hybrid Flexibility Index**
4. **Top 20 In-Demand Tech Stacks**
5. **Seniority Level Distribution Matrix**
6. **Company Hiring Velocity Tracker**
7. **Role Growth Month-over-Month**
8. **Applicant-to-Job Ratio Ratings**
9. **Required Experience vs. Compensation Curves**
10. **Skills Co-occurrence Matrix (e.g., Python + AWS + Docker)**
11. **Tier-1 vs Tier-2 City Hiring Ratios**
12. **Industry Domain Categorization**
13. **Education Level Requirements**
14. **Contract vs Full-Time Split**
15. **Per-Company Employee Growth Proxy**
16. **Notice Period Expectations**
17. **Skill Premium Value Index**
18. **Market Demand Score**

---

## 🛠️ Repository Layout

```
JobScoutAI/
├── backend/                  # Flask REST API, Gemini AI integration, MongoDB pipelines
│   ├── app.py                # Core Flask entrypoint
│   ├── routes/               # API Endpoint routes (/jobs, /analytics, /ai)
│   ├── pipeline/             # MongoDB aggregation pipelines
│   └── utils/                # Helper utilities & database connection wrappers
├── frontend/                 # React 18 + Vite + TailwindCSS Frontend Application
│   ├── src/                  # React components, pages, charts
│   ├── package.json
│   ├── vite.config.js
│   └── tailwind.config.js
└── scraper/                  # Automated Selenium ETL Pipeline
    ├── main.py               # Scraper orchestrator
    ├── scrapper.py           # Selenium WebDriver extractor
    └── Dockerfile            # Containerized Chrome/Selenium build
```

---

## 🚀 Getting Started

### Prerequisites
* **Python 3.10+**
* **Node.js 18+** & **npm**
* **MongoDB Server 6.0+**
* **Google Gemini AI API Key**

### 1. Backend Setup
```bash
cd backend
pip install -r requirements.txt
export GEMINI_API_KEY="your_api_key_here"
export MONGO_URI="mongodb://localhost:27017/jobscoutai"
python app.py
```

### 2. Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

### 3. Run Automated Scraper
```bash
cd scraper
python main.py --keyword "Software Engineer" --location "India"
```

---

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author
* **Atharv Vijay Naik**
* **M.Tech Computer Science & Engineering, IIT Bombay**
* **GitHub:** [@atharv3903](https://github.com/atharv3903)
