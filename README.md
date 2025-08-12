Data Availability:
This repository does not contain patient-level data due to privacy restrictions.
The provided code is intended to be run on local datasets matching the input format described in data/README.md.

# Kaplan-Meier Survival Plot for DLI Study

This repository contains code to generate Kaplan-Meier survival plots for patients receiving donor lymphocyte infusion (DLI) after allogeneic stem cell transplantation. It includes overall survival analysis, subgroup comparisons (e.g., by diagnosis or DLI type), and displays a number-at-risk table below the curves.

## Features

- Reads clinical data from Excel files
- Computes and plots Kaplan-Meier curves using `lifelines`
- Adds median survival time lines
- Displays number-at-risk tables for subgroups
- Exports high-resolution TIFF images for publication

## Files

- `Preemptive_vs_Therapeutic_DLI.ipynb`: Jupyter Notebook containing all code and visualizations
- `requirements.txt`: Required Python packages
- `LICENSE`: MIT License for open sharing and reuse

## Example Output

The notebook generates plots such as:

- Overall survival curve with number at risk
- Kaplan-Meier curves by diagnosis (AML, sAML, MDS, ALL)
- Comparison of preemptive vs. therapeutic DLI strategies

## Installation

Clone the repository and install dependencies via:

```bash
pip install -r requirements.txt
```

## Data Input

Make sure your Excel file includes the following columns:
- `Time` or `DLI to FU` (time from DLI to last follow-up)
- `Death Status` (1 = event occurred, 0 = censored)
- `Diagnosis` (optional, coded as 0 = AML, 1 = sAML, 2 = MDS, 3 = ALL)
- `Preemptive vs. Therapeutic` (optional: 0 = preemptive, 1 = therapeutic)

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

Dr. Alexander Angleitner  
University Medical Center Göttingen  
