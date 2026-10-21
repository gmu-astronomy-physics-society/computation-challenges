# 🪐 GMAPS: Computational Physics & Scientific Sandbox

> **The hands-on computational proving ground for the George Mason University Physics & Astronomy Society (GMAPS / FOTO).**
>
> Zero local installation required. Launch directly in your browser with GitHub Codespaces, clone locally via GitHub Desktop, pick your language, and start exploring physical simulations.

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/gmu-astronomy-physics-society/computation-challenges?quickstart=1)
[![Discord](https://img.shields.io/badge/Discord-GMAPS_Hub-5865F2?style=flat-square&logo=discord&logoColor=white)](https://discord.gg/KvQBnc2Gj)
[![Languages](https://img.shields.io/badge/Languages-Python_%7C_Julia-blueviolet?style=flat-square)](https://github.com/gmu-astronomy-physics-society)

---

## 🧭 Table of Contents

1. [Why This Repository Exists](#why-this-repository-exists)
2. [The Languages: Origins & Physics Workflows](#the-languages-origins--physics-workflows)
   * [Python: The Scientific Ecosystem Lingua Franca](#1-python-the-scientific-ecosystem-lingua-franca)
   * [Julia: The High-Performance Mathematical Native](#2-julia-the-high-performance-mathematical-native)
   * [The Dual-Language Mandate in This Repo](#the-dual-language-mandate-in-this-repo)
3. [Repository Architecture](#repository-architecture)
4. [Curriculum Overview (Notebooks 01–05)](#curriculum-overview-notebooks-0105)
5. [Getting Started: Codespaces vs. GitHub Desktop](#getting-started-codespaces-vs-github-desktop)
6. [Contribution & Git Workflow](#contribution--git-workflow)
7. [Contributor Roles & Server Recognition](#contributor-roles--server-recognition)
8. [The "Endgame" Protocol: Submitting Community Challenges](#the-endgame-protocol-submitting-community-challenges)
9. [Academic Integrity & Honor Code](#academic-integrity--honor-code)

---

## 🌌 Why This Repository Exists

Most undergraduate physics curricula treat computation like an afterthought: a rushed spreadsheet exercise or a script copy-pasted at 2:00 AM before a lab deadline.

In modern scientific research—whether isolating $Z$-boson resonance spikes at CERN, reconstructing dark matter rotation curves, modeling chaotic non-linear orbital dynamics, or solving bound states in quantum potentials—**analytical physics and numerical execution are the exact same discipline.**

This sandbox is engineered to:

* **Demystify mathematical formalisms:** Take analytical equations (Euler-Lagrange equations, Runge-Kutta integrators, singular value decomposition, Fourier transforms) and run them on live physical data.
* **Overcome technical intimidation:** You do not need a computer science degree to write high-performance scientific code.
* **Build verifiable portfolio lines:** Every merged challenge is an open-source commit permanently tracked on your GitHub profile and linked to your resume, CV, or graduate school application.

---

## ⚡ The Languages: Origins & Physics Workflows

Scientific computing has historically suffered from the **"Two-Language Problem"**: researchers prototype ideas in an expressive, easy-to-read language (like Python, MATLAB, or R), only to discover it runs far too slowly for large-scale production, forcing them to rewrite the entire codebase in C, C++, or Fortran.

To prepare you for contemporary research, this repository centers on the two defining languages of modern computational science:

| Attribute | Python | Julia |
| :--- | :--- | :--- |
| **Conceived** | 1989 by Guido van Rossum at CWI (Netherlands) as an intuitive, high-level language. | 2009 at MIT by Bezanson, Karpinski, Shah, and Edelman to eliminate the Two-Language Problem. |
| **Role in Physics** | The universal glue: vast data ecosystems (`Astropy`, `ROOT`/`uproot`, `SciPy`, `NumPy`, `Lightkurve`). | High-performance differential equations, quantum state tensors, and native blackboard math syntax. |
| **Execution Model** | Interpreted; relies on compiled C-extensions (`NumPy`, BLAS/LAPACK) for vectorized speed. | JIT compiled via LLVM to native machine code for direct C/Fortran-level speed. |

### 1. Python: The Scientific Ecosystem Lingua Franca

#### Where It Comes From

Python was created in late 1989 by Dutch programmer Guido van Rossum at the Centrum Wiskunde & Informatica (CWI) in Amsterdam and released in 1991. Van Rossum set out to design an intuitive, highly readable language emphasizing clean syntax and developer productivity (naming it after *Monty Python's Flying Circus*).

Python was not originally designed specifically for scientific computing. However, in the late 1990s and early 2000s, physicists and astronomers rallied around community extensions (`Numeric` and `Numarray`, unified in 2005 by Travis Oliphant into `NumPy`). The emergence of `SciPy`, John Hunter’s `Matplotlib`, and `IPython`/`Jupyter` transformed Python into the standard platform for open science worldwide.

#### How Physicists Use It

* **Astrophysics & Space Science:** The default stack across NASA, STScI, and ESA missions. Packages like `Astropy` handle celestial coordinate frames, FITS file ingestion, and cosmological models; `Lightkurve` analyzes exoplanet transit dips from Kepler and TESS.
* **High-Energy Particle Physics:** CERN, Fermilab, and the Large Hadron Collider rely on Python for event filtering. Packages like `awkward-array`, `uproot`, and `PyROOT` let particle physicists filter terabytes of collision data to compute relativistic invariant masses and plot di-lepton resonance spikes.
* **Gravitational Waves & Cosmology:** The LIGO Scientific Collaboration uses the Python-based `LALSuite` pipeline to filter strain data, perform matched filtering against template banks, and detect black hole and neutron star coalescences.

### 2. Julia: The High-Performance Mathematical Native

#### Where It Comes From

Julia was born out of frustration with existing numerical tools. Conceived in 2009 and publicly released in 2012 by Jeff Bezanson, Stefan Karpinski, Viral B. Shah, and Alan Edelman at MIT, Julia was engineered from line one specifically for scientific, mathematical, and numerical computing.

The MIT team designed Julia to solve the Two-Language Problem: they wanted the readability and dynamism of Python, the mathematical ergonomics of MATLAB, and the raw speed of C/Fortran. By coupling a multiple-dispatch paradigm with a Just-In-Time (JIT) compiler built on top of LLVM, Julia compiles mathematical code directly to native CPU machine instructions on the fly.

#### How Physicists Use It

* **Adaptive Dynamical Systems:** Julia’s `DifferentialEquations.jl` suite is recognized as one of the fastest and most sophisticated differential equation engines in existence, used to simulate complex non-linear dynamics, chaotic attractors, and spacecraft orbital transfers.
* **Quantum Many-Body Physics & Tensors:** Modern condensed matter and quantum information physics leverage packages like `ITensors.jl` and `Yao.jl` for quantum circuits and tensor-network contractions, where Julia's multiple dispatch handles high-rank tensor operations effortlessly.
* **Black Hole Imaging & Large-Scale Modeling:** The Event Horizon Telescope (EHT) collaboration uses Julia routines for high-dimensional interferometric reconstructions of supermassive black hole shadow images.
* **Mathematical Notation in Code:** Julia allows native Unicode syntax directly in code: you can write Greek letters, derivatives, and tensor products ($dx/dt = v$, $\mathbf{E} = -\nabla\phi$, $\alpha \otimes \beta$) identically to how they appear on a classroom blackboard.

### The Dual-Language Mandate in This Repo

* **Notebook 01 (Foundations):** Divided into two independent beginner tracks: `track-python/` and `track-julia/`. If you are entirely new to programming, choose **Python** to learn basic array manipulation. If you want to experience cutting-edge numerical design, choose **Julia**.
* **Notebooks 02 through 05:** Dual-track challenges. Every challenge folder provides starter files for **both** languages. You choose which language you want to deploy to solve the challenge.
* **The "Alternative Language" Rule:** You may submit solutions in C, C++, Rust, or Fortran, provided you include a `WHY_AND_HOW.md` demonstrating why Python or Julia was insufficient for your physical constraints and showing how to compile it with zero external dependencies.

---

## 📂 Repository Architecture

```text
computation-challenges/
├── .devcontainer/                  <-- Codespaces cloud container: Python 3.11 & Julia
├── Notebook-01-Foundations/        <-- Entry level: array slicing, float gotchas
│   ├── track-julia/                <-- Pure Julia syntax, structs, broadcasting
│   └── track-python/               <-- Pure Python/NumPy indexing, memory layout
├── Notebook-02-Dynamics/           <-- Numerical calculus, RK4, chaotic attractors
├── Notebook-03-Linear-Algebra/     <-- Resistor networks, SVD compression, inertia tensors
├── Notebook-04-Roots-Optimization/ <-- Lennard-Jones potentials, non-linear decay fitting
├── Notebook-05-Signals-Fields/     <-- Cooley-Tukey FFT, 2D electrostatic vector fields
├── Notebook-06-Advanced-Frontiers/ <-- Community-authored challenges & endgame sandbox
├── CONTRIBUTING.md                 <-- Git contribution & code style guidelines
└── README.md                       <-- You are here
```

---

## 📚 Curriculum Overview (Notebooks 01–05)

### 🔹 Notebook 01: Foundations & The Scientific Sandbox

*Goal: Understand memory models, vectorized array operations, and floating-point roundoff traps.*

* **Track Python:**
  * `P1.1`: Ballistic kinematics, parameter assertions, and testing floating-point precision (`0.1 + 0.2 != 0.3`).
  * `P1.2`: The "Where $PV=nRT$ Dies" isotherm explorer (vectorized Van der Waals phase collapse).
  * `P1.3`: Vectorized 2D Brownian motion, random walks, and verifying Einstein's $\langle r^2 \rangle \propto t$.
* **Track Julia:**
  * `J1.1`: Artillery tables, array broadcasting (`.`), and angle of reach calculations.
  * `J1.2`: Simulating the Curta mechanical calculator via bitwise ALU shifts and register logic.
  * `J1.3`: Modeling Falcon 9 propellant burn budgets using custom mutable `struct`s with physical invariants.

### 🔹 Notebook 02: Numerical Calculus & Dynamical Systems

*Goal: Move beyond pen-and-paper integrals; conquer non-linear differential equations and deterministic chaos.*

* `02.1`: Forward vs. central finite differences and locating the catastrophic cancellation floor ($h_{\text{opt}} \sim \sqrt{\epsilon_m}$).
* `02.2`: The chaotic driven pendulum: implementing Runge-Kutta 4th-order (RK4) to visualize phase-space strange attractors.
* `02.3`: Quantum well bound states: solving the 1D Time-Independent Schrödinger Equation via the Shooting Method and Numerov algorithm.

### 🔹 Notebook 03: Linear Algebra & Matrix Mechanics

*Goal: Ground abstract matrix spaces into physical networks, coordinate frames, and dimensionality reduction.*

* `03.1`: Multi-loop Kirchhoff resistance networks, LU decomposition, and matrix condition numbers ($\kappa(A)$).
* `03.2`: Principal moments and axes of inertia: diagonalizing $3 \times 3$ rigid-body inertia tensors.
* `03.3`: Astronomical image compression: Singular Value Decomposition (SVD) and low-rank matrix approximations.

### 🔹 Notebook 04: Roots, Optimization & Parameter Fitting

*Goal: Find equilibria in non-linear potentials and extract physical parameters from noisy detector telemetry.*

* `04.1`: Diatomic Lennard-Jones molecular potential energy minimization via gradient descent / BFGS.
* `04.2`: Non-linear least squares: fitting multi-isotope radioactive decay chains with missing (`NaN`) detector values.

### 🔹 Notebook 05: Spectral Analysis & Vector Fields

*Goal: Decompose signals into constituent harmonics and visualize multivariable spatial forces.*

* `05.1`: Radix-2 Cooley-Tukey Fast Fourier Transform (FFT) from scratch: identifying discrete harmonics vs. broadband chaos.
* `05.2`: Streamline mapping: discretizing 2D Poisson/Laplace equations and rendering electric vector fields $\mathbf{E} = -\nabla \phi$.

---

## 🚀 Getting Started: Codespaces vs. GitHub Desktop

You can complete these challenges completely in the cloud or on your local machine:

| Feature | Option 1: GitHub Codespaces *(Recommended)* | Option 2: GitHub Desktop *(Local Setup)* |
| :--- | :--- | :--- |
| **Installation** | Zero local installation required. | Requires local Python, Julia, and Jupyter setup. |
| **Runtime** | Runs directly in your web browser. | Runs locally on your machine. |
| **Dependencies** | Python 3.11, Julia, and all packages pre-installed. | Manual package management via `pip` and `Pkg`. |
| **Portability** | Work seamlessly across laptops, tablets, or library PCs. | Tied to your local workstation; works offline. |

### Option 1: GitHub Codespaces (Recommended for Beginners)

*If you are just starting out, we strongly suggest using Codespaces. You can begin coding immediately without configuring PATH variables or environment conflicts:*

1. Click the **`Open in GitHub Codespaces`** badge at the top of this README (or fork this repo, click the green **`Code`** button $\to$ **`Codespaces`** tab $\to$ **`Create codespace on main`**).
2. GitHub will spin up an isolated Linux container in your browser pre-loaded with:
   * Python 3.11 + `numpy`, `scipy`, `matplotlib`, `astropy`, `sympy`, `jupyter`.
   * Stable Julia release + `IJulia`, `Plots`, `LinearAlgebra`.
3. Open any notebook under `Notebook-01-Foundations/` and run the cells.

### Option 2: GitHub Desktop (Local Development)

*If you prefer working locally on your personal machine:*

1. Install [GitHub Desktop](https://desktop.github.com/) and clone your fork of the repository:
   * In GitHub Desktop: **File** $\to$ **Clone repository...** $\to$ select your fork.
2. Ensure you have installed locally:
   * Python (3.10+) with Jupyter notebook support.
   * Julia (1.9+) with `IJulia` installed via `using Pkg; Pkg.add("IJulia")`.
3. Open the cloned folder in your local editor (VS Code, JupyterLab, etc.) and select the corresponding Python or Julia kernel.

---

## 🛠️ Contribution & Git Workflow

All challenge solutions and additions must be submitted via Pull Requests (PRs) on GitHub:

```bash
# 1. Create a feature branch for your challenge
git checkout -b solve/notebook-02-rk4

# 2. Complete your solution cells and verify test assertions pass
# (Do NOT commit bulky cache directories or .ipynb_checkpoints)

# 3. Stage and commit your work
git add Notebook-02-Dynamics/
git commit -m "feat(dynamics): complete RK4 chaotic pendulum challenge"

# 4. Push to your branch and open a Pull Request
git push origin solve/notebook-02-rk4
```

### Pull Request Guidelines

1. **One challenge per PR:** Keep diffs clean and reviewable.
2. **Comment your derivations:** Explain *why* a particular step size, discretization scheme, or boundary condition was chosen.
3. **Publication-quality plots:** Figures must include labeled axes and physical SI units.

---

## 🎖️ Contributor Roles & Server Recognition

Merging approved PRs unlocks permanent roles on the GMAPS Discord server, celebrating your technical milestones:

| Contributor Tier | Server Role | Milestone Requirement |
| :--- | :--- | :--- |
| **Tier 1: Solver** | `@eigenbaby` | Solve and merge any challenge from **Notebook 01** (Python or Julia). |
| **Tier 2: Practitioner** | `@rk4 demon` | Solve and merge at least 3 challenges across **Notebooks 02–04**. |
| **Tier 3: Veteran** | `@hamiltonian menace` | Solve advanced dynamics (02.2 chaos, 02.3 quantum shooting, or 05.1 custom FFT). |
| **Tier 4: Architect** | `@flight director` | Complete all 5 core notebooks or author an approved community challenge. |

---

## 🏆 The "Endgame" Protocol: Submitting Community Challenges

Once you have completed all five core notebooks, you unlock **Architect Status** (`@flight director`).

To ensure the club curriculum remains fresh and expands with every incoming class, challenge completers are invited to design and publish **their own original computational physics challenges** for future members.

### Two Ways to Submit Your Challenge

#### Option A: Expand an Existing Notebook (Notebooks 01–05)

If your challenge expands upon a core topic (e.g., adding an asymmetric spinning top to `Notebook-03` or a driven Duffing oscillator to `Notebook-02`):

1. Navigate to the target notebook folder.
2. Append a new section formatted as:  
   `### Challenge [X.Y]: [Title] (Contributed by @YourGitHubHandle)`.
3. Provide:
   * Theoretical framing and physical equations formatted in LaTeX.
   * Starter code scaffolding with clear `TODO` markers.
   * Assert-based unit tests for students to verify their results.
   * A companion solution key branch or reference file.

#### Option B: Submit to `Notebook-06-Advanced-Frontiers`

For advanced, cross-disciplinary, or specialized topics (e.g., General Relativity geodesics, Monte Carlo Ising models, N-body orbital resonances, Lattice Boltzmann fluid simulations, or Quantum Computing circuits):

1. Open `Notebook-06-Advanced-Frontiers/`.
2. Create a dedicated folder: `Challenge-[Topic-Slug]/` containing:
   * `problem.ipynb` (starter challenge with scaffolding).
   * `solution.ipynb` (verified, fully working reference).
   * `README.md` explaining the background physics and literature citations.
3. Open a Pull Request tagged with the label `community-challenge`.
4. Once reviewed and verified by an officer, your challenge will be merged into the official club curriculum and permanently credited under your name!

---

## ⚖️ Academic Integrity & Honor Code

* **Engage with the derivations:** Looking up analytical formulas is standard research; generating raw code using LLMs without understanding the numerical discretization leaves you stranded in upper-level physics courses.
* **Collaborate openly:** We encourage working through numerical algorithms together in the `#projects-and-code` Discord channel or during in-person Whiteboard Salons. If someone helps you catch an algebraic sign error, credit them in your comments!
* **Coursework Policy & The Past-Semester Exception:**
  * **The Core Rule:** You may **NEVER** post, adapt, or share active, graded coursework or exam problems.
  * **The Past-Semester Exception:** You **ARE permitted** to submit adaptations of your own original projects and code that were originally submitted for university coursework (e.g., PHYS 251, 325, 410, etc.), **provided that the course was completed and graded at least one full semester ago.** Submissions based on past coursework must be your own original work and formatted to fit the club's educational template.
  * **Why This Rule Exists (Protecting YOU from Plagiarism Accusations):** This policy is designed first and foremost to protect **you**. Posting code or project work from an active, ongoing class creates serious academic risk: if a classmate stumbles across your public repository, copies your code, or submits similar work, automated similarity software (like MOSS or Canvas plagiarism checkers) will flag your submission. You could find yourself dragged before the GMU Honor Committee facing accusations of unauthorized collaboration, publishing course material, or self-plagiarism. Enforcing a strict buffer of **at least one full graded semester** ensures the class is closed, grades are permanently logged, and your code can never be weaponized against you.
