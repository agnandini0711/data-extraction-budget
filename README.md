# Data Extraction from Government Budget PDF

## Overview

This project extracts structured financial data from a government budget PDF using R.

The goal is to convert unstructured PDF tables into clean, analysis-ready datasets.

---

## Dataset

* Source file: `Gr09.pdf`
* Contains financial data for the Energy Department (Budget 2024–25)

---

## Objectives

* Extract tabular data from PDF
* Clean and standardize messy text (Hindi + numeric data)
* Structure data into tidy formats
* Export final datasets as CSV files

---

## Pages Extracted

### Page 3 – Division of Grant

* Major heads (2045, 2049, etc.)
* Revenue and Capital breakdown
* Voted / Charged classification

Outputs:

* `division_of_grant_wide.csv`
* `division_of_grant_long.csv`

---

### Page 6 – Other Taxes and Duties

* Item-level expenditure (Salary, Travel, etc.)
* Extracted using text parsing

Output:

* `other_taxes_final.csv`

---

## Tools and Libraries

* R
* tabulapdf
* pdftools
* dplyr
* stringr
* tidyr
* readr

---

## Methodology

1. Extract tables from Page 3 using `tabulapdf`
2. Clean and correct broken Hindi text
3. Extract numeric values and structure dataset
4. Convert data into:

   * Long format (tidy)
   * Wide format (report-ready)
5. Extract Page 6 using `pdf_text()` and regex
6. Map item codes to Hindi and English descriptions
7. Export final datasets as CSV

---

## Outputs

| File                       | Description                 |
| -------------------------- | --------------------------- |
| division_of_grant_wide.csv | Summary in wide format      |
| division_of_grant_long.csv | Tidy long format            |
| other_taxes_final.csv      | Item-level expenditure data |

---

## How to Run

1. Clone this repository
2. Place `Gr09.pdf` in the project folder
3. Open `Data-Extraction-from-Government-Budget-PDF.Rmd`
4. Click Knit (HTML)
5. Output CSV files will be generated automatically

---

## Result

* Successfully extracted structured data from PDF
* Clean and consistent datasets generated
* Fully reproducible workflow using R Markdown

---

## Notes

* Some preprocessing was required to fix encoding issues in Hindi text
* Missing values (`--`) were handled and converted appropriately
* Warnings/messages suppressed for clean output

---

## Author

Nandini Agarwal

---

## Submission

This repository contains:

* R Markdown file (code + output)
* Extracted CSV datasets
* Source PDF
* README documentation
