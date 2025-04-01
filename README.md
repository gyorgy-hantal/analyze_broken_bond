## <center> Broken or not_broken? </center>

## A set of python based tools to identify and train a ML model predicting bond breakage in molecular simulation of a strained epoxy polymer.

The current version considers only C-S bonds ("ca-sy") in sulfone groups (R-S(O2)-R') as it is found more prone to breake than any other bonds.

All configurations are taken from classical molecular dynamics simulations of an epoxy network made by crosslinking the DGEBA monomer with the amine-based DDS crosslinker.    

![fig](https://github.com/user-attachments/assets/12c42754-6354-4be2-89c2-19cf614cf50a)

The configurations are in GAUSSIAN's input file format prepared for QM/MM calculations. Every configuration was tested a priori at the QM/MM level to obtain a label "broken" or "not_broken".

This python script attempts to correlate a big bunch of structural descriptors, or "collective variables" (CVs), with the final label of the configuration to propose a ML model that predicts the label using only the CVs found relevant (and thus save a lot of compute time in the future when performing fracture simulations).

Requirements: 
```
python==3.9.6
numpy==1.26.4
mdtraj==1.10.3
matplotlib==3.9.1.post1
```
