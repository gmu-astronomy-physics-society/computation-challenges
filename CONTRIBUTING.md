# Contributing to GMAPS Computational Challenges

Welcome! Whether you are completing your first Python/Julia challenge or designing a brand-new simulation for future members, we are glad to have you contributing to our chapter repository.

This repository is built to be practical and low-friction: everything can be run in the cloud via GitHub Codespaces or locally on your machine. Every merged Pull Request gives you an open-source contribution badge on your GitHub profile and unlocks permanent roles on our Discord server.

---

## 🧭 Table of Contents

1. [Ground Rules & Academic Integrity](#ground-rules--academic-integrity)
2. [Ways to Contribute](#ways-to-contribute)
3. [Environment Setup: Codespaces vs. Local](#environment-setup-codespaces-vs-local)
4. [Step-by-Step Git Workflow](#step-by-step-git-workflow)
5. [Code & Submission Standards](#code--submission-standards)
6. [Earning Discord Roles & Verification](#earning-discord-roles--verification)
7. [Authoring Community Challenges](#authoring-community-challenges)
8. [Getting Help](#getting-help)

---

## ⚖️ Ground Rules & Academic Integrity

Before diving in, please review our core integrity expectations:

* **Understand your code:** It is normal scientific practice to reference documentation, consult textbooks, or search for algorithm syntax. However, avoid pasting blind AI outputs or unvetted code into your branch. You should understand the physical equations and numerical methods you submit.
* **The Past-Semester Rule (Protecting Yourself):**
  * You may **never** post, adapt, or share active, graded homework, lab, or exam materials from current GMU courses.
  * You **are allowed** to submit adaptations of your own original project code from past Mason courses (e.g., PHYS 251, 325, 410), **provided the course was completed and graded at least one full semester ago.**
  * *Why this protects you:* This buffer is here strictly to keep you safe from honor committee inquiries. Automated plagiarism tools (such as MOSS or Canvas scrapers) flag public code if classmates look up answers to active assignments. Waiting a semester guarantees that grades are locked in and your work cannot be flagged.
* **Credit your peers:** If an officer or fellow student helped you debug a coordinate conversion or find a step-size error in Discord, credit them with a quick shoutout in your PR description or code comments.

---

## 🎯 Ways to Contribute

You do not have to finish the entire curriculum to make meaningful contributions:

* **Solve Challenges:** Work through notebooks in `Notebook-01-Foundations` through `Notebook-05-Signals-Fields`.
* **Fix Bugs & Typos:** Notice a broken equation in a markdown cell, a missing import statement, or an unclear instruction? Open a quick patch PR!
* **Author Original Challenges:** Completed the core notebooks or earned `@flight director`? Write a new challenge for the club curriculum.
* **Improve Infrastructure:** Help optimize our `.devcontainer` configuration, add automated test workflows, or expand documentation.

---

## 💻 Environment Setup: Codespaces vs. Local

You can work entirely in your browser or on your personal machine:

### Option A: GitHub Codespaces (Recommended)
* Click **Open in GitHub Codespaces** on the repo homepage or launch a codespace from your fork's `Code` dropdown.
* Python 3.11, Julia, and all core scientific libraries (`numpy`, `scipy`, `matplotlib`, `astropy`, `Plots.jl`, `IJulia`) are pre-installed.
* Launching takes under a minute, with zero local configuration required.

### Option B: Local Setup (GitHub Desktop / VS Code / Terminal)
* Clone your fork to your laptop:
  ```bash
  git clone https://github.com/<your-username>/computation-challenges.git
  cd computation-challenges
  ```
* Requirements:
  * Python $\ge 3.10$ with Jupyter notebook support (`pip install numpy scipy matplotlib astropy jupyter`).
  * Julia $\ge 1.9$ with `IJulia` installed (`using Pkg; Pkg.add(["IJulia", "Plots"])`).

---

## 🛠️ Step-by-Step Git Workflow

All submissions go through GitHub Pull Requests (PRs). If you are new to Git, follow these steps:

### 1. Fork and Branch
Never push directly to `main`. Create a descriptive branch for your work:

```bash
# Keep main clean
git checkout main
git pull origin main

# Create a feature branch for your challenge
git checkout -b solve/02.2-rk4-pendulum
```

### 2. Work on Your Notebook
* Open the challenge file in Jupyter or VS Code.
* Fill in the missing numerical logic, run all cells sequentially, and confirm test assertions pass.
* Make sure your plots render clearly with labeled axes and physical units.

### 3. Clean Up Before Committing
To keep our repository history clean and easy to review:
* Clear temporary variables or scratch cells.
* **Do not commit `.ipynb_checkpoints/`** or temporary OS files (`.DS_Store`).
* If your output files or datasets are excessively large ($>10\text{ MB}$), generate them at runtime rather than committing them.

### 4. Stage and Commit

Use clear, direct commit messages:

```bash
# Stage only the relevant notebook and support files
git add Notebook-02-Dynamics/02.2-chaotic-pendulum.ipynb

# Commit with a concise summary
git commit -m "feat(dynamics): implement RK4 solver and phase space plots"
```

### 5. Push and Open a Pull Request

```bash
git push -u origin solve/02.2-rk4-pendulum
```

* Go to the main GMAPS repository on GitHub and click **Compare & pull request**.
* Fill out the Pull Request template:
  * Reference which challenge or bug you worked on.
  * Briefly explain any design choices (e.g., choice of integration step size $h$ or boundary conditions).
  * Attach a screenshot of your resulting plot or simulation output.

---

## 📋 Code & Submission Standards

* **Language Choice:** Notebook 01 has separate `track-python/` and `track-julia/` directories. From Notebook 02 onward, you can solve challenges in either language.
* **Alternative Languages:** If you prefer C, C++, Rust, or Fortran, include a brief `WHY_AND_HOW.md` explaining why Python/Julia was insufficient for your specific calculation and providing standalone compilation commands with zero external dependencies.
* **Scope:** Keep PRs focused. Submit **one challenge per PR** so officers can review, test, and merge your work quickly.
* **Plotting Guidelines:**
  * Always label your axes with physical quantities and units (e.g., `Time (s)`, `Potential Energy (eV)`).
  * Include a title or legend whenever multiple curves are displayed.
  * Use accessible color palettes where possible.

---

## 🎖️ Earning Discord Roles & Verification

Once an officer reviews and merges your Pull Request, you unlock permanent roles on the GMAPS Discord server:

| Tier | Role | Trigger Condition |
| :--- | :--- | :--- |
| **Tier 1** | `@eigenbaby` | Merge any challenge from **Notebook 01** (Python or Julia). |
| **Tier 2** | `@rk4 demon` | Merge at least 3 challenges across **Notebooks 02–04**. |
| **Tier 3** | `@hamiltonian menace` | Solve an advanced challenge (02.2 chaos, 02.3 quantum shooting, or 05.1 FFT). |
| **Tier 4** | `@flight director` | Complete all core notebooks or author an approved community challenge. |

After your PR is merged, drop the link in `#projects-and-code` on Discord so an officer can assign your role!

---

## 🏆 Authoring Community Challenges

If you have completed the core notebooks or want to contribute a problem from your own computational research, we encourage you to publish a **Community Challenge**.

### Where to Place Your Challenge
* **Option A (Extension):** If your problem fits into an existing topic (e.g., adding an asymmetric top to `Notebook-03` or a Duffing oscillator to `Notebook-02`), add it directly to that folder as `Challenge [X.Y]: [Title]`.
* **Option B (Advanced Frontiers):** For cross-disciplinary or advanced research topics (e.g., N-body orbital integrators, relativistic ray-tracing, Monte Carlo Ising models), create a subfolder in `Notebook-06-Advanced-Frontiers/`:
  ```text
  Notebook-06-Advanced-Frontiers/
  └── Challenge-[Topic-Name]/
      ├── problem.ipynb       <-- Starter notebook with scaffolding & TODO markers
      ├── solution.ipynb      <-- Verified working reference solution
      └── README.md           <-- Background physics, derivations, and literature links
  ```

### Authoring Checklist
1. **Low Floor, High Ceiling:** Provide boilerplate code for data loading and plotting so students can focus on the physical derivations and algorithms.
2. **Clear Scaffolding:** Clearly mark sections where student code belongs with `# TODO: Implement ...` blocks.
3. **Automated Assertions:** Include `assert` tests (in Python) or `@test` macros (in Julia) so solvers receive immediate feedback when their code works.
4. **Physical Equations:** Write the theoretical background and governing equations cleanly in LaTeX markdown.

---

## ❓ Getting Help

Need help with a derivation, debugging an integration error, or getting Git set up?

* **Discord:** Ask in `#projects-and-code` or post scratch work in `#pset-debug`.
* **GitHub Issues:** Open an issue if you encounter an environment bug, dependency conflict, or error in the starter notebooks.
* **Officers:** Reach out to Isa Santos (`@President`) or Michael Young (`@Vice President`) on Discord or via campus email.
