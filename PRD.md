# Product Requirement Document (PRD)

## Project Details
- **Project Name:** Fuel&Go
- **Team Name:** NextMind
- **Document Version:** 1.0.0
- **Status:** Approved / In Development

---

## 1. Project Overview & Background
**Fuel&Go** is a unified mobile-first service designed to streamline fuel station and EV charging point discovery, real-time availability tracking, digital activation, and seamless payment. 

This project aims to convert our original Product Management project into an **interactive HTML presentation system** that effectively demonstrates our product vision, core features, UI/UX flows, and technical integrations (including Python dynamic calculations and Three.js 3D visualizations) to both context-aware evaluators and new audiences.

---

## 2. Purpose & Goals
* **Unified Fueling & Charging:** Present an all-in-one platform integrating fossil fuel pumps and EV chargers.
* **Product Management Showcase:** Explain key product decisions, value propositions, market differentiation, and MVP prioritization.
* **Interactive Demonstration:** Engage the audience with functional, interactive flows (fueling vs. EV charging) directly within the presentation.
* **Technical Integration:** Demonstrate full-stack and web visualization skills by integrating JavaScript interactivity, PyScript/Python execution for financial calculators, and Three.js for interactive 3D rendering.

---

## 3. Problem Statement
1. **Tool Fragmentation:** Drivers currently use separate apps to locate fuel stations, search for EV chargers, check charger availability, and execute payments.
2. **Uncertainty & Wasted Time:** Lack of real-time visibility regarding pump/charger availability leads to unexpected queuing and detour trips.
3. **Disjointed User Experience:** Existing solutions lack a continuous, friction-free journey from discovery through pump activation to digital invoicing.

**Fuel&Go** solves this by unifying station discovery, pump/charger reservation, live activation, and instant payment into one smooth, continuous mobile experience.

---

## 4. Target Audience
### 4.1 Product End-Users
* **Private ICE Vehicle Drivers:** Seeking fast discovery, queue-skipping, and automatic digital receipts.
* **EV Owners:** Seeking real-time socket availability (AC/DC fast charging), plug compatibility, and transparent cost estimates.
* **Fleet / Tech-Savvy Commuters:** Users who prefer digital app-based interactions over physical terminal payments.

### 4.2 Presentation Audience
* **Course Lecturer & Academic Evaluators:** Looking for rigorous product thinking, clean execution, precise documentation, and technical compliance.
* **Peers & Classmates:** Requiring clear context, visual engagement, and easy-to-follow demonstrations.

---

## 5. Presentation Structure (10-Slide Outline)

| Slide # | Slide Title | Core Content & Key Messages |
| :--- | :--- | :--- |
| **Slide 1** | Introduction | Title, Team **NextMind**, project vision, and team intro. |
| **Slide 2** | The Problem | Driver pain points: fragmentation, EV queue uncertainty, payment friction. |
| **Slide 3** | Target Users & Needs | Personas (ICE driver, EV owner, fleet operator) & core requirements. |
| **Slide 4** | Solution & Value Prop | Fuel&Go unified concept, core value pillars, unified UI. |
| **Slide 5** | Core MVP Capabilities | Feature matrix: Discovery, Real-time status, Activation, Payment, AI assistant. |
| **Slide 6** | User Journey | Step-by-step workflow: Find $\rightarrow$ Reserve/Select $\rightarrow$ Activate $\rightarrow$ Pay. |
| **Slide 7** | Interactive Demo Flow | Live JS simulator for Fueling vs. EV Charging activation flow. |
| **Slide 8** | Cost Estimator (Python) | Live PyScript/Python powered calculator for fuel and EV charging costs. |
| **Slide 9** | Business & Differentiation| Competitive matrix, Gartner differentiation strategy, revenue models. |
| **Slide 10**| Summary & Roadmap | Demonstration limitations, future scope, Q&A, and conclusion. |

---

## 6. Design, Layout & Language Specifications
* **Language & Alignment:** Primary presentation content in English with left-to-right (LTR) layout.
* **BiDi Support:** Robust Bidirectional (BiDi) text engine to correctly render mixed Hebrew, English, numbers, and measurement units (e.g., `15 kWh`, `₪7.85 / Liter`) without punctuation flip.
* **Design System:** Modern, high-contrast dark/light theme aligned with Fuel&Go branding (Electric Cyan & Neon Green accents on Dark Slate).
* **Responsiveness:** Fluid layout supporting Desktop ($1920 \times 1080$), Laptops, and Mobile viewports.

