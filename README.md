
# 📦 Robotic Arm Package Sorting Challenge

## Overview
This project simulates the ingestion, cleaning, and classification of package data for a robotic automation system, as part of the Thoughtful AI live coding challenge.

It focuses on processing real-world imperfect data — including missing, invalid, or inconsistent entries — to accurately classify packages according to predefined sorting criteria.

The main goals were:
- Handle and clean messy data gracefully.
- Apply sorting logic based on volume and mass thresholds.
- Generate clear outputs highlighting both successful classifications and detected errors.

---

## Problem Description
Customers submit CSV files describing their packages.  
Our robotic system must:
1. **Read** the package data.
2. **Clean** the dataset (handle missing or invalid values).
3. **Classify** each package into one of three categories: `STANDARD`, `SPECIAL`, or `REJECTED`.
4. **Report** results clearly and reliably.

---

## Sorting Rules
Each package is classified according to the following criteria:

- **Bulky**: Volume ≥ 1,000,000 cm³  
  (Volume = Width × Height × Length)  
  or any dimension (Width, Height, Length) ≥ 150 cm.
- **Heavy**: Mass ≥ 20 kg.

| Conditions                        | Classification |
|:----------------------------------|:---------------|
| Heavy **and** Bulky               | REJECTED       |
| Heavy **or** Bulky                | SPECIAL        |
| Neither Heavy nor Bulky           | STANDARD       |

---

## Approach
- **Manual data ingestion** from a CSV-like raw text string.
- **Error handling** for:
  - Duplicated headers
  - Missing fields
  - Invalid types (e.g., non-numeric values)
  - Negative dimensions or mass
- **Custom classification function** to assign sorting categories.
- **Separation** between valid processed entries and discarded rows with detailed error messages.

---

## Results
The script outputs:
- A list of successfully classified packages with original dimensions and assigned category.
- A detailed error log for invalid or discarded rows, indicating the reason for rejection.

---

## Potential Improvements
Given more time, I would enhance this solution by:
- Implementing a full statistical report: counts, percentages, and mass/volume distributions for each category.
- Using `pandas` for more efficient data ingestion and aggregation.
- Adding unit tests and validation pipelines for larger datasets.
- Improving scalability to handle very large files through batch processing.

---

## How to Run
Clone the repository and open the notebook:

```bash
git clone https://github.com/oscgonz19/interviews-code-exercises.git
cd interviews-code-exercises
jupyter notebook robotic_arm_package_sorting.ipynb
```

Alternatively, view the notebook directly via GitHub or Jupyter environments.

---

## File Structure
```
robotic_arm_package_sorting.ipynb    # Main notebook with the complete solution
README.md                           # Project overview and documentation
```

---

## Author
Oscar González  
*Candidate for Forward Deployed Engineer – Thoughtful AI*  
[LinkedIn Profile](https://www.linkedin.com/in/oscgonz19/) (optional)

---

# 🚀
