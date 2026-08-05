# ⚡ NormIQ — Interactive DBMS Normalization Analyzer

> **Course**: DBMS Innovative Assignment (Course Code: `2CS505CC23`)  
> **Institution**: Charotar University of Science & Technology (CHARUSAT)

---

## 📌 Overview

**NormIQ** is a web-based, interactive Database Normalization & Analysis Tool designed to help students, database designers, and software engineers understand and execute database relational normalization step-by-step. 

From computing attribute closures and finding candidate keys to generating minimal canonical covers and testing for **Lossless Join** and **Dependency Preservation**, NormIQ automates the complex set-theoretic algorithms behind DBMS normalization up to **BCNF (Boyce-Codd Normal Form)**.

---

## ✨ Features

- 🔑 **Attribute Closure & Candidate Key Detection**: Automatically computes all attribute closures ($X^+$) and identifies minimal candidate keys, prime attributes, and non-prime attributes.
- ⚡ **Canonical Cover (Minimal Cover)**: Computes the minimal equivalent set of Functional Dependencies (FDs) through three algorithm stages:
  1. Decomposition of RHS attributes into singletons.
  2. Removal of extraneous LHS attributes.
  3. Elimination of redundant functional dependencies.
- 📊 **Step-by-Step Normal Form Verification**:
  - **1NF**: Atomicity check.
  - **2NF**: Detects partial dependencies (non-prime attributes depending on candidate key subsets) and decomposes relations into 2NF.
  - **3NF**: Detects transitive dependencies and performs 3NF synthesis.
  - **BCNF**: Identifies violations where determinants are not superkeys and performs BCNF decomposition.
- 🧪 **Advanced Properties Testing**:
  - **Lossless Join Test**: Uses the **Chase Algorithm** with matrix visualization ($a_j$ and $b_{i,j}$ symbols).
  - **FD Preservation Test**: Verifies if the original set of functional dependencies can be satisfied across all decomposed relations.
- 🌿 **Visual Decomposition Tree & Guided Slides UI**: Interactive step-by-step wizard UI featuring glassmorphic design, smooth animations, progress tracking, and sidebar navigation.

---

## 📁 Repository Structure

```
DBMS/
└── normalization_tool/
    └── normalization_tool/
        ├── index.html                  # Main application UI & layout
        ├── style.css                   # Custom glassmorphism styling & animations
        ├── engine.js                   # Core set-theory & normalization algorithms
        ├── slides.js                   # UI orchestration & slide renderer logic
        └── DB_Normalization_Report.docx # Detailed project report document
```

### File Breakdown

| File | Role & Description |
| :--- | :--- |
| **`index.html`** | Structure for Landing Page, Top Navigation, Interactive Step Slides, and Footer. |
| **`style.css`** | Futuristic dark UI styled with Google Fonts (*Outfit*, *JetBrains Mono*), CSS Grid, and responsive flex containers. |
| **`engine.js`** | Core engine containing closure math, power set generator, candidate key solver, canonical cover solver, normal form checkers, BCNF/3NF/2NF decomposers, Chase Matrix algorithm, and FD preservation solver. |
| **`slides.js`** | Controls slide transitions, sidebar updates, user input handlers, and step rendering. |
| **`DB_Normalization_Report.docx`** | Comprehensive academic report accompanying the software tool. |

---

## 🛠️ Tech Stack

- **Frontend Core**: HTML5, Vanilla JavaScript (ES6+)
- **Styling**: Custom CSS3 (Glassmorphism, CSS Variables, Flexbox/Grid Layout)
- **Typography**: Google Fonts (*Outfit* for UI elements, *JetBrains Mono* for code/sets)
- **Dependencies**: None! Pure native web technology (Zero external npm libraries required).

---

## 🚀 Getting Started

Since NormIQ is built with pure web technologies, no installation or compilation step is required.

### Quick Run
1. Clone or download the repository.
2. Navigate to `normalization_tool/normalization_tool/`.
3. Open `index.html` directly in any standard web browser (Google Chrome, Mozilla Firefox, Microsoft Edge, Brave, Safari).
4. *(Optional)* Use VS Code **Live Server** extension for real-time development reloading.

---

## 📖 How to Use NormIQ

1. **Enter Relation Name & Attributes**:
   - Provide relation name (e.g., `STUDENT` or `R`).
   - Input attributes separated by commas (e.g., `A, B, C, D, E`).
2. **Define Functional Dependencies**:
   - Input FDs in standard format `LHS -> RHS` (e.g., `A -> B`, `B -> C`, `AC -> D`).
3. **Run Analyzer**:
   - Click **Start Normalization** to launch the step-by-step simulation.
4. **Navigate Steps**:
   - **Step 1-2**: Input Summary & Schema Overview.
   - **Step 3**: Attribute Closures.
   - **Step 4**: Candidate Keys & Prime/Non-Prime Attribute Breakdown.
   - **Step 5**: Canonical Cover Computation with intermediate reduction steps.
   - **Step 6-9**: 1NF, 2NF, 3NF, and BCNF evaluation and relational decomposition.

---

## 👥 Authors & Credits

### **Project Team**
- **Prince Dholakiya** (`24BCE387`)
- **Rushil Shah** (`24BCE378`)

### **Faculty Guide**
- **Prof. Monika Shah** (Faculty Guide)

**Department of Computer Science Engineering**  
*Nirma University*  
Course Code: **2CS505CC23** — Database Management Systems

---

## 📜 License

This project is created for academic and educational purposes under the DBMS Innovative Assignment curriculum at Nirma University.
