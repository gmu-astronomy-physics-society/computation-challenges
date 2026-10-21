# 🪐 GMAPS: Computational Physics & Scientific Sandbox

> The computational project hub for the George Mason University Physics & Astronomy Society (GMAPS / FOTO).
>
> Zero local installation required. Launch straight in your browser with GitHub Codespaces, clone locally using GitHub Desktop, pick Python or Julia, and work through real physical simulations.

## 🧭 Table of Contents

1. [Why This Repository Exists](#why-this-repository-exists)

2. [Why Python & Julia?](#why-python--julia)

   * [Python: The Scientific Standard](#1-python-the-scientific-standard)

   * [Julia: Built for Numerical Math](#2-julia-built-for-numerical-math)

   * [How Languages Work in This Repo](#how-languages-work-in-this-repo)

3. [Repository Layout](#repository-layout)

4. [Curriculum Overview (Notebooks 01–05)](#curriculum-overview-notebooks-0105)

5. [Getting Started: Codespaces vs. GitHub Desktop](#getting-started-codespaces-vs-github-desktop)

6. [Git Workflow & Submitting Solutions](#git-workflow--submitting-solutions)

7. [Discord Roles & Recognition](#discord-roles--recognition)

8. [Community Challenges: Creating Your Own](#community-challenges-creating-your-own)

9. [Academic Integrity & Honor Code](#academic-integrity--honor-code)

## 🌌 Why This Repository Exists

In most physics degree programs, computational skills are barely taught—usually crammed into a quick spreadsheet exercise or an unguided Python script due at midnight before a lab report.

In actual research—analyzing particle collision data at CERN, fitting exoplanet light curves, modeling chaotic orbits, or solving quantum bound states—analytical theory and numerical computation go hand-in-hand.

This repository exists to help you:

* **Connect lecture math to working code:** Take analytical equations (Runge-Kutta integration, singular value decomposition, Fourier transforms) and run them on realistic datasets.

* **Get comfortable with scientific programming:** You do not need a computer science background to write clean, effective code for physics problems.

* **Build portfolio projects for your resume:** Every merged pull request is an open-source commit on your public GitHub profile that you can put on your resume, CV, or grad school applications.

## ⚡ Why Python & Julia?

Scientific computing has historically run into the **"Two-Language Problem"**: researchers prototype code in an easy-to-write language like Python, MATLAB, or R, only to find that it runs too slowly for large-scale simulations—forcing them to rewrite the entire project in C, C++, or Fortran.

To give you practical experience with modern research tools, this repo focuses on the two primary languages used in computational science today:

| Feature | Python | Julia | 
| ----- | ----- | ----- | 
| **Origin** | Created in 1989 by Guido van Rossum at CWI (Netherlands) as an accessible, high-level language. | Created in 2009 at MIT by Bezanson, Karpinski, Shah, and Edelman to solve the Two-Language Problem. | 
| **Role in Physics** | The industry standard: vast ecosystem of libraries (`Astropy`, `uproot`, `SciPy`, `NumPy`, `Lightkurve`). | High-speed differential equations, quantum tensors, and clean mathematical notation. | 
| **Execution** | Interpreted; relies on compiled C/C++ backends (`NumPy`, BLAS/LAPACK) for fast vectorized math. | JIT (Just-In-Time) compiled via LLVM directly into native machine code at C/Fortran speeds. | 

### 1. Python: The Scientific Standard

#### Background

Python was developed in late 1989 by Dutch programmer Guido van Rossum at Centrum Wiskunde & Informatica (CWI) and released in 1991. He designed it to be readable, intuitive, and beginner-friendly, naming it after the comedy troupe *Monty Python*.

Python was not built specifically for science. However, in the late 1990s and early 2000s, scientists built numerical extensions for it (`Numeric` and `Numarray`, which Travis Oliphant merged in 2005 to form `NumPy`). With the arrival of `SciPy`, `Matplotlib`, and `Jupyter`, Python became the default open-source platform for academic research worldwide.

#### How Physicists Use It

* **Astrophysics & Space Science:** The standard stack at NASA, STScI, and ESA. Libraries like `Astropy` handle celestial coordinate frames, FITS data, and cosmology, while `Lightkurve` analyzes transit photometry from missions like Kepler and TESS.

* **Particle Physics:** Experiments at CERN and Fermilab rely heavily on Python. Packages like `uproot`, `awkward-array`, and `PyROOT` let researchers analyze terabytes of LHC collision data to calculate invariant masses and isolate resonance peaks.

* **Gravitational Waves:** The LIGO Scientific Collaboration relies on Python pipelines (`LALSuite`) to filter detector strain data, run matched filtering against waveform template banks, and detect gravitational-wave events.

### 2. Julia: Built for Numerical Math

#### Background

Julia was created to fix the inefficiencies of existing numerical platforms. Started in 2009 and released in 2012 by Jeff Bezanson, Stefan Karpinski, Viral B. Shah, and Alan Edelman at MIT, Julia was engineered specifically for technical, scientific, and numerical work.

The creators wanted the high-level readability of Python, the mathematical ease of MATLAB, and the execution speed of C. Julia uses multiple dispatch alongside a Just-In-Time (JIT) compiler built on LLVM, compiling functions into fast machine code the first time they are executed.

#### How Physicists Use It

* **Non-Linear Dynamics & ODEs:** Julia's `DifferentialEquations.jl` suite is one of the most capable differential equation engines available, widely used for simulating non-linear dynamics, chaotic systems, and orbital trajectories.

* **Quantum Many-Body Physics:** Condensed matter and quantum information researchers use packages like `ITensors.jl` and `Yao.jl` for quantum circuits and tensor network contractions, where multiple dispatch handles high-rank tensor algebra efficiently.

* **Black Hole Imaging:** The Event Horizon Telescope (EHT) collaboration uses Julia libraries for high-dimensional image reconstruction of supermassive black holes.

* **Blackboard Math Syntax:** Julia natively supports Unicode characters in source code, meaning you can write Greek letters, derivatives, and vectors ($dx/dt = v$, $\mathbf{E} = -\nabla\phi$, $\alpha \otimes \beta$) exactly as they appear in lectures and textbooks.

### How Languages Work in This Repo

* **Notebook 01 (Foundations):** Split into two separate beginner tracks: `track-python/` and `track-julia/`. If you are new to programming, pick **Python** to learn basic syntax and array operations. If you want to explore high-performance numerical computing, pick **Julia**.

* **Notebooks 02 through 05:** Dual-track challenges. Every challenge folder provides starter files for **both** languages. You choose which one you want to use.

* **Alternative Languages:** You are welcome to submit solutions in C, C++, Rust, or Fortran, provided you include a `WHY_AND_HOW.md` explaining why Python or Julia was insufficient for your specific problem and how to compile your code with zero external dependencies.

## 📂 Repository Layout

```
computation-challenges/
├── .devcontainer/                  <-- Pre-configured Codespaces setup (Python 3.11 & Julia)
├── Notebook-01-Foundations/        <-- Beginner basics: indexing, vectors, float precision
│   ├── track-julia/                <-- Pure Julia syntax, structs, broadcasting
│   └── track-python/               <-- Pure Python, NumPy arrays, memory layouts
├── Notebook-02-Dynamics/           <-- Numerical calculus, RK4, chaotic pendulums
├── Notebook-03-Linear-Algebra/     <-- Resistor circuits, SVD image compression, inertia
├── Notebook-04-Roots-Optimization/ <-- Potential energy minimization, curve fitting
├── Notebook-05-Signals-Fields/     <-- FFT algorithms, 2D electric field mapping
├── Notebook-06-Advanced-Frontiers/ <-- Community-authored student challenges
├── CONTRIBUTING.md                 <-- Git contribution & style guidelines
└── README.md                       <-- You are here

```

## 📚 Curriculum Overview (Notebooks 01–05)

### 🔹 Notebook 01: Foundations & Scientific Sandboxes

*Focus: Learn array slicing, vectorization, and floating-point roundoff errors.*

* **Python Track:**

  * `P1.1`: Projectile kinematics, parameter validation, and exploring floating-point precision issues (`0.1 + 0.2 != 0.3`).

  * `P1.2`: Van der Waals isotherms—using vectorized arrays to find where the ideal gas law fails near critical temperature $T_c$.

  * `P1.3`: 2D Brownian motion random walks, verifying Einstein's diffusion relation ($\langle r^2 \rangle \propto t$) without slow `for` loops.

* **Julia Track:**

  * `J1.1`: Trajectory tables, array broadcasting (`.`), and angle-of-reach calculations.

  * `J1.2`: Simulating a Curta mechanical calculator using bitwise shifts and ALU logic.

  * `J1.3`: Modeling rocket stage mass depletion using mutable `struct` types with physical validation rules.

### 🔹 Notebook 02: Numerical Calculus & Dynamical Systems

*Focus: Move beyond analytical formulas; solve non-linear differential equations and deterministic chaos.*

* `02.1`: Comparing forward and central finite difference schemes, and observing the balance between truncation and roundoff error ($h_{\text{opt}} \sim \sqrt{\epsilon_m}$).

* `02.2`: Writing a 4th-order Runge-Kutta (RK4) integrator to simulate a driven pendulum transitioning into chaotic phase space.

* `02.3`: Finding bound-state energy levels in a 1D quantum well using the Shooting Method and the Numerov algorithm.

### 🔹 Notebook 03: Linear Algebra & Matrix Mechanics

*Focus: Apply matrix methods to physical systems, coordinate transforms, and data compression.*

* `03.1`: Solving multi-loop resistor networks via LU decomposition, and checking condition numbers ($\kappa(A)$) for circuit sensitivity.

* `03.2`: Diagonalizing $3 \times 3$ rigid-body inertia tensors to find principal moments and rotation axes.

* `03.3`: Compressing 2D detector images using Singular Value Decomposition (SVD) and low-rank matrix approximations.

### 🔹 Notebook 04: Roots, Optimization & Parameter Fitting

*Focus: Find equilibrium states in potentials and extract parameters from experimental data.*

* `04.1`: Finding the equilibrium bond length and spring constant of a Lennard-Jones molecular potential using gradient descent.

* `04.2`: Non-linear least-squares fitting of radioactive decay chains containing noisy and missing (`NaN`) detector entries.

### 🔹 Notebook 05: Spectral Analysis & Vector Fields

*Focus: Decompose signals into frequency components and visualize multivariable fields.*

* `05.1`: Implementing a Radix-2 Cooley-Tukey Fast Fourier Transform (FFT) from scratch to contrast periodic signals against chaotic noise.

* `05.2`: Discretizing Poisson's equation on a 2D grid and rendering electric field streamlines ($\mathbf{E} = -\nabla \phi$).

## 🚀 Getting Started: Codespaces vs. GitHub Desktop

You can work on these challenges entirely in your web browser or locally on your computer:

| Detail | Option 1: GitHub Codespaces *(Recommended)* | Option 2: GitHub Desktop *(Local Setup)* | 
| ----- | ----- | ----- | 
| **Setup Required** | Zero local installation. | Requires installing Python, Julia, and Jupyter manually. | 
| **Environment** | Runs in your web browser inside an isolated cloud container. | Runs directly on your personal computer. | 
| **Pre-installed Tools** | Python 3.11, Julia, and all necessary physics libraries ready to go. | You manage your own packages using `pip` and `Pkg`. | 
| **Portability** | Works on any device (laptop, tablet, campus library PC). | Stays on your machine; works offline. | 

### Option 1: GitHub Codespaces (Recommended for Beginners)

*If you want to start coding immediately without troubleshooting PATH variables or package conflicts, use Codespaces:*

1. Click the **`Open in GitHub Codespaces`** badge at the top of this README (or fork this repo, click the green **`Code`** button $\to$ **`Codespaces`** tab $\to$ **`Create codespace on main`**).

2. GitHub will open a full VS Code environment in your browser with everything pre-configured:

   * Python 3.11 with `numpy`, `scipy`, `matplotlib`, `astropy`, `sympy`, and `jupyter`.

   * Stable Julia release with `IJulia`, `Plots`, and `LinearAlgebra`.

3. Open any challenge file in `Notebook-01-Foundations/` and start running cells.

### Option 2: GitHub Desktop (Local Development)

*If you prefer working locally on your personal laptop or desktop:*

1. Install [GitHub Desktop](https://desktop.github.com/) and clone your fork of the repository:

   * Open GitHub Desktop: **File** $\to$ **Clone repository...** $\to$ select your fork.

2. Install the required runtimes on your machine:

   * Python (version 3.10 or higher) with Jupyter notebook support.

   * Julia (version 1.9 or higher) with the Jupyter kernel installed via `using Pkg; Pkg.add("IJulia")`.

3. Open the folder in your code editor of choice (VS Code, JupyterLab, etc.) and select the appropriate Python or Julia kernel.

## 🛠️ Git Workflow & Submitting Solutions

All challenge solutions are submitted via standard GitHub Pull Requests (PRs):

```
# 1. Create a feature branch for your challenge
git checkout -b solve/notebook-02-rk4

# 2. Write your code and make sure tests/assertions pass
# (Do not commit temporary files or .ipynb_checkpoints)

# 3. Stage and commit your changes
git add Notebook-02-Dynamics/
git commit -m "feat(dynamics): complete RK4 chaotic pendulum challenge"

# 4. Push your branch to GitHub and open a Pull Request
git push origin solve/notebook-02-rk4

```

### Pull Request Guidelines

1. **One challenge per PR:** Keeps review diffs focused and easy for officers to test.

2. **Comment your physical reasoning:** Briefly explain why you picked a specific step size, boundary condition, or discretization method.

3. **Clean plots:** Make sure your plots have labeled axes, legends, and physical units.

## 🎖️ Discord Roles & Recognition

Merging approved PRs unlocks permanent contributor roles on the GMAPS Discord server:

| Tier | Role | Requirement | 
| ----- | ----- | ----- | 
| **Tier 1: Solver** | `@eigenbaby` | Solve and merge any challenge from **Notebook 01** (Python or Julia). | 
| **Tier 2: Practitioner** | `@rk4 demon` | Solve and merge at least 3 challenges across **Notebooks 02–04**. | 
| **Tier 3: Veteran** | `@hamiltonian menace` | Solve an advanced challenge (02.2 chaos, 02.3 quantum shooting, or 05.1 FFT). | 
| **Tier 4: Architect** | `@flight director` | Complete all 5 core notebooks or author an approved community challenge. | 

## 🏆 Community Challenges: Creating Your Own

Once you have completed the core curriculum or reached `@flight director` status, you are invited to design and publish **original computational challenges** for future members.

### How to Submit a Challenge

#### Option A: Add to an Existing Notebook (Notebooks 01–05)

If your challenge directly builds on an existing topic (e.g., adding an asymmetric spinning top to `Notebook-03` or a Duffing oscillator to `Notebook-02`):

1. Go to the relevant notebook folder.

2. Add a new section formatted as:

   `### Challenge [X.Y]: [Title] (Contributed by @YourGitHubHandle)`.

3. Include:

   * The theoretical context and governing physics equations written in LaTeX.

   * Starter scaffolding with clear `TODO` markers.

   * Assert-based test cases so students can verify their work.

   * A working reference solution.

#### Option B: Add to `Notebook-06-Advanced-Frontiers`

If your challenge covers advanced, cross-disciplinary, or specialized topics (e.g., General Relativity geodesics, Monte Carlo Ising models, N-body orbital mechanics, or lattice fluids):

1. Open `Notebook-06-Advanced-Frontiers/`.

2. Create a folder named `Challenge-[Topic-Name]/` containing:

   * `problem.ipynb` (starter challenge with scaffolding).

   * `solution.ipynb` (verified working solution).

   * `README.md` explaining the background physics and relevant papers or textbook references.

3. Open a Pull Request tagged with the `community-challenge` label.

4. Once reviewed and tested by an officer, it will be merged into the club curriculum with permanent attribution under your name.

## ⚖️ Academic Integrity & Honor Code

* **Understand the math:** Looking up formulas or asking for help is normal scientific practice; copying code from an LLM without understanding the numerical method will hurt you in upper-level courses.

* **Collaborate openly:** You are encouraged to work through problems together in the `#projects-and-code` Discord channel or during club meetings. If someone helps you fix a bug or derivation, credit them in your code comments.

* **Coursework Policy & The Past-Semester Rule:**

  * **The Rule:** You may **never** post, adapt, or share active, graded homework, lab, or exam assignments from courses.

  * **The Past-Semester Exception:** You **are permitted** to submit adaptations of your own original projects and code that were completed for GMU courses (e.g., PHYS 251, 325, 410), **provided the course was finished and graded at least one full semester ago.** Submissions must be your own work and adapted to fit the club's challenge format.

  * **Why This Rule Protects You:** This rule is in place specifically to keep you safe from honor code issues. Posting solutions or project code from an active class exposes you to automated plagiarism tools (like MOSS or Canvas checkers) if a classmate copies your public code. Enforcing a buffer of **at least one completed semester** ensures the class is finished, grades are finalized, and your public work cannot be used against you in an academic integrity inquiry.
