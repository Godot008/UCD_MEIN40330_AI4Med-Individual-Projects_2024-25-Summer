# AI for Personalised Medicine Individual Project

[![CRAN](https://img.shields.io/badge/CRAN-4.4.2+-green.svg)](#) [![Python](https://img.shields.io/badge/python-3.10-blue.svg)](#)

> This is my complete individual project for the AI for Personal Medicine course, which consists of three sub-projects: the ML mini-project, the modelling project, and the group project.
> 
> **Mechine Learning**, **Kaplan-Meier survival analysis**, **p53 model**, **signaling pathway**, **Transformer**

---

## Project Object

- **ML Mini Project**

    This project aims to realize personalized medicine through the integration of omics and clinical data and the exploration of machine learning applications, thereby supporting precision oncology and enhancing the potential for improved patient outcome prediction. Specifically, the project aims to:
    - Formulate a research question that can be addressed by analyzing and integrating omics and clinical datasets.
    - Obtain, preprocess, and integrate multiple data types to ensure meaningful cross-dataset comparisons.
    - Perform feature selection to identify informative sets of genes or proteins that may serve as biomarkers.
    - Apply complementary analytical approaches, including both unsupervised (e.g., clustering, subtype discovery) and supervised methods (e.g., classification, survival analysis), to uncover patterns and their association with clinical outcomes.
    - Integrate data and results, linking molecular signatures with patient characteristics and clinical endpoints to provide insights into disease mechanisms and potential treatment strategies.

- **Modelling Project**

    This project is dedicated to evaluating and expanding mechanistic p53 signaling models within the context of precision medicine. By integrating mechanistic modeling with data-driven artificial intelligence approaches, it aims to deepen our understanding of p53's role in cancer progression, therapeutic response, and potential pathways for therapeutic targeting. The primary goals are:
    - Predicting Patient Survival – Assess whether the p53 model can stratify patients based on survival outcomes using TCGA clinical and genomic datasets.
    - Drug Response Prediction – Investigate if the model can predict cell line responses to DNA-damaging agents by integrating data from CCLE and GDSC drug sensitivity screens.
    - Model Refinement – Explore potential improvements of the p53 model, such as the inclusion of additional regulatory genes or pathways, based on insights from data-driven analysis.
    - Benchmarking Against Machine Learning – Compare the predictions of the mechanistic p53 model with machine learning approaches (e.g., regression models, deep learning) to evaluate predictive performance and interpretability.

- **Group Project**

    This project forms part of University College Dublin's “Artificial Intelligence for Personalised Medicine” programme, aiming to explore computational strategies for precision oncology by integrating machine learning and systems biology approaches to support more effective and personalised cancer treatments. Its primary objective is to utilise multi-omics and pharmacogenomics datasets:
    - Build predictive models of patient response across different datasets, addressing challenges of data heterogeneity and completeness.
    - Develop predictors of cell viability under standard-of-care drug treatments and evaluate their correlation with patient-level predictions.
    - Investigate mechanistic modeling approaches, such as ordinary differential equation (ODE) models, to capture dynamic cellular processes.
    - Identify novel therapeutic targets using large-scale resources like LINCS and DepMap.
    - Propose treatment strategies by comparing the potential of chemotherapy, immunotherapy, and other modalities, guided by data-driven insights.

## Quick Start

### Overall Project Directory Structure

The complete directory structure is as follows:

```bash
ai4med_individual_project/
        ├─ ml_mini_project/
        │  ├─ ml_mini_project_work.qmd          # Project source files (Quarto document format)
        │  └─ ml_mini_project_work.pdf          # Project file after rendering the project source file
        ├─ modelling_project/
        │  ├─ p53_model_updated.ipynb           # Updated p53 model source file provided by the lecturer
        │  ├─ p53_parameters_summaryTable.txt   # p53 model dependent parameter file
        │  └─ modelling_project_work.ipynb      # Modelling project source file (Jupyter notebook format)
        ├─ group_project/
        │  ├─ question_2.ipynb                  # Project source files
        │  └─ question_4.ipynb
        ├─ LICENSE                              # This project employs a custom licence; for details, see LICENCE
        └─ README.md
```

### Create Running Environment

In this overall project, I used two different programming languages to address the tasks. For the ML mini-project, I used a Quarto document with the R language. The easiest way to set up the runtime environment for reproducing this work is to use the standard official combination: [the Comprehensive R Archive Network (CRAN)](https://cran.r-project.org/mirrors.html) together with [RStudio](https://posit.co/download/rstudio-desktop/). Since the ML mini-project only relies on regular R packages, it can be reproduced with any CRAN version. (For reference, I developed the project using CRAN `4.4.2`. If you want rigorous reproducibility, you may follow this version.)

For the modelling project and the group project, I used Jupyter Notebooks with the Python language. I recommend using Conda/Anaconda together with Visual Studio Code as the IDE for running or debugging the Jupyter Notebook code. I have not tested other environments, but if you are familiar with them, you may also set up and run the notebooks by following the instructions. Below, I demonstrate how to configure the environment using my recommended setup:

To reproduce the project results, you first need to have a Conda environment installed (if not, see the [Conda official documentation](https://docs.conda.io/projects/conda/en/stable/) for installation instructions). Then, if you want to reproduce the modeling project, run the following shell commands to create an environment suitable for executing the Jupyter Notebook code (I also included these commands in the notebook for reference):

```bash
(base) user@device ai4med_individual_project % conda create -n afpm-lab-env python=3.10 -y
(base) user@device ai4med_individual_project % conda activate afpm-lab-env
(afpm-lab-env) user@device ai4med_individual_project % pip install numpy pandas scipy matplotlib lifelines openpyxl
```

If you want to reproduce the group project, please use the following shell commands, the same as in the modeling project.

```bash
(base) user@device ai4med_individual_project % conda create -n afpm-lab-env python=3.10 -y
(base) user@device ai4med_individual_project % conda activate afpm-lab-env
(afpm-lab-env) user@device ai4med_individual_project % pip install pandas torch scikit-learn numpy matplotlib cmapPy
```

After creating the environment, simply open the Jupyter Notebook in Visual Studio Code and select the Python environment `afpm-lab-env` that you just created as the interpreter. You can then run the notebook code cell by cell.
