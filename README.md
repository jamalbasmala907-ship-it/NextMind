# Fuel&Go — Interactive Product Management Presentation

![Version](https://img.shields.io/badge/Version-v1.0.0_Initial-00f2fe)
![Team](https://img.shields.io/badge/Team-NextMind-00ff87)
![Status](https://img.shields.io/badge/Status-Approved%20%2F%20In%20Development-blue)
![Evaluator](https://img.shields.io/badge/Evaluator-rmisegal%40gmail.com-purple)

**Fuel&Go** is a unified mobile-first mobility energy management platform designed to streamline fossil fuel pump and EV charging point discovery, real-time availability tracking, digital activation, and seamless payment.

Developed by team **NextMind**, this repository houses the interactive HTML presentation system showcasing the product vision, market strategy, UX architecture, dynamic financial cost engine, and visual simulation.

---

## 📁 Repository Structure & Strict Workflow Rules

To ensure strict version control, local progress preservation, and clear progress for academic evaluation, this project adheres to the following structure:

```
NextMind/
├── current_version.html     # Active working version of the presentation (always up to date)
├── index.html               # Direct entry point (redirects to current_version.html)
├── PRD.md                   # Complete Product Requirement Document
├── README.md                # Project architecture, instructions, and documentation
├── Sub_NextMind/            # Internal snapshot folder for historical milestones
│   └── v1_initial.html      # Milestone 1: 10-slide core presentation + simulator
└── prompts/                 # Prompt logs and iterative refinement documentation
    └── prompt_log.md        # Complete record of engineering prompts and architecture decisions
```

### Versioning Rules
1. **Active Presentation:** `current_version.html` at the project root is always the primary, functional version to open.
2. **Snapshot Copies in `Sub_NextMind`:** Every major release or milestone is archived inside `Sub_NextMind/` (e.g., `v1_initial.html`, `v2_calculator.html`, `v3_3d_final.html`).
3. **Frequent Git Sync:** Changes are committed iteratively to GitHub with descriptive messages for full transparent version tracking.

---

## 🖥️ Presentation Slide Deck Overview (10 Slides)

| Slide # | Slide Title | Core Content & Interactive Features |
| :--- | :--- | :--- |
| **Slide 01** | Introduction | Title, Team **NextMind**, product vision, metadata & evaluator access. |
| **Slide 02** | The Problem | Driver pain points: tool fragmentation, EV queue uncertainty, payment friction. |
| **Slide 03** | Target Users & Needs | Personas: ICE Commuter, EV Owner, and Mixed Fleet Operator. |
| **Slide 04** | Solution & Value Prop | Fuel&Go unified concept, 4 core value pillars, before vs. after. |
| **Slide 05** | Core MVP Capabilities | Scope matrix: In-Scope MVP capabilities vs. Future Production Roadmap. |
| **Slide 06** | End-to-End User Journey | 4-Stage visual workflow: Discover $\rightarrow$ Select Bay $\rightarrow$ Energize $\rightarrow$ Auto-Pay. |
| **Slide 07** | Interactive Demo Simulator | **Live JS Simulator**: Toggle between Fueling & EV Charging, bay selection, live meters, and digital receipt generation. |
| **Slide 08** | Cost Estimator & Energy Math | **Dynamic Calculator**: Real-time energy math, battery % target, ICE vs. EV savings in Israeli Shekels (₪). |
| **Slide 09** | Business & Differentiation | Competitive matrix (Waze, Pango, Cello, EV apps) & 3-tier monetization model. |
| **Slide 10** | Summary & Roadmap | Project limitations disclaimer, NextMind milestones, and Q&A sign-off. |

---

## ⚡ Key Technical Capabilities

### 1. Robust BiDi (Bidirectional) Text Support
The presentation includes specialized BiDi handling to ensure mixed Hebrew and English text, numerical calculations, and Israeli currency units (e.g. `₪7.85 / Liter`, `15 kWh`, `כולל מע"מ`) render with 100% typographic accuracy and without punctuation flip.

### 2. Dual Interactive Activation Simulator (Slide 7)
- Allows evaluators to switch between **⛽ Fueling Journey** and **⚡ EV Charging Journey**.
- Dynamically updates available stations, pump bays, and CCS fast-charging plugs.
- Simulates real-time flow meters (dispensed liters / kWh), dynamic charging rates, and automated digital tax invoice generation.

### 3. Financial & Cost Estimator Engine (Slide 8)
- Real-time slider-driven calculator comparing EV charging cost vs. ICE fuel benchmark.
- Uses exact energy formulas:
  $$\text{Energy Required (kWh)} = \text{Capacity} \times \left( \frac{\text{Target \%} - \text{Current \%}}{100} \right)$$
  $$\text{Total Cost (₪)} = \text{Energy (kWh)} \times \text{Tariff (₪/kWh)}$$
- Computes direct financial savings and savings percentage per session.

---

## 🚀 How to Run Locally

No build tools, npm packages, or server installation required.

1. Clone or download the repository to your local computer:
   ```bash
   git clone <repo-url>
   cd NextMind
   ```
2. Double-click **`current_version.html`** or **`index.html`** in any modern web browser (Google Chrome, Microsoft Edge, Safari, Mozilla Firefox).
3. **Keyboard Controls:**
   - Next slide: `Right Arrow` ($\rightarrow$), `Spacebar`, or `Page Down`
   - Previous slide: `Left Arrow` ($\leftarrow$) or `Page Up`
   - Jump to start / end: `Home` / `End`
   - Fullscreen: Click the **⛶ Fullscreen** button in the header.

---

## 👥 Team & Evaluator Access

- **Team:** NextMind
- **Course Evaluator Contact:** `rmisegal@gmail.com`
- **Milestone:** v1 Initial Prototype
