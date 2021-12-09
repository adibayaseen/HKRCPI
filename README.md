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
Dataset can be downloaded from this link [https://github.com/adibayaseen/HemoNet/blob/main/Datasets.docx]<br/>
Seprate Hemolytic examples can be downloaded from here https://github.com/adibayaseen/HemoNet/blob/main/hemo_All_seq.txt<br/>
Non-hemolytic examples can be downloaded from here https://github.com/adibayaseen/HemoNet/blob/main/Nonhemo_All_seq.txt <br/>
External dataset from here https://github.com/adibayaseen/HemoNet/blob/b1291e5b378d1f11e9cf0dad407dc36fef26e806/HemolyticExternalwithNCmodification.txt <br/>
Clinical dataset from here https://github.com/adibayaseen/HemoNet/blob/0052f9f33e49db889d0c128a0e4a1453ae1da78e/DRAMP_Clinical_data.txt <br/>
## Code Structure
[weights.hdf ](https://github.com/adibayaseen/HemoNet/blob/main/weights.hdf)file have link of google drive in which neural network weights  of SeqVec features are stored <br/>
[5-foldResultsComparison.py](https://github.com/adibayaseen/HemoNet/blob/b000b4522c3a0b64109db32b3667047804ef12d4/5-foldResultsComparison.py) is used for 5-fold comparison with existing models and basline results.<br/>
[HemoNet10RunsResults](https://github.com/adibayaseen/HemoNet/blob/87270b7deeb05334e7c3ffe84476a56061b11229/HemoNet10RunsResults(%205-fold%20and%20Non-redundant).py)( 5-fold and Non-redundant) is used for HemoNet's all methods(5-fold and Non-redundant Cross-Validation Analysis)<br/>
[UMAP.py](https://github.com/adibayaseen/HemoNet/blob/b000b4522c3a0b64109db32b3667047804ef12d4/UMAP.py) file is used for visulaization of the data <br/>
[Clusterify.py](https://github.com/adibayaseen/HemoNet/blob/b000b4522c3a0b64109db32b3667047804ef12d4/Clusterify.py) used for making non-redendend clusters <br/>
[Final_Baseline_blaster_NN_5fold_cv_from_output_files.py](https://github.com/adibayaseen/HemoNet/blob/b000b4522c3a0b64109db32b3667047804ef12d4/Final_Baseline_blaster_NN_5fold_cv_from_output_files.py) used for Baseline Blast search <br/>
[Results.py](https://github.com/adibayaseen/HemoNet/blob/b000b4522c3a0b64109db32b3667047804ef12d4/Results.py) used for result in multiple runs(10)<br/>
## Generate predictions
Input File format <br/>
>Id_Nterminal_CTerminal<br/>
sequence<br/>
[Sample External data](https://github.com/adibayaseen/HemoNet/blob/447bc1f0253e9c1da4f9f9afee2728ca06de5be3/HemolyticExternalwithNCmodification.txt)<br/>
[Genearate_Prediction](https://colab.research.google.com/drive/1ihMYIuz_s3JlabfLcrd0o7PXSgeGAGQ9?usp=sharing) used for prediction of test file in given format<br/>
