
# Insights into performance evaluation of compound-protein interaction prediction methods 
# HKRCPI
HKRCPI: Heterogeneous Kernel Representation for Compound-Protein Interaction Prediction
A Heterogeneous Kernel-based method that perdict classification of a compound and protein pair as interacting or non-interacting.This network captures protein features and Circular Fingerprint repersatation of SMILES.
# Abstract
Abstract
Motivation:
Machine learning based prediction of compound-protein interactions (CPIs) is important for drug design, screening and repurposing studies and can improve the efficiency and cost-effectiveness of wet lab assays. Despite the publication of many research papers reporting CPI predictors in the recent years, we have observed a number of fundamental issues in experiment design that lead to over optimistic estimates of model performance.
Results:
In this paper, we analyze the impact of several important factors affecting generalization perfor-mance of CPI predictors that are overlooked in existing work:
1.	Similarity between training and test examples in cross-validation
2.	The strategy for generating negative examples, in the absence of experimentally verified negative examples.
3.	Choice of evaluation protocols and performance metrics and their alignment with real-world use of CPI predictors in screening large compound libraries.
Using both an existing state-of-the-art method (CPI-NN) and a proposed kernel based approach,
we have found that assessment of predictive performance of CPI predictors requires careful con-trol over similarity between training and test examples.  We also show that random pairing for gen-erating synthetic negative examples for training and performance evaluation results in models with better generalization performance in comparison to more sophisticated strategies used in existing studies. Furthermore, we have found that our kernel based approach, despite its simple design, exceeds the prediction performance of CPI-NN.  We have used the proposed model for compound screening of several proteins including SARS-CoV-2 Spike and Human ACE2 proteins and found strong evidence in support of its top hits.

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
* Comparative results for different Kernels can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/blob/main/Supplementary%20data.docx]<br/><br/>
* Experimental setup for screening with Non-redundant Cross-validation (NRCV) or Screening SuperDRUG2 can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/blob/main/Supplementary%20data.docx]<br/><br/>
* Experimental setup for RFPP calculation can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/blob/main/Supplementary%20data.docx]<br/> <br/>
* Comparison of non-redundant cross-validation (CV) results of our proposed model with previous method CPI-NN using 40% redundancy removal  can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/blob/main/Supplementary%20data.docx]<br/><br/>
* Target Compound Screening (TCS) for Drugreprurposing RFPP for  the test set for CPINN and our proposed model results comparison can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/blob/main/Supplementary%20data.docx]<br/><br/>
* Target Compound Screening (TCS) for Drugreprurposing scores for all pairs of proteins in the test set for one fold can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/blob/main/Supplementary%20data.docx]<br/><br/>
* RFPP of TCS proteins in the test fold (RFPP of protein whos all pair scores mentioned in the previous file can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/blob/main/Supplementary%20data.docx]<br/><br/>
Supplementary data can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/blob/main/Supplementary%20data.docx]<br/>
* SARS-Cov2 Results and Supporting Evidence can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/blob/main/Supplementary%20data.docx]<br/>
* SARS-Cov2 all results with top 100 predictions from our model can be downloaded from this link [https://github.com/adibayaseen/HKRCPI/blob/main/Supplementary%20data.docx]<br/>
* SARS-Cov2 Median ranks for ACE2 and Spike proteins along with names of top drugs predicted from our model can be downloaded from this link   [https://github.com/adibayaseen/HKRCPI/blob/main/ACE2%20and%20Spike%20Median%20Results%20Excluding%20Lightweight%20Compounds.xlsx]<br/>
## Code Structure
[Proposed model](https://colab.research.google.com/drive/1mkAFLcYeHQED0p2qvn92178cmlO9SEIP?usp=sharing) used for prediction of test file in given format<br/>
[Baseline SVM](https://colab.research.google.com/drive/1qMFqYPFBxeydNnf_NxGY5XS7AmWEmVcG?usp=sharing) used for baseline results.<br/> 
[Product Kernel SVM](https://colab.research.google.com/drive/1o78nKbk3t-KjUniTxUHBOgY5QTzJjr85?usp=sharing)used for experimental setup of product kernel.<br/> 
[Validation over BindingDB](https://colab.research.google.com/drive/1nK30uc0DxGjXqXUDQsvGyDT3DDnUzaxE?usp=sharing) used for validation over experimentally verified negative examples from Binding DB  <br/> 
[Dissimilarity Controlled Negative Examples generation](https://colab.research.google.com/drive/1IuX0taNfWNt0DttZ8eM4IwSrn2QRCXvd?usp=sharing) Dissimilarity Controlled Negative Examples generation and proposed method. <br/>
[RFPP](https://colab.research.google.com/drive/1I-x5E7SxAwcepfC7zOD-2r9OnPGyEXLr?usp=sharing) Screening with Non-redundant Cross-validation (NRCV) where we train a model using training folds of the NRCV dataset and then compute prediction scores of all-vs-all compound-protein pairs in the test fold using the trained model (see supplementary information file for an illustration) and rank of first positive pair (RFPP) is calculated<br/>
[RFPP with SuperDrug2](https://colab.research.google.com/drive/13TUFUGSpHsmw6qgK2MLd6pF2eaxHd6tD?usp=sharing) used for drug-repurposing analysis with the proposed model, we used the SuperDRUG2 dataset containing 3,633 FDA-approved drugs. In this experiment, a CPI model is first trained on all examples in training folds of the NRCV dataset and then used to generate prediction scores for all proteins in the test fold paired with all compounds in the SuperDRUG2 database (see supple-mentary material for an illustration of the experimental setup).  <br/>
## Generate predictions
Input File format <br/>
> SMILES of Compound Protein Sequence label<br/>
[Sample input data](https://github.com/adibayaseen/HKRCPI/blob/0f1153be22c4ce6235259bef8cff1dd820e69a39/Sample%20Data)<br/>
[Genearate_Prediction](https://colab.research.google.com/drive/18576Mvg2tHovQweM3LD9Hkj68MSzZoO9?usp=sharing) used for prediction of test file in given format<br/>
