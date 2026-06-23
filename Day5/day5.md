# Day 5: Context Engineering vs. Prompt Engineering

## 📝 Task Overview
In this task, I explored the concept of **Context Engineering** by testing two different prompts in Claude. The goal was to observe how providing structural and personal context alters the utility, precision, and personalization of an AI-generated 30-day learning roadmap.

---

## 🤖 Prompt A: Without Context (Generic)

### Prompt Submitted:
> Create a 30-day learning roadmap. Include: Weekly milestones, Daily tasks, Resources, Projects, Final outcome. Make it practical and beginner-friendly.

### Claude's Output (Summary):
* **Topic:** General Python Programming.
* **Focus:** Basic syntax, simple loops, and generic beginner data structures.
* **Projects:** A basic calculator and a text-based guessing game.
* **Drawback:** Highly generic. It assumes no prior programming knowledge, making it repetitive for someone who already knows C++ or MATLAB.



## 🎯 Prompt B: With Context (Tailored)

### Prompt Submitted:
> Create a 30-day learning roadmap.
> 
> **Context:**
> - Current Situation: 3rd-semester ETE (Electronics and Telecommunication Engineering) Student at RUET
> - Current Skills: C++, MATLAB, Fundamentals of Circuits & Signal Systems
> - Goal: Learn Machine Learning foundations and transition to Python
> - Available Time: 2 Hours per Day
> - Experience Level: Beginner in ML / Intermediate in Programming
> - Preferred Learning Style: Hands-on Projects & Code-along Videos
> 
> Include: Weekly milestones, Daily tasks, Resources, Projects, Final outcome. Make it practical and beginner-friendly.

### Claude's Output (Summary):
* **Topic:** Python and Machine Learning Foundations for ETE Engineers.
* **Focus:** Skipping basic loops to focus on syntax mapping (C++ to Python) and migrating matrix manipulation from MATLAB to NumPy/Pandas.
* **Projects:** Preprocessing simulated signal data and building a **Telecommunication/Signal Quality Predictor** using Scikit-Learn.
* **Advantage:** Highly efficient, time-optimized (2 hours/day), and directly aligns with engineering coursework.



## 📊 Comparison & Observations

### 1. Which roadmap feels more personalized?
**Prompt B** feels vastly more personalized. Instead of teaching me what an `if-else` statement is (which I already know from C++), it specifically guided me on how Python manages dynamic typing compared to C++, and how to replicate MATLAB matrix calculations using NumPy.

### 2. Which roadmap would you actually follow?
I would definitely follow **Prompt B**. Prompt A's projects (like building a calculator) offer zero value to a university engineering student. Prompt B's capstone project—predicting signal paths using SNR (Signal-to-Noise Ratio)—directly connects Machine Learning with my academic major, keeping me highly motivated.

### 3. What role did context play in improving the result?
Context acted as an **attention filter** for the LLM, optimizing its finite "attention budget":
* **Efficiency:** It pruned away unnecessary topics (basic logic) because it knew my current skill level.
* **Relevance:** It bridged my existing domain knowledge (Signals/MATLAB) with my target goal (ML), creating a custom learning path.
* **Feasibility:** It constrained the daily scope to fit my 2-hour daily availability without causing cognitive overload.

---

## 💡 Key Learnings on Context Engineering
1. **Context is a Finite Resource:** Giving the AI an explicit "Attention Budget" by defining parameters ensures high-signal outputs and avoids "Context Rot."
2. **Beyond Prompt Engineering:** It’s no longer just about using the right words; it's about engineering the complete environment (state, background, and constraints) to maximize the AI’s reasoning accuracy.
3. **Just-in-Time Principle:** Designing prompts with structured profiles helps the agent generate highly steerable, production-grade results instead of generic templates.
