# Thoughtful AI – Technical Screen

This repository contains the solution to the technical challenge from **Thoughtful AI** for the **Forward Deployed Engineer** role.

## Objective

Implement a function that classifies packages as `STANDARD`, `SPECIAL`, or `REJECTED` based on their physical properties. The logic simulates the decision-making process of a robotic arm in an automated dispatch system.

---

## Classification Rules

A package is considered:

- **Bulky** if its volume is ≥ 1,000,000 cm³  
  or if **any dimension** (width, height, or length) is ≥ 150 cm  
- **Heavy** if its mass is ≥ 20 kg

Final classification logic:

- `REJECTED`: if the package is both **bulky** and **heavy**
- `SPECIAL`: if it is either **bulky** or **heavy** (but not both)
- `STANDARD`: if it is neither bulky nor heavy

---

##  Tech Stack

- Python 3
- Jupyter Notebook (`.ipynb`)
- Google Colab compatible

---

## How to Run

### Option 1: Run in Google Colab

Click the badge below to launch the notebook directly in Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/oscgonz19/thoughtful-ai-tech-screen/blob/main/solution.ipynb)

---

### Option 2: Run Locally

```bash
git clone git@github.com:oscgonz19/thoughtful-ai-tech-screen.git
cd thoughtful-ai-tech-screen
