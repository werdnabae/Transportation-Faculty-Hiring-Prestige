# Faculty Prestige and Academic Placement in Transportation Engineering

This repository contains data and code for a study of prestige stratification and faculty placement patterns within transportation focused civil and environmental engineering departments in the United States.

## Data

### `data_transportation_faculty.xlsx`

The Excel file contains two sheets:

**Sheet 1: `People`** - Primary analysis dataset. Each row is one faculty member.

| Column | Description |
|---|---|
| `Name` | Faculty member name (deidentified) |
| `Rank` | Current academic rank |
| `Current_Institution` | Current academic institution |
| `First_Hire` | Institution of first tenure-track appointment |
| `UG_Institution` | Undergraduate institution |
| `UG_Country` | Country of undergraduate training |
| `PhD_Institution` | PhD institution |
| `PhD_Country` | Country of PhD training |
| `PhD_Year` | Year PhD was awarded |
| `Postdoc_Institution` | Postdoctoral institution, if applicable |
| `Postdoc_Country` | Country of postdoctoral training |

**First-hire convention:** If `First_Hire` is blank, current institution is treated as the first hire.

**Sheet 2: `University Rankings`** - Institution-level prestige rankings used to construct tier classifications.

## Analysis

### `faculty_prestige_analysis.ipynb`

A Jupyter notebook that reproduces the main analyses and figures. The notebook is fully reproducible using the provided Excel file. It covers:

- the PhD-tier to first-hire-tier transition matrix, mobility summaries, and placement-concentration figures;
- the ordered logit models of first-hire prestige and the model-implied predicted probabilities;
- a robustness check under an alternative three-tier ranking scheme (manuscript Appendix A); and
- a cohort-stratified robustness check showing the prestige gradient is stable across doctoral completion cohorts, with a likelihood-ratio test for a PhD-tier by cohort interaction (manuscript Appendix B).

## Data Sources

- Data compiled from publicly available web sources as of January 2026
- Sample focuses on transportation oriented faculty within civil engineering departments
- Only tenure track academic placements are included

No private, proprietary, or confidential data are used.

## Reproducibility

All results can be reproduced using the anonymized dataset and analysis notebook. No proprietary data are used.

## License

This repository is released for research and academic use. Redistribution of the anonymized data is permitted with attribution.
