# Day 20: Web-Based Webcam Face Puzzle Game

## 📌 Project Overview
This project focuses on building a fully client-side, interactive **Face Puzzle Game** using HTML5, Tailwind CSS, and Vanilla JavaScript. The application utilizes the browser's WebRTC API to access the user's webcam, capture a real-time snapshot, slice the captured image into structured grid matrices (3x3, 4x4, or 5x5), and challenge the user to rearrange the scrambled puzzle pieces via drag-and-drop or touch interactions.

---

## 🎮 1. Application Features & Technical Implementation
*   **Media Stream Integration:** Powered by the HTML5 MediaDevices API (`getUserMedia`) for real-time camera streaming and canvas-based image snapshot processing.
*   **Dynamic Grid Generation:** Dynamically cuts the captured image into specific responsive cells depending on user selection ($3 \times 3$, $4 \times 4$, or $5 \times 5$).
*   **Interaction Model:** Native HTML5 Drag and Drop API implemented with full pointer/touch event bindings for seamless cross-device mobile support.
*   **State Management:** Real-time state machine tracking milliseconds elapsed (Timer), valid piece transitions (Move Counter), state verification (Win Condition Check), and local storage caching for the continuous Leaderboard.

---

## 🔍 2. Gameplay & UI Architecture
1.  **Welcome & Camera Stage:** Clean, modern glassmorphic dashboard prompt requesting secure webcam access with a live canvas viewport.
2.  **Configuration Matrix:** Grid size selection options mapping dynamic piece splits:
    *   *Easy Mode ($3 \times 3$):* 9 interchangeable puzzle pieces.
    *   *Medium Mode ($4 \times 4$):* 16 interchangeable puzzle pieces.
    *   *Hard Mode ($5 \times 5$):* 25 interchangeable puzzle pieces.
3.  **The Game Board:** Randomly shuffled tiles layout keeping track of real-time positions. Includes smooth CSS transitions and validation sounds/visual flash indicators upon successful piece alignments.

---

## 📁 3. Deliverables in this Folder
*   `game.html` -> The fully functional web application containing embedded modern styling, canvas engines, responsive grid rules, and leaderboard scripts.
*   `day20.md` -> This technical log detailing project scope, mechanics, and design workflows.

---

## 💡 4. Key Learnings
1.  **Client-Side Hardware Interfacing:** Gained hands-on experience utilizing browser native video streams and using HTML5 Canvas objects to perform structural image slicing directly in the browser runtime.
2.  **Mathematical Grid Coordinate Mapping:** Deepened understanding of managing arrays, computing random shuffles with verified solve parameters, and detecting match intersections via row-column coordinates.
3.  **Modern Web UX Foundations:** Learned to design engaging web mechanics containing dynamic feedback interfaces (Timers, Sound-bytes, CSS animations) entirely within a single standalone file.

---
*Educational Submission for the #60DayClaudeChallenge.*
