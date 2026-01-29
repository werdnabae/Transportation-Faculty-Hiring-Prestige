# Faculty Prestige and Academic Placement in Transportation Engineering

This repository contains data and code for a study of prestige stratification and faculty placement patterns within transportation focused civil and environmental engineering departments in the United States.

The project links doctoral training institutions to first academic placements and analyzes how prestige tiers shape hiring outcomes across the academic labor market.

## Data Description
### `data_transportation_faculty.xlsx`

The Excel file contains **two sheets**:

#### Sheet 1: `People`
This is the **primary analysis dataset**.  
Each row corresponds to a single faculty member in the sample.

Variables include:

| Column | Description |
|------|------------|
| `Name` | Faculty member name (deidentified)|
| `Rank` | Current academic rank (e.g., Assistant, Associate, Full) |
| `Current_Institution` | Faculty member’s current academic institution |
| `First_Hire` | Institution of first tenure-track academic appointment |
| `UG_Institution` | Undergraduate degree granting institution |
| `UG_Country` | Country of undergraduate training |
| `PhD_Institution` | PhD degree granting institution |
| `PhD_Country` | Country of PhD training |
| `PhD_Year` | Year PhD degree was awarded |
| `Postdoc_Institution` | Postdoctoral institution, if applicable|
| `Postdoc_Country` | Country of postdoctoral training |

**First-hire convention:**  
If `First_Hire` is blank, the faculty member’s **current institution is treated as their first hire institution**. This reflects cases where no prior tenure-track appointment could be identified from public records.

This sheet is the sole input used for faculty-level placement analyses.

**Postdoc columns:**
Postdoctoral training is recorded only when explicitly identified as a postdoctoral appointment in public records. Other intermediate roles, including research scientist, visiting, or non tenure track research faculty positions, are not coded as postdoctoral training. 

Multiple postdoctoral appointments are separated by a "+"

---

#### Sheet 2: `University Rankings`
This sheet contains **institution-level prestige information** used to construct prestige tiers and comparative rankings.

It includes mappings from university names to prestige indicators used in the analysis (e.g., tier classifications or ranking groupings). These rankings are merged with the `People` sheet within the analysis notebook to compute prestige transitions and placement concentration measures.

This sheet does not represent individuals and contains no faculty-level records.


## Analysis Notebook

### `faculty_prestige_analysis.ipynb`
A Jupyter notebook that reproduces the main analyses and figures in the paper, including:

- Prestige tier construction and validation  
- Placement transition matrices  
- Placement concentration metrics by PhD institution  
- Summary statistics and visualizations  

The notebook is designed to be fully reproducible using the provided Excel file.

## Data Sources and Scope

- Data are compiled from publicly available web sources as of January 2026  
- The sample focuses on transportation oriented faculty within civil engineering departments  
- Only tenure track academic placements are included in the primary analyses  

No private, proprietary, or confidential data are used.


## Reproducibility

All results in the associated paper can be reproduced using the anonymized dataset and analysis notebook in this repository. No proprietary or confidential data are used.

## License

This repository is released for research and academic use. Redistribution of the anonymized data is permitted with attribution.