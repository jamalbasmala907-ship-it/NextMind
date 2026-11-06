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


---

## Iteration 2: Version 2 (v2_calculator) Milestone

### Prompt Summary
- **Goal:** Update to Version 2 (`v2_calculator`) based on PRD.md:
  1. **Color Palette Theme:** Triad theme combining Blue (`#00f2fe`, `#0284c7`), Green (`#00ff87`, `#10b981`), and Orange (`#ff7b00`, `#ff6b35`).
  2. **Team Names & Branding:** Add authors **BASMALA JAMAL + MARIA MNASRA** prominently on Slide 1 and header; create and include project SVG logo assets.
  3. **Python Calculator & Interactivity:** Integrated WebAssembly Pyodide execution with pure Python script evaluation for EV charging and ICE benchmark costs with Israeli Shekels (`₪`).
  4. **Three.js 3D Animation:** Integrated 3D station workflow scene (Slide 6) with interactive orbit controls, vehicle arrival, fuel dispenser, high-speed EV charger, animated energy particle stream, and 4-stage workflow tracking.
  5. **Snapshot & Git Workflow:** Save snapshot `Sub_NextMind/v2_calculator.html`, update `current_version.html`, stage all changes, commit: `'Add Python calculator, Three.js 3D workflow animation, color theme, team names, and logo'`, and push to GitHub.
