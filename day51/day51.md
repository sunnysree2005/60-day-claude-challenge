An AI-powered project for the AB Talks Claude AI Challenge requires a polished and professional `README.md` file. Given the context of a 10-day capstone following a strict Product Discovery & Sprint Planning framework, this `README.md` acts as the primary documentation portal for the repository.

---

# 🚀 AI-Powered Adaptive Interview Defense Simulator

> A dynamic, intelligent simulation tool built during the **AB Talks 60-Day Claude AI Challenge** (Capstone v1.0). Designed to simulate high-pressure technical interviews, viva voce sessions, and project defenses by dynamically tailoring questions based on your technical stack, resume, and real-time responses.

---

## 📌 Table of Contents

* [Overview](https://www.google.com/search?q=%23overview)
* [Problem Statement](https://www.google.com/search?q=%23problem-statement)
* [Target Users](https://www.google.com/search?q=%23target-users)
* [Core Features (v1.0)](https://www.google.com/search?q=%23core-features-v10)
* [Tech Stack](https://www.google.com/search?q=%23tech-stack)
* [10-Day Capstone Roadmap](https://www.google.com/search?q=%2310-day-capstone-roadmap)
* [Project Architecture](https://www.google.com/search?q=%23project-architecture)
* [Getting Started](https://www.google.com/search?q=%23getting-started)
* [Future Scope](https://www.google.com/search?q=%23future-scope)
* [Author](https://www.google.com/search?q=%23author)

---

## 🌟 Overview

Engineering students, developers, and job seekers often struggle with unexpected viva questions, technical grillings, and articulation under pressure. **Adaptive Interview Defense Simulator** bridges this gap by acting as an intelligent, conversational practice partner. It analyzes uploaded project summaries or tech stacks, generates targeted cross-examinations, evaluates user responses in real-time, and provides actionable feedback to sharpen interview performance.

---

## 🎯 Problem Statement

Traditional mock interviews are either static (pre-written Q&A flashcards) or expensive (requiring human mentors). They lack adaptability, fail to simulate the unpredictable line of questioning typical of technical board vivas or recruiter cross-examinations, and do not offer objective, immediate performance breakdowns.

---

## 👥 Target Users

* **Undergraduate Engineering Students:** Preparing for thesis defenses, lab vivas, and technical job interviews.
* **Junior Developers & Job Seekers:** Looking to build confidence in technical screening and behavioral deep-dives.
* **Self-Taught Programmers:** Needing a sandbox environment to test their ability to explain and defend their code architecture.

---

## ✨ Core Features (v1.0)

1. **Dynamic Scenario Configurator:** Select interview modes (e.g., Technical Board Viva, Software Engineering Job Screen, Machine Learning Project Defense).
2. **Context-Aware Questioning Engine:** Generates intelligent follow-up questions tailored directly to the user's previous responses rather than static scripts.
3. **Real-Time Defense Evaluation:** Instant scoring rubric tracking technical accuracy, clarity, and composure.
4. **Comprehensive Post-Session Debrief:** Summary dashboard outlining strong points, missed edge cases, and suggested areas for improvement.
5. **Clean & Responsive UI:** Minimalist, distraction-free interface optimized for high-focus practice sessions.

---

## 🛠️ Tech Stack

* **Frontend:** Next.js / React (TypeScript, Tailwind CSS)
* **Backend / API Integration:** Node.js / Python FastAPI, LLM API Integration (Claude / Gemini APIs)
* **Deployment:** Vercel / Render
* **Version Control:** Git & GitHub

---

## 📅 10-Day Capstone Roadmap

This project was built from scratch over a rigorous 10-day development sprint:

* **Day 1:** Product Discovery, PRD, and Sprint Planning
* **Day 2:** Architecture Setup & Repository Initialization
* **Day 3:** Core UI Layout & Navigation Design
* **Day 4:** API Integration & Prompt Engineering Layer
* **Day 5:** Session State Management & Dynamic Questioning Flow
* **Day 6:** Evaluation Dashboard & Scoring Logic
* **Day 7:** End-to-End Integration & Bug Fixing
* **Day 8:** User Testing, Polish, and UI Refinements
* **Day 9:** Production Deployment & Environment Configuration
* **Day 10:** Final Documentation, Pitch Deck, and Submission Showcase

---

## 🏗️ Project Architecture

```text
├── src/
│   ├── components/       # Reusable UI components (Chatbox, Dashboard, Cards)
│   ├── app / pages/      # Route pages (Home, Session, Debrief)
│   ├── services/         # API integration and LLM prompt handlers
│   └── utils/            # Helper functions and scoring logic
├── public/               # Static assets and icons
├── README.md             # Project documentation
└── package.json          # Dependencies and scripts

```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed on your local machine:

* Node.js (v18+)
* Git

### Installation & Local Setup

1. **Clone the repository:**
```bash
git clone https://github.com/your-username/adaptive-interview-defense-simulator.git
cd adaptive-interview-defense-simulator

```


2. **Install dependencies:**
```bash
npm install

```


3. **Configure environment variables:**
Create a `.env.local` file in the root directory and add your required API keys:
```env
NEXT_PUBLIC_API_URL=your_api_url_here
LLM_API_KEY=your_llm_api_key_here

```


4. **Run the development server:**
```bash
npm run dev

```


5. **Open your browser:**
Navigate to `http://localhost:3000` to view the application.

---

## 🔮 Future Scope

* **Voice-to-Voice Integration:** Real-time speech recognition and text-to-speech simulation for an authentic verbal interview experience.
* **Peer Challenge Mode:** Share custom interview prompts and challenge friends or colleagues.
* **Resume Parsing Engine:** Automatic extraction of skills and projects to instantly generate personalized viva scenarios.

---

## 👩‍💻 Author

**Sreeja Ghosh**

* Undergraduate Engineering Student (ETE), RUET
* Participant in the AB Talks 60-Day Claude AI Challenge
