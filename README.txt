TCGA miRNA Analysis – Code and Reproducibility Package

Overview
This repository accompanies the manuscript section titled:
  "Computational analysis of The Cancer Genome Atlas (TCGA) identified highly expressed miRNAs in breast cancer."
  The package provides a reproducible analysis workflow using Jupyter Notebooks. It includes:
  A minimal Conda environment to ensure a consistent setup.
  Example input data and expected output to verify the workflow.
  A notebook that performs the analysis on miRNA expression data from TCGA.

Contents
　　README.txt (this file)
  env/environment.yml (reproducible conda env)
  code/cfDNA-tdd.ipynb (notebook with analysis)
  examples/example_input.csv (toy data to test the notebook)
  examples/expected_output.txt (expected results on the toy data)

Quick Start
To get started with the analysis, follow these steps:
  1. Install Conda (Miniconda or Anaconda).
  2. Create the Conda environment: bash
  conda env create -f env/environment.yml
  conda activate tcga-mirna
  3. Open the notebook:
  bash
  notebook code/cfDNA-tdd.ipynb
  4. Set the `DATA_PATH` variable in the notebook to point to your TCGA data or use the provided toy dataset (`examples/example_input.csv`).
  5. Run the notebook to generate summary tables and plots, and print the top miRNAs along with their normalized counts.

Example Data and Expected Output
　　examples/example_input.csv : toy counts for four miRNAs across two samples.
　　examples/expected_output.txt : the top-4 miRNAs and their toy normalized counts, to confirm the run.
　　
Example Data and Expected Output
　　Example Input: `examples/example_input.csv` contains toy data with four miRNAs across two samples.
  Expected Output: `examples/expected_output.txt` lists the top-4 miRNAs and their normalized counts from the toy dataset:

  Expected Top miRNAs on toy input:
  1. hsa-miR-143 ~ 6.2e4
  2. hsa-miR-182 ~ 2.95e4
  3. hsa-let-7a ~ 2.05e4
  4. hsa-miR-183 ~ 1.45e4

Data Availability
　　Real TCGA data are subject to TCGA/GDC access policies. Provide instructions or scripts to download public-level miRNA quantification from GDC (or include DOIs/DRS IDs if controlled). The notebook expects a table with miRNA IDs and normalized counts (e.g.,RPM/CPM/DESeq2-normalized).
　　
Reproducibility Notes
　　The software versions are pinned in `env/environment.yml` for reproducibility.
  Random seeds are set within the notebook where applicable to ensure deterministic results.
  The analysis is deterministic given the same input dataset.

Reproducibility Notes
　　Software versions are pinned in env/environment.yml.
　　Random seeds are set in the notebook where applicable.
　　The analysis is deterministic for a given input table.