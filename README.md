## Quality Control Interface
Implementation of a graphical interface in a jupyter notebook for the annotation of 3D T1w brain MRI for the quality control of a clinical dataset.

This repository contains the jupyter notebook of the implementation described in Bottani et al. 2021 (full reference below) for the quality control of 3D T1w brain MRI.

#### Dependencies
- Python 3.6.2
- ipywidgets 
- numpy
- pandas
- nibabel
- matplotlib
- nilearn


#### Input necessary
- CAPS folder: It contains preprocessed images in the MNI space (See `clinica run t1-linear` from www.clinica.run)
- PNG folder: where central slice of the 3D T1w brain MRI will be saved
- participants tsv: tsv file containing participant id and session id of the image
- output file: txt file containing labeled images


#### How it works
The code produces a screenshot of the central slice of the 3D T1w brain MRI. The user can annotate 5 different characteristics:
- `r`: the image is not a complete 3D T1w brain MRI
- `k`: if the image is injected with gadolinium
- `a`: some motion, `aa` severe motion
- `z`: medium contrast, `zz` bad contrast
- `d`: some noise, `dd`severe noise

The graphical interface allows to come back to the choice to label again an image and it automatically saves each input. 
The final label is automatically calculated (see Bottani et al. 2021 for more details)

#### Final output
Txt file containing the code assigned by the user and the final label for each image

## Citing this work

> S. Bottani, N. Burgos, A. Maire, A. Wild, S. Ströer, D. Dormont, O. Colliot, the APPRIMAGE Study Group, **Automatic quality control of brain T1-weighted magnetic resonance images for a clinical data warehouse**, Medical Image Analysis, 2022, vol. 75, p. 102219. 
