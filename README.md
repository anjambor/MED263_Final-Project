## MED263 - Final Project
This project aims to provide a tutorial on analyzing single-cell RNA sequencing data using the scanpy package. The tutorial is designed for users with basic Python and Jupyter Notebook knowledge.

## Background:
RNA sequencing can mostly be done in two ways: by sequencing the mixed RNA from the source of interest across cells (bulk sequencing) or by sequencing the transcriptomes of each cell individually (single-cell sequencing). Most of the time, mixing the RNA of all the cells is cheaper and easier than single-cell sequencing, which is expensive and hard to do. Bulk RNA-Seq gives cell-averaged expression profiles, which are generally easier to analyze but hide some important complexity. For example, some drugs may only affect certain types of cells or the way those cells communicate with each other. Even on cultured cells, it is hard to find these cells with simple bulk RNA-seq. So, looking at gene expression in a single cell is important to find these kinds of connections. Single-cell RNA-seq enables transcriptomic profiling at a single cell resolution, permitting the identification and characterization of different cell types in a bulk tissue sample, as well as the calculation of their relative abundance.

## Goals:
This tutorial aims to provide a step-by-step guide to analyzing single-cell human PBMCs using the scanpy package, from the processed/post-alignment count matrix to transcript expression analysis, clustering, covariate regression, and final publication-ready visualization generation.

## Prerequisites and Installation:
 Users should have a basic knowledge of Python 3 and Jupyter Notebook. Also, instructions for creating python environment are available on:    
 https://github.com/MED263-WI23/MED263_Intro/blob/main/Step4_Conda_JupyterNotebooks_Tutorial.md

However, you can follow the following steps to create a conda environment to perform the analysis too:       
- conda create --name env_name python==3.9   
- conda activate env_name   
- conda install pip    
- conda install -c anaconda jupyter    
- pip install --user ipykernel    
- python -m ipykernel install --user --name=env_name    

Then, the following python packages need to be installed using pip3 or conda: numpy, pandas, scanpy, and leidenalg.    
To install packages using pip3, use the following command:    
 - !pip3 install numpy    
 - !pip3 install pandas    
 - !pip3 install scanpy    
 - !pip3 install leidenalg    
 
 Alternatively, you can download them using conda:    
 - !conda install -c anaconda numpy    
 - !conda install -c anaconda pandas    
 - !conda install -c conda-forge scanpy    

## Usage:
The tutorial starts with loading the publicly available dataset representing 32,738 genes in 2,700 PBMCs using the datasets.pbmc3k() function and storing it in an Anndata structure. Then performs quality control steps, including filtering out low-quality reads. And finally proceeds with clustering and visualization of the data.

## Contributors:
This tutorial was created by Alex Jambor, Behrooz Mamandipoor, Hetsi Modi, and Avery Pong for MED263 Final Project.

## Acknowledgments
We thank the MED263 course instructors for their support and guidance throughout the winter quarter 2023.
