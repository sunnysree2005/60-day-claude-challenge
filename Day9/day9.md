# Day 9: Iterative AI App Development — NutriScope v2

## 📝 Overview
In this session, I explored the power of **Iterative Development** by building an advanced single-file HTML application called **NutriScope**. Instead of asking the AI to build a massive, complex application in a single prompt, I followed a professional workflow: first creating a stable **Minimum Viable Product (MVP)**, and then progressively enhancing it with advanced data-driven features.

---

## 📸 Application Showcases

### 1. MVP Version (Prompt 1)
The MVP established the core infrastructure of the app, including basic profile inputs, a 20-food tracking database, macro/micro calculations, and a responsive dark-themed dashboard.



### 2. Enhanced Version (Prompt 2)
The enhanced version added sophisticated capabilities, including a 2-Day Meal Planner, heuristic Risk Analysis, CSV upload/export, an expanded 60-food database, and advanced dietary recommendations.


## 🔄 Comparison Notes: MVP vs. Enhanced

| Feature / Metric | MVP Version (v1) | Enhanced Version (v2) |
| :--- | :--- | :--- |
| **Food Database** | 20 Common Foods | **60 Foods** (Expanded regional variations) |
| **Nutrient Tracking** | 10 Core Metrics (Calories, Macros, basic Micros) | **Comprehensive Micro-profile** + Additional Trace Elements |
| **Data Interaction** | Manual Entry Table only | **CSV Drag & Drop Upload** + **Log Export** |
| **Data Analytics** | Single Daily Target Ring & Macros | **Nutrient Radar Chart**, **Calorie Timeline**, & Detailed Grid |
| **Planning Capabilities** | Real-time immediate tracking | **2-Day Comparative Meal Planner** |
| **Clinical Context** | Basic target percentage completion | **Heuristic Risk Analysis Engine** + Educational Disclaimers & Methodology Sources |

---

## 💡 Key Learnings

1. **The Fallacy of Single-Prompt Giants:** Attempting to generate a production-ready, feature-rich application in one prompt causes modern AI models to lose context, truncate code, or produce logical bugs. 
2. **Iterative Scaffolding Works Best:** Building a rock-solid MVP first gives the AI a concrete foundational structure. When asking for enhancements later, the model treats the existing codebase as strict context, drastically reducing generation errors.
3. **Claude Artifacts Efficiency:** Keeping the entire front-end application within a single HTML file—leveraging CDNs for libraries like `Chart.js`—makes prototyping and testing incredibly fast, locally scalable, and highly performant.
4. **Heuristics & Guardrails:** Adding features like "Risk Analysis" highlights the developer's responsibility to balance data computations with strict educational disclaimers (e.g., citing ICMR-NIN 2020 guidelines) to prevent misleading users in health tech.

---

## 📂 Source Files
* [NutriScope MVP Source Code](./nutri-scope-v1.html) *(Ensure you save your Prompt 1 file here)*
* [NutriScope Enhanced v2 Source Code](./nutri-scope-v2.html) *(The file containing your generated v2 code)*
