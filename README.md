# Visual-Inertial Navigation for Autonomous UAV Operation

This repository contains the LaTeX source code for the **Project Proposal** submitted to the Department of Computer Science and Engineering, University of Moratuwa.

## 📄 Project Overview
**Title:** Visual-Inertial Navigation for Autonomous UAV Operation in GPS-Restricted Environments  
**Supervisor:** Prof. Chandana Gamage  

**Group Members:**
- D. V. A. I. Delgahagoda
- T. T. Kashmeera
- K. D. R. P. Rathnayake

## 📂 Repository Structure
*   **`main.tex`**: The root LaTeX entry file.
*   **`sections/`**: Contains individual chapters (Introduction, Problem Statement, Methodology, etc.).
*   **`images/`**: Project graphics and figures.
*   **`references.bib`**: Bibliography data.
*   **`.github/workflows/`**: CI/CD automation scripts.

## 🤖 GitHub Actions Workflow
This project uses a GitHub Action to automatically compile the PDF when changes are pushed.

*   **Workflow File**: `.github/workflows/latex-compile.yml`
*   **Trigger**: Pushes and Pull Requests to the `main` branch.
*   **Action Used**: `xu-cheng/latex-action` (uses `latexmk` for compilation).
*   **Output**: The compiled PDF is uploaded as an Artifact named `Project-Proposal-PDF`.

### How to Download the PDF
1. Go to the **Actions** tab in this repository.
2. Click on the latest workflow run.
3. Scroll down to the **Artifacts** section and download `Project-Proposal-PDF`.

## 🛠 Local Build Instructions
To build the project locally, ensure you have a TeX distribution (TeX Live, MiKTeX) installed.

```bash
# Clean build with latexmk (recommended)
latexmk -pdf -pvc -interaction=nonstopmode main.tex

# Or manual compilation sequence
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```
