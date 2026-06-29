# Day 15: Complex Reports & Astrological Life Analysis via AI

## 📌 Project Overview
This project demonstrates how to leverage large language models (like Claude) to handle complex, multi-step reasoning tasks. By providing structured data inputs and using advanced prompt engineering, we transform raw personal data into a comprehensive, deeply structured **Vedic Astrology & Life Analysis Report**. 

### Key Learning Objectives
1. **Structured Inputs:** Understanding how the depth and accuracy of input data directly dictate the quality of the AI's output.
2. **Multi-Step Reasoning:** Guiding AI through layered analysis (combining Parashara, Jaimini, Nakshatra, and Dasha systems).
3. **Report Generation:** Designing outputs that cleanly separate facts, interpretations, probabilities, and actionable timelines.
4. **Prompt Design:** Building structured frameworks that keep the AI aligned with complex, technical domain logic (Vedic Astrology rules).

---

## 🛠️ Step-by-Step Walkthrough

### Step 1: Data Gathering & Environment Setup
* **Tool:** Claude AI (Effort Level: **Medium** or **Low** for optimized structuring).
* **Directory Structure:** Created a `Day15` folder containing this `README.md` (or `day15.md`) and a `/screenshots` directory.

### Step 2: Prompt Execution
The system prompt (found below) was fed into Claude along with the required user variables, including birth details, current profession, and top 3 immediate life concerns.

### Step 3: Review & Capture
* Carefully audited the **Career & Wealth Analysis** section to evaluate the AI's logic on job vs. business suitability and wealth timelines.
* Reviewed the **5-Year Forecast Table** for alignment with major turning points.
* Saved the final generated report and took screenshots of the high-value sections.

---

## 📋 The Prompt Template Used

> **System Prompt fed into Claude:**
```text
You are an expert Vedic astrologer specializing in Parashara, Jaimini, Nakshatra, Vimshottari Dasha, and Transit Analysis.

Before starting, collect:
* Full Name, Gender, Date of Birth, Exact Birth Time, Birth Time Accuracy, Place of Birth, Current City, Relationship Status, Profession, Top 3 Current Concerns.

After receiving the details, generate a report covering:
1. Birth Chart Summary (Lagna, Moon/Sun Sign, Yogas, Doshas, Planet Strengths)
2. Life Pattern Analysis (Core personality, karmic loops, relationship tendencies)
3. Career & Wealth (Suitability, leadership, breakthrough age ranges - HIGHEST PRIORITY)
4. Relationships & Marriage (Timing windows, spouse traits)
5. Current Dasha Analysis (Mahadasha/Antardasha opportunities & challenges)
6. 5-Year Forecast (Tabular view for Career, Money, Relationships, Health)
7. Astrologically justified Remedies (Mantras, Donations, Gemstones)

Output Rules: Use tables where possible, explain the astrological reasoning, and focus on practical guidance rather than generic text.
