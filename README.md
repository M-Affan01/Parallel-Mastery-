<div align="center">

# Parallel Mastery 
### *Interactive Mathematical Simulation for Amdahl's & Gustafson's Laws*

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![License: MIT](https://img.shields.io/badge/License-MIT-success.svg?style=for-the-badge)
![Status: Production Ready](https://img.shields.io/badge/Status-Production_Ready-blueviolet?style=for-the-badge)

**An enterprise-grade, infinitely-generating educational dashboard designed to demystify the theoretical limits of parallel computing through real-time mathematical visualizations.**

</div>

---

## Project Overview

Understanding the theoretical maximum speedup of parallel computing is crucial for systems architecture and performance engineering. **Parallel Mastery** transforms abstract mathematical formulas—specifically **Amdahl's Law** (fixed problem size) and **Gustafson's Law** (scaled problem size)—into an immersive, gamified visual experience. 

Designed with a premium "Midnight Cyber" glassmorphism aesthetic, the application procedurally generates unlimited challenges, tracks user performance streaks, and provides animated, step-by-step visual breakdowns of how multiple processors divide parallel workloads.

---

## Main Features

### ♾️ Infinite Procedural Generation Engine
The application relies on a custom `Generator` module that algorithmically randomizes sequential/parallel fractions ($s$ and $p$) and processor counts ($N$). It mathematically guarantees solvable, unique scenarios every time you request a new challenge.

### Premium "Midnight Cyber" UI / UX
Built purely with Vanilla CSS, the interface features enterprise-level design systems:
*   **Deep Glassmorphism**: Blurred backdrop filters, glowing interactive borders, and floating background orbs.
*   **Real-world Interactions**: Tactile input fields with inset shadows, button depress states, and staggered layout entry animations.
*   **Distraction-Free Focus**: Removed unnecessary iconography in favor of clean, readable typography using *Inter* and *JetBrains Mono*.

### Interactive Visual Solver
Instead of standard text-based solutions, the application features an animated step-by-step visualizer:
*   **Step 1:** Dynamically draws the original program's execution time, highlighting Sequential vs. Parallel workloads.
*   **Step 2:** Visually shrinks (Amdahl) or scales (Gustafson) the parallel CSS blocks in real-time to demonstrate the processor's impact.
*   **Step 3:** Overlays the final mathematical formula mapped directly to the visual blocks.

### Gamified Learning State
Features local streak tracking, rolling number animations, and dynamic difficulty scaling. A persistent "Skip Question" mechanic allows users to freely navigate challenges without penalty.

---

## Technical Stack & Tools

*   **Core Languages**: HTML5, CSS3, JavaScript (ES6+)
*   **Architecture**: Vanilla SPA (Single Page Application)
*   **Icons & Assets**: Lordicon (Animated SVGs)
*   **Typography**: Google Fonts (`Inter` for UI, `JetBrains Mono` for math, `Outfit` for headers)
*   **Design Paradigm**: Vanilla CSS Variables (`:root`), Flexbox/Grid, Keyframe Animations

---

## Architecture & System Design

The application is encapsulated within a lightweight, zero-dependency, single-file architecture (`index.html`) utilizing the Module Pattern:

1.  **`Generator` Object (Logic Layer)**:
    *   `generateAmdahl()`: Calculates $Speedup = \frac{1}{(1-P) + \frac{P}{N}}$
    *   `generateGustafson()`: Calculates $Speedup = N + (1 - N) \times s$
    *   Responsible for generating the question text, formatting parameters, and calculating the strict float tolerance for the correct answer.
2.  **`Quiz` Object (State & Controller Layer)**:
    *   Manages user `streak`, `totalSolved`, and `isAnswered` states.
    *   Handles DOM manipulation, triggering CSS animations (`slideUpFade`, `pulseStat`), and rendering the dynamic visual solver via `revealSolution()`.
3.  **Visual Engine (Presentation Layer)**:
    *   CSS-driven visualizer bars (`.v-seq`, `.v-par`) that use dynamic inline styling (`width: X%`) injected by the Controller to visually represent hardware scaling.

---

## Quick Start & Installation

Because this is a Vanilla JS application with no build steps, deployment and local running are instantaneous.

### Method 1: Local File Execution (Easiest)
1. Clone the repository or download the ZIP file.
2. Extract the folder.
3. Double-click `index.html` to open it in your default web browser.

### Method 2: VS Code Live Server (Recommended for Development)
1. Open the project folder in **Visual Studio Code**.
2. Install the **Live Server** extension by Ritwick Dey.
3. Right-click `index.html` and select **"Open with Live Server"**.

---

## Usage Guide

1. **Analyze the Prompt**: Read the dynamically generated question. The UI will indicate whether you are solving for Amdahl's or Gustafson's Law via the top-left badge.
2. **Calculate**: Determine the theoretical speedup using the provided Parallel/Sequential fractions and Processor ($N$) count.
3. **Submit**: Enter your answer (e.g., `4.25`) into the input field and press `Enter` or click **Verify Answer**. (The system accepts a tolerance of $\pm0.05$).
4. **Review Visuals**: If you are stuck, or simply want to review the math, click **Reveal Solution** to watch the animated breakdown of how the processors scale the workload.
5. **Continue**: Click **Next Challenge** to generate a new scenario and build your streak.

---

## Project Structure

```text
📦 Amdahls-and-Gustafsons
 ┗ index.html        # Core application (HTML, CSS, JS Engine)
 ┗ README.md         # Project Documentation
```

---

## Performance & Optimization

*   **Zero Dependencies**: No React, Vue, or heavy JS libraries. The application loads instantaneously.
*   **Hardware-Accelerated Animations**: Uses `transform` and `opacity` for all CSS animations (`slideUpFade`, `slideInRight`) to ensure smooth 60FPS rendering without triggering expensive browser repaints.
*   **Event Delegation**: Keyboard listeners are bound to the global window object to provide seamless `Enter` key support without requiring input focus.

---

## Future Plans

*   **Persistent Storage**: Implement `localStorage` API to save high scores and long-term streaks across browser sessions.
*   **Confetti Canvas Integration**: Upgrade the `launchConfetti()` stub with a particle physics engine for enhanced positive reinforcement.
*   **Additional Architectures**: Introduce formulas for the **Sun-Ni Law** (memory-bounded scaling) to complete the parallel computing trifecta.

---

## Contributing Guidelines

Contributions are welcome! If you have ideas for improving the visualizer algorithms, adding new parallel computing laws, or enhancing the CSS animations:
1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## Contact Info

Designed and developed for Professional Parallel Computing Analysis.
*   **LinkedIn**: [Affan Nexor](https://www.linkedin.com/in/affan-nexor-66abb8321/)
*   **Email**: maffan2830@gmail.com
