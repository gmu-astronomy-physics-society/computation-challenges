# ⚛️ GMAPS Computational Physics & Collaborative Sandbox
> Modular physics computing, browser-based sandboxes, and verifiable portfolio builds for the George Mason Astronomy & Physics Society (`gmu-astronomy-physics-society`).

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/gmu-astronomy-physics-society/computation-challenges?quickstart=1)
[![Discord](https://img.shields.io/badge/Discord-GMAPS_Hub-5865F2?style=flat-square&logo=discord&logoColor=white)](https://discord.gg/KvQBnc2Gj)
[![Languages](https://img.shields.io/badge/Languages-Python_%7C_Julia-blueviolet?style=flat-square)](https://github.com/gmu-astronomy-physics-society)

---

## 🚀 Overview

Research labs often come with heavy prerequisites and steep time commitments. **GMAPS Computational Challenges** is an asynchronous, zero-intimidation sandbox where members learn computational physics by doing real calculations—analyzing CERN collider telemetry, modeling non-linear chaotic dynamics, extracting exoplanet transit dips, and simulating quantum systems.

Everything runs directly in your web browser via **GitHub Codespaces**. You don't need Python or Julia installed on your personal computer, you won't deal with broken PATH variables, and every merged solution permanently records you as an open-source contributor.

---

## ⚡ The Zero-Install Workflow (How to Play)

1. **Get Added to the Org:** Drop your GitHub handle in the `#🚀・active-projects` channel on Discord and tag `@President` (Isa) to receive your repository invite.
2. **Launch Cloud Environment:** Click the **Open in GitHub Codespaces** badge above. In ~60 seconds, a full VS Code environment will launch in your browser with Python, Julia, Jupyter, and all scientific libraries pre-installed.
3. **Select a Challenge:** Navigate the `/Module-XX/` folders, open a challenge notebook (`.ipynb` or `.jl`), and tackle the 3–5 lines of missing physical math or array operations.
4. **Test & Verify:** Run the notebook cells to generate your validation plots and verify test assertions.
5. **Submit a Pull Request (PR):** Use the built-in VS Code **Source Control tab** (on the left sidebar) to commit your branch and submit a PR directly through GitHub. Once reviewed and merged by an officer, you earn your verified server roles and permanent portfolio credit.

---

## 🐍 Why Python & Julia?

Our curriculum focuses strictly on **Python** and **Julia** as primary scientific computing environments:

### 1. Python: The Universal Scientific Stack
* **Ecosystem Breadth:** Python is the current lingua franca of astrophysics, data analysis, and particle physics instrumentation (`NumPy`, `SciPy`, `Matplotlib`, `Astropy`, `Lightkurve`).
* **Glue Language:** It interfaces seamlessly with legacy C/Fortran routines and national laboratory databases (CERN Open Data, MAST, NASA Exoplanet Archive).
* **Gentle Onramp:** Readable syntax allows beginners to immediately focus on physical intuition rather than memory management or syntax boilerplate.

### 2. Julia: High-Performance Mathematical Expressiveness
* **Solving the "Two-Language Problem":** Traditionally, scientists prototype algorithms in Python or MATLAB, then rewrite them in C++ or Fortran for execution speed. Julia eliminates this barrier by compiling directly to native machine code via LLVM, running as fast as C while remaining as expressive as Python.
* **Multiple Dispatch & Linear Algebra:** Julia treats mathematical operations as first-class citizens. Operators match mathematical equations directly (e.g., Unicode operators like `α`, `∇`, and `×`), and its type system naturally reflects physical structures (such as coordinate tensors, custom unit systems, and state vectors).
* **Modern Numerical Solvers:** Libraries like `DifferentialEquations.jl` provide world-class adaptive differential equation solvers that outperform standard scientific libraries.

> **The Alternative Language Policy (C/C++, Rust, Fortran):**  
> Solutions submitted in languages other than Python or Julia are welcomed **only** if accompanied by a `WHY_AND_HOW.md` document explaining:
> 1. *Why* Python or Julia was insufficient (e.g., bare-metal microsecond timing for an SDR satellite receiver, embedded memory constraints).
> 2. *How* to compile, test, and run the code with zero dependencies.

---

## 📚 Curriculum Roadmap

```text
computation-challenges/
├── .devcontainer/                  <-- Pre-configured container configuration
├── Module-01-Foundations/
│   ├── track-python/               <-- Dedicated Python beginner track
│   └── track-julia/                <-- Dedicated Julia beginner track
├── Module-02-Dynamics/             <-- Open track (Solve in Python or Julia)
├── Module-03-Linear-Algebra/       <-- Open track
├── Module-04-Roots-Optimization/   <-- Open track
├── Module-05-Spectral-Fields/      <-- Open track
├── Module-06-Community-Challenges/ <-- Unlocked by Challenge Completers
└── CONTRIBUTING.md                 <-- Contribution, style, and PR guidelines
