# PMUY Clean-Fuel Adoption — Causal DiD Analysis (ECO 6810)

## Project Overview
This project evaluates the impact of the Pradhan Mantri Ujjwala Yojana (PMUY) on clean cooking fuel adoption across Indian states.

Using NFHS-4 (2015–16) and NFHS-5 (2019–21) data, we implement a Difference-in-Differences (DiD) design comparing high-exposure (low baseline access) and low-exposure states.

---

## Data Sources

- **NFHS-4 & NFHS-5 Household Data**
  - We have attached it in the data folder :[PMUY Data](https://github.com/Neha10000/PMUY-final-project-project/blob/main/data/pmuy_data_compressed.csv.gz)
  - Used to construct clean fuel adoption variable (`hv226`)

- **PPAC PMUY Data**
  - Used for validation of exposure classification

---

## Methodology

- Outcome: Clean fuel usage (binary, derived from `hv226`)
- Treatment: `high_exposure = 1` for states below NFHS-4 median clean fuel access
- Design: Difference-in-Differences (DiD)

Baseline metric:
- Naive DiD estimate of clean fuel adoption change

---

## How to Run (Milestone — Official Method)

Clone the repository:

```
git clone https://github.com/tanisha0710-ui/PMUY-AI.git
cd PMUY-AI
```

Run the milestone pipeline:

```
uv run main.py --milestone
```

---

## Alternative (Colab — Used by Team)

This project was developed and tested in Google Colab.

Steps used:

1. Clone the repository:
```
%cd /content
!rm -rf PMUY-final-project-project
!git clone https://github.com/Neha10000/PMUY-final-project-project.git
%cd PMUY-final-project-project

```

2. Install:
```
!pip install uv -q
!uv sync
```


3. Run the pipeline:
```
!uv run main.py
```
4. Check:
```
!echo "=== GREP CHECK ===" 
!grep -r "replace_me\|is_template.*true\|blocked\|Template outputs written" \
    --include="*.py" --include="*.md" --include="*.json" . \
    || echo "CLEAN"
```


## Outputs

Running the pipeline generates:

```
outputs/baseline_metric.json
outputs/milestone_manifest.json
outputs/primary_metric.json
```

---

## Data Probe

A data probe confirming access to NFHS data is provided in:

```
artifacts/probes/pmuy_probe.md
```

---

Note- We have attached the pdf for codes and output(colab) under folder Notebook with file - [FINAL_Test.Repo.ipynb-Colab.pdf](https://github.com/Neha10000/PMUY-final-project-project/blob/main/notebooks/FINAL_Test.Repo.ipynb%20-%20Colab.pdf).

This shows our previous changes - {This is based on our final milestone data file which we have uploaded in the data folder as [pmuy_data_compressed.csv.gz](https://github.com/Neha10000/PMUY-final-project-project/blob/main/data/pmuy_data_compressed.csv.gz)
This is our final colab file .We have attached the pdf for codes and output
(colab) under folder Notebook with file - [Test_Repo_Final.ipynb-Colab.pdf](https://github.com/Neha10000/PMUY-final-project-project/blob/main/notebooks/Test_Repo_Final.ipynb%20-%20Colab.pdf)
. This pdf shows how we added the results fom Colab to Github 

The below represents the test files we had for our csv file taken from google drive(using gdown: which could not reproduce the entire repo for review.)
-This is our old colab file {We have attached the pdf for codes and output
(colab) under folder Notebook with file - [Test_Repo.ipynb-Colab.pdf](https://github.com/Neha10000/PMUY-final-project-project/blob/main/notebooks/Test_Repo.ipynb%20-%20Colab.pdf) 
. Also this pdf shows how we added the results fom Colab to Github 
Now, this is is our updated file (it includes colab codes that we used to run our codes and ity also has the output for the same ) and we have added it under folder notebook named [Test_Repo_2.ipynb-Colab.pdf](https://github.com/Neha10000/PMUY-final-project-project/blob/main/notebooks/Test_Repo_2.ipynb%20-%20Colab.pdf)}

## Team

- Tanisha Aggarwal  
- Neha Rana  
- Jaswathi Lalitha R  

