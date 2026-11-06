# LLM Prompt & Iteration Log — Team NextMind (Fuel&Go)

This log records the engineering prompts, requirements alignment, and architectural refinements during the creation of the Fuel&Go interactive HTML presentation system.

---

## Iteration 1: Repository Initialization & v1_initial.html

### Prompt Summary
- **Input Goal:** Review `PRD.md` and establish the core 10-slide interactive presentation structure for Fuel&Go.
- **Workflow Constraints:**
  - Work directly in the desktop project folder `NextMind`.
  - Maintain an internal versioning folder `Sub_NextMind/` with historical milestone snapshots (`v1_initial.html`).
  - Keep the active root file named `current_version.html`.
  - Stage all files, create descriptive Git commits, and push to GitHub.
  - Ready for academic sharing with `rmisegal@gmail.com`.

### Technical Decisions & Implementation Details
1. **Architecture:** Single-page responsive HTML5/CSS3/ES6 application with no external build-chain dependencies, ensuring immediate executability across any browser.
2. **Design Language:** Modern mobility theme featuring Electric Cyan (`#00f2fe`) and Neon Emerald (`#00ff87`) on dark slate (`#080d1a`).
3. **Typography & BiDi:** Standardized on Plus Jakarta Sans, JetBrains Mono, and Heebo for flawless Hebrew/English BiDi mixed rendering (currency units `₪`, `kWh`, `Liter`).
4. **Interactive Flow Simulator (Slide 7):** Live station, bay, and connector selector with simulated IoT handshake, real-time meter increments, and bilingual receipt generation.
5. **Cost Estimator (Slide 8):** Real-time mathematical calculation engine comparing EV charging vs. ICE fuel benchmark costs.
6. **Navigation System:** Multi-modal navigation supporting keyboard arrow keys, Spacebar, Prev/Next buttons, slide counter, and clickable progress dots.
