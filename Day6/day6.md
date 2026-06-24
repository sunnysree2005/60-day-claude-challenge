# Day 6: Resume Optimization and ATS Parsing

## 📝 Task Overview
In this session of the challenge, I focused on understanding the core mechanics of Applicant Tracking Systems (ATS) and recruiter readability. Using Claude as an ATS optimization expert, I transformed unstructured, raw educational and technical data into a highly structured, single-column, A4-ready resume format optimized for parsing algorithms.

---

## 📊 PART 1 — ATS SCORE & ANALYSIS

### Score Transformation
* **Before Optimization:** 38/100
* **After Optimization:** 84/100

### Why the Score Increased (Key Changes Made):
* **Standardized ATS Headings:** Introduced universally recognized labels like "Professional Summary," "Education," "Experience & Activities," "Projects," and "Technical Skills" to ensure zero parsing misclassifications.
* **Keyword-Dense Professional Summary:** Drafted a powerful introduction tracking industry-specific terms such as *embedded systems*, *analog circuit design*, *microcontroller programming*, and *Machine Learning*.
* **Action-Verb Bullet Points:** Replaced passive phrases with strong, achievement-oriented verbs (e.g., *Constructed*, *Designed*, *Programmed*, *Applied*).
* **Categorized Technical Skills:** Split a flat list into five distinct categories to maximize search-query matches against technical job descriptions.
* **Tech Stack Sub-labels:** Added explicit hardware and software tags directly under projects (e.g., *Arduino Nano*, *MG90S Servos*, *LPF, HPF, BPF, BRF*).
* **Parser-Safe Layout:** Adhered strictly to a single-column architecture, avoiding tables, columns, text boxes, or icons that traditionally scramble automation systems.

---

## 📸 ATS Analysis Chart
![ATS Optimization Chart](images/ats_chart.png)

---

## 📄 PART 2 — FINAL OPTIMIZED RESUME

### **Sreeja Ghosh**
Dhaka, Bangladesh | sreeja.ghosh@email.com | linkedin.com/in/sreejaghosh | github.com/sreejaghosh

#### **Professional Summary**
Detail-oriented Electronics and Telecommunication Engineering student with strong programming foundations in C++ and MATLAB, alongside hands-on experience in circuit simulations and robotics. Passionate about machine learning applications, embedded systems, and hardware-software integration.

#### **Education**
* **Rajshahi University of Engineering and Technology (RUET)**  
  Bachelor of Science in Electronics and Telecommunication Engineering (ETE)  
  *Status: 3rd Semester Undergrad | Expected Graduation: 2028*
* **Holy Cross College**  
  Higher Secondary Certificate (HSC)  
* **Viqarunnisa Noon School (VNS)**  
  Secondary School Certificate (SSC)

#### **Technical Skills**
* **Programming Languages:** C++, Python, MATLAB
* **Computer Science Fundamentals:** Data Structures and Algorithms (DSA), Matrix Operations
* **Circuit Design & Simulation:** Op-Amp Circuit Design, BJT Circuits, Active Filter Topologies
* **Embedded Systems:** Arduino IDE, Microcontroller Programming, Servo Control Sequences
* **AI/ML:** Machine Learning Foundations

#### **Experience & Activities**
* **Team ElectroKnights (Project Member) — RUET**
  * Collaborated within an engineering student team to architect and assemble complex electronic systems.
  * Accelerated system debugging workflows through structural troubleshooting of hardware-software communication barriers.

#### **Projects**
* **4-DOF Mini Robotic Arm Model** | *Tech Stack: Arduino Nano, MG90S Servos*
  * Designed and assembled a functional 4-DOF mini robotic arm model during a workshop organized by the Robotic Society of RUET.
  * Programmed customized servo control sequences via the Arduino IDE to handle precise multi-axis movements.
* **Electronic Filter Design Project** | *Tech Stack: LPF, HPF, BPF, BRF Simulation*
  * Calculated, designed, and optimized explicit parameters for multiple filter topologies (Low Pass, High Pass, Band Pass, and Band Reject).
  * Applied foundational Op-Amp and circuit theories to meet rigid hardware performance metrics.
* **Graph Theory & Network Connectivity Framework** | *Tech Stack: Logic Presentation*
  * Developed a structured technical roadmap mapping out core network connectivity, vertex paths, and communication routing topologies.

---

## 💡 Key Learnings

1. **The Myth of Visual Resumes:** Colorful multi-column templates and graphic icons look great to humans but act as massive roadblocks for standard ATS parsers. Text cleanliness always wins over aesthetic complexity.
2. **Context Matters to Parsers:** ATS Natural Language Processing (NLP) engines score resumes based on context. Writing "Member of a team" scores poorly compared to using high-impact verb strings like "Collaborated within an engineering team to architect...".
3. **Skill Hierarchy Enhances Searchability:** Simply dumping keywords into a long comma-separated line decreases the relevance profile. Categorizing skills dynamically aligns the resume with automated recruiter search parameters.
