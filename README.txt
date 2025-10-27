Overview
　　This repository accompanies the manuscript section titled:"Computational analysis of The Cancer Genome Atlas (TCGA) identified highly expressed miRNAs in breast cancer." The package provides a reproducible analysis workflow using Visual Studio Code. It includes:
1.A minimal Conda environment to ensure a consistent setup.
2.Example input data and expected output to verify the workflow.
3.A Jupyter Notebook that performs the analysis on miRNA expression data from TCGA.
Contents
1、README.txt (this file)
2、env/environment.yml (reproducible conda env)
3、code/cfDNA-tdd.ipynb (Jupyter notebook with analysis)
4、examples/example_input.csv (toy data to test the notebook)
5、examples/expected_output.txt (expected results on the toy data)
Quick Start
To get started with the analysis, follow these steps:
1.Install Visual Studio Code..
2.Create the Conda environment:
　　bash
　　conda env create -f env/environment.yml
　　conda activate tcga-mirna
3.Open the folder in Visual Studio Code and open the script code/cfDNA-tdd.py.
4.Set the DATA_PATH variable in the notebook to point to your TCGA data or use the provided toy dataset (examples/example_input.csv).
5.Run the notebook to generate summary tables and plots, and print the top miRNAs along with their normalized counts.
Example Data and Expected Output
1.examples/example_input.csv : toy counts for four miRNAs across two samples.
2.examples/expected_output.txt : the top-4 miRNAs and their toy normalized counts, to confirm the run.
Expected Top miRNAs on toy input:
(1)hsa-miR-143 ~ 6.2e4
(2)hsa-miR-182 ~ 2.95e4
(3) hsa-let-7a ~ 2.05e4
(4) hsa-miR-183 ~ 1.45e4
Data Availability
Real TCGA data are subject to TCGA/GDC access policies. 
Reproducibility Notes
The software versions are pinned in `env/environment.yml` for reproducibility. Random seeds are set within the notebook where applicable to ensure deterministic results. The analysis is deterministic given the same input dataset.