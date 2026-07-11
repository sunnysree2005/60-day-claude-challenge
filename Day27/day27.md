# Day 27: Prior Authorization Story Simulator

An interactive, append-only conversation simulator capturing the diagnostic, administrative, and appellate journey of a patient navigating utilization management roadblocks. This project uses clear, descriptive language and standard healthcare education design rules to make complex medical authorization steps easy to understand.

---

## 🏛️ Healthcare Core Concepts Covered

### 1. Direct Provider-to-Payer Workflow
*   **Workflow Path:** Provider → Direct PA Request → Payer System.
*   **Operational Detail:** The medical office uploads the prior authorization folder directly to the insurer (**StarCare Health**, used as an illustrative example) without involving an intermediate pharmacy. Once an approval reference code is issued, it is permanently saved on file to clear future treatment cycles.

### 2. Clinical Impact of Step Therapy
*   **Not Just Bureaucracy:** For aggressive conditions like Rheumatoid Arthritis, structural system delays do not just affect administrative timelines—they can cause permanent joint erosion and advanced disease progression.
*   **Statistical Data:** As highlighted in the **AMA 2023 PA Survey**, prior authorization workflows cause treatment delays in the absolute majority of cases.

### 3. Institutional Cost of Rejections
*   A prior authorization denial is a common friction point, not a permanent rejection.
*   Resolving an insurance denial takes significant administrative resources, costing physician offices an average of **2+ staff hours per case** to correct, re-verify, and appeal.

---

## 🏗️ Technical Architecture & DOM Rules

*   **Immutable Container State:** To prevent screen flickering and protect historical feed inputs, the application strictly uses `document.createElement` and `Element.appendChild` to inject new chat messages. Calling `innerHTML =` on the chat stream container is completely restricted.
*   **Visual Strategy Design:** Utilizes a custom, clean healthcare color theme. Messages on the left use a soft blue theme for the patient (**Rahul**), messages on the right use a professional slate theme for the specialist (**Priya**), and narrations are rendered as centered italic text.
*   **Interactive Branching:** Each step provides two choice points that log actions directly to the clinical feed tracker, updating the progress bar as the user advances through all 8 sequential scenes.

---

## 📂 Repository Structure
```text
your-repo/
└── Day27/
    ├── index.html               # The self-contained story simulator application
    └── day27.md                 # This core learning report file