---

## 7. JavaScript Interactivity Requirements
* **Slide Controls:** Next/Previous buttons, keyboard arrows (`Left`/`Right`/`Space`), touch swiping, and slide counter indicator (`Slide X of 10`).
* **Journey Switcher:** Interactive toggle allowing the user to select between a **Fueling Journey** and an **EV Charging Journey**.
* **Simulated Station Flow:**
  1. Station Selection (e.g., "Fuel&Go Hub - Central").
  2. Pump / Charger Slot Selection (e.g., Fast Charger #3 vs. Unleaded 95 Pump #2).
  3. Activation Confirmation step.
  4. Simulated Payment & Digital Receipt generation.
* **State Management:** Clear state feedback at every step with an option to reset/replay the simulation at any time.

---

## 8. Python Calculator Integration (Proposed Feature)
The presentation embeds a live Python-powered calculation engine (via PyScript / WebAssembly) allowing real-time estimation of fueling and charging costs.

### 8.1 Formulas
* **Fueling Cost Estimation:**
  $$\text{Total Cost (₪)} = \text{Liters Purchased } (L) \times \text{Price per Liter (₪/L)}$$
* **EV Charging Cost Estimation:**
  $$\text{Energy Required (kWh)} = \text{Battery Capacity (kWh)} \times \left( \frac{\text{Target \%} - \text{Current \%}}{100} \right)$$
  $$\text{Total Cost (₪)} = \text{Energy Required (kWh)} \times \text{Price per kWh (₪/kWh)}$$

### 8.2 Input Validation & Assumptions
* **Validation Rules:** Throw clear UI errors for missing inputs, negative numbers, or invalid battery percentages (where $\text{Current \%} \ge \text{Target \%}$ or values $>100\%$).
* **Disclaimers:** Explicitly display assumptions (e.g., "Excludes battery thermal management losses, variable network fees, or dynamic surge pricing").

---

## 9. Animated 3D Element (Three.js)
* **Visual Scene:** A stylized, low-poly 3D scene featuring a modern vehicle positioned between a traditional fuel pump and a high-speed EV charging post.
* **Interactivity & Performance:** 
  * Smooth rotation/orbit controls or automated camera panning.
  * Dedicated "Replay Animation" / "Reset Camera" control.
  * Non-blocking background/foreground rendering ensuring text remains legible and frame rate stays at $\ge 60\text{ FPS}$.

---

## 10. Content Accuracy & Scope Disclaimer
* **Data Sources:** Station locations, socket counts, pump availability, and fuel prices used in the demo are **simulated mock data**.
* **Payment Processing:** All transaction steps are simulated locally (no live gateway calls).
* **Capability Matrix:** Clear visual indicators separating implemented presentation features from future production roadmap capabilities.
* **Market Claims:** All competitor comparisons and market figures are verified against current industry benchmark data.

---

## 11. GitHub Documentation & Repository Deliverables
The project repository must include:
1. `index.html` (or single standalone bundle) containing the full interactive HTML presentation system.
2. `PRD.md` — Complete Product Requirement Document (this document).
3. `README.md` — Comprehensive project guide covering architecture, local setup instructions, technology stack, screenshots, and operational limitations.
4. `prompts/` directory — Full log of LLM prompts, iterations, code feedback, and architectural refinements.
5. **Git Commit History:** Clean, frequent commit log reflecting progressive development stages by team **NextMind**.

---

## 12. Acceptance Criteria (Definition of Done)

- [ ] **Navigation:** All 10 slides navigate seamlessly via keyboard, buttons, and direct selection.
- [ ] **BiDi & Typography:** Mixed Hebrew, English, numbers, and units display with zero visual corruption.
- [ ] **Interactive Journey:** Users can complete both Fueling and EV Charging demo paths, view simulated receipts, and reset the state.
- [ ] **Python Calculator:** The cost calculator handles valid inputs accurately and safely rejects edge-case/invalid inputs with helpful messaging.
- [ ] **3D Rendering:** Three.js animation loads without errors, runs smoothly, and supports camera replay.
- [ ] **Documentation:** `PRD.md`, `README.md`, and `prompts/` are fully written and committed.
- [ ] **Executability:** An external viewer can run the project locally without complex environment setup.