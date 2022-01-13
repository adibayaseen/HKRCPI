# HKRCPI
HKRCPI: Heterogeneous Kernel Representation for Compound-Protein Interaction Prediction 
A Heterogeneous Kernel-based method that perdict classification of a compound and protein pair as interacting or non-interacting.This network captures protein features and Circular Fingerprint repersatation of SMILES.
# Abstract

## Set Up Environment
```
python=3.6
conda install -c conda-forge rdkit
```
## Dataset
NR-HCPI Dataset can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/tree/main/Datasets/NR-HCPI]<br/>
External dataset from here https://github.com/adibayaseen/HKRCPI/blob/main/Datasets/BindingDB_m62021_top4000_1783000nM.txt <br/>
SuperDrugbank2 dataset from here https://github.com/adibayaseen/HKRCPI/blob/main/Datasets/approved_drugs_chemical_structure_identifiers.xlsx <br/>
## Supplementary Data
Supplementary data can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/blob/main/Supplementary%20data.docx]<br/>
## SARS-Cov2 Results
Median ranks along with names of top drugs predicted from our model can be downloaded from this link   [https://github.com/adibayaseen/HKRCPI/blob/main/ACE2%20and%20Spike%20Median%20Results%20Excluding%20Lightweight%20Compounds.xlsx]<br/>
## Code Structure
[Proposed model](https://colab.research.google.com/drive/1ihMYIuz_s3JlabfLcrd0o7PXSgeGAGQ9?usp=sharing) used for prediction of test file in given format<br/>) 
[Baseline SVM](https://colab.research.google.com/drive/1qMFqYPFBxeydNnf_NxGY5XS7AmWEmVcG?usp=sharing) 
[Product Kernel SVM](https://colab.research.google.com/drive/1o78nKbk3t-KjUniTxUHBOgY5QTzJjr85?usp=sharing)
[Validation over BindingDB](https://colab.research.google.com/drive/1IuX0taNfWNt0DttZ8eM4IwSrn2QRCXvd?usp=sharing)
[Dissimilarity Controlled Negative Examples generation](https://colab.research.google.com/drive/1IuX0taNfWNt0DttZ8eM4IwSrn2QRCXvd?usp=sharing) Dissimilarity Controlled Negative Examples generation and proposed method. 
[RFPP](https://colab.research.google.com/drive/1I-x5E7SxAwcepfC7zOD-2r9OnPGyEXLr?usp=sharing)
[RFPP with SuperDrug2](https://colab.research.google.com/drive/13TUFUGSpHsmw6qgK2MLd6pF2eaxHd6tD?usp=sharing)
## Generate predictions
Input File format <br/>
> SMILES of Compound Protein Sequence label<br/>
[Sample External data](https://github.com/adibayaseen/HemoNet/blob/447bc1f0253e9c1da4f9f9afee2728ca06de5be3/HemolyticExternalwithNCmodification.txt)<br/>
[Genearate_Prediction](https://colab.research.google.com/drive/1ihMYIuz_s3JlabfLcrd0o7PXSgeGAGQ9?usp=sharing) used for prediction of test file in given format<br/>
