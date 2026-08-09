# Medical Imaging Data

> Historical entries are preserved from the original catalog. Some URLs or access models may have changed; verify each source before use.

## Core imaging datasets and archives

### MedPix
Database of medical images and teaching cases from the U.S. National Library of Medicine.

- Access: https://medpix.nlm.nih.gov/home
- `modality:imaging` `access:registration`

### ABIDE — Autism Brain Imaging Data Exchange
Structural and resting-state functional MRI data with phenotypic information for autism research.

- Paper: http://www.ncbi.nlm.nih.gov/pubmed/23774715
- Information: http://fcon_1000.projects.nitrc.org/indi/abide/
- Preprocessed: http://preprocessed-connectomes-project.org/abide/
- `modality:mri` `domain:autism` `access:registration`

### Alzheimer's Disease Neuroimaging Initiative (ADNI)
MRI plus clinical, genomic, biomarker and related Alzheimer's disease data.

- Access: http://adni.loni.usc.edu/data-samples/access-data/
- Paper: http://www.neurology.org/content/74/3/201.short
- `modality:mri` `domain:alzheimer` `access:registration`

### CT Colonography / Cancer Imaging Archive
CT data used for colon-polyp and colon-cancer imaging research.

- Historical catalog link: https://wiki.cancerimagingarchive.net/display/Public/CT+COLONOGRAPHY
- Current TCIA portal: https://www.cancerimagingarchive.net/
- `modality:ct` `domain:oncology`

### DRIVE — Digital Retinal Images for Vessel Extraction
Retinal images for comparative blood-vessel segmentation research.

- Paper: https://ieeexplore.ieee.org/document/1282003
- Historical access: http://www.isi.uu.nl/Research/Databases/DRIVE/download.php
- `modality:retinal-image` `task:segmentation`

### Cardiac Atlas resources
Historical catalog entries include:

- AMRG Cardiac Atlas
- Congenital Heart Disease (CHD) Atlas
- DETERMINE
- MESA
- SCMR Consensus Data
- Sunnybrook Cardiac Data

Historical access: http://www.cardiacatlas.org/studies/

### OASIS — Open Access Series of Imaging Studies
Cross-sectional and longitudinal brain MRI datasets spanning nondemented and demented participants.

- Access: https://www.oasis-brains.org/
- `modality:mri` `domain:neuroimaging`

### ISIC Archive — Skin lesion / melanoma
Large archive of skin-lesion images with diagnostic and segmentation metadata.

- Access: https://www.isic-archive.com/
- Historical downloader: https://github.com/GalAvineri/ISIC-Archive-Downloader
- `modality:dermatology-image` `task:classification` `task:segmentation`

### LIDC-IDRI — Lung Image Database Consortium
Thoracic CT resource for lung nodule detection, characterization and CAD evaluation.

- TCIA: https://www.cancerimagingarchive.net/collection/lidc-idri/
- `modality:ct` `domain:lung` `task:detection`

### TCIA Collections
Cancer imaging collections across diseases, anatomical sites and modalities.

- Access: https://www.cancerimagingarchive.net/
- `modality:imaging` `domain:oncology` `access:mixed`

### Belarus tuberculosis portal
Historical resource containing chest X-ray and CT imaging for tuberculosis cases.

- Historical access: http://tuberculosis.by/
- `modality:xray` `modality:ct` `domain:tuberculosis`

## Mammography

### DDSM — Digital Database for Screening Mammography
Approximately 2,500 mammography studies in the historical database with abnormality metadata and ground-truth regions.

- Historical access: http://marathon.csee.usf.edu/Mammography/Database.html
- `modality:mammography`

### INbreast
Digital mammography database with masses, calcifications, asymmetries and distortions; expert contours are provided.

- Historical access: http://medicalresearch.inescporto.pt/breastresearch/index.php/Get_INbreast_Database
- `modality:mammography` `task:segmentation`

### mini-MIAS
322 digitized mammograms with radiologist markings in the historical MIAS resource.

- Historical access: http://peipa.essex.ac.uk/info/mias.html
- `modality:mammography`

## Other specialized imaging resources

### I2CVB Prostate
Multiparametric MRI for prostate cancer computer-aided detection/diagnosis.

- Access: http://i2cvb.github.io/
- `modality:mri` `domain:prostate-cancer`

### eHealthLab datasets
Historical catalog included:
- MRI Lesion Segmentation in Multiple Sclerosis
- Emergency Tele-Orthopedics X-ray Digital Library
- IMT Segmentation
- Needle EMG MUAP Time Domain Features

Historical access: http://www.ehealthlab.cs.ucy.ac.cy/index.php/facilities/32-software/218-datasets

### DICOM sample sets
Historical OsiriX DICOM teaching/research files. The original catalog notes non-redistribution/commercial restrictions; verify current terms.

- Historical access: http://www.osirix-viewer.com/resources/dicom-image-library/
- `format:dicom` `access:restricted`

### SCR — Segmentation in Chest Radiographs
Chest radiograph segmentation of lung fields, heart and clavicles.

- Historical access: http://www.isi.uu.nl/Research/Databases/SCR/
- `modality:xray` `task:segmentation`

### VIA Group Public Databases
Historical lung CT public database resources.

- Historical access: http://www.via.cornell.edu/databases/

### CVonline Image Databases
General computer-vision image-database directory retained from the original catalog.

- Historical access: http://homepages.inf.ed.ac.uk/rbf/CVonline/Imagedbase.htm

### USC-SIPI Image Database
General image-processing dataset retained for historical completeness.

- Access: http://sipi.usc.edu/database/

### Histology registration dataset
108 histological image pairs with manually placed landmarks for image-registration evaluation.

- Historical access: http://cmp.felk.cvut.cz/~borovji3/?page=dataset
- `modality:histology` `task:registration`

## Historical medical image libraries

The original README also cataloged medical image/reference libraries, including:

- e-Anatomy
- Medical Pictures and Definitions
- Nucleus Medical Art
- UTHSCSA medical image database directory
- MedlinePlus surgery videos
- ADAM Medical Encyclopedia illustrations
- Hardin MD
- Health Education Assets Library (HEAL)
- CDC Public Health Image Library (PHIL)
- NLM Images from the History of Medicine
- Pozemedicale
- Old Medical Pictures
- Gray's Anatomy / Bartleby
- Crookston Collection
- DAVE Project
- Dermnet
- Interactive Dermatology Atlas
- Multi-Dimensional Human Embryo
- GastroLab Endoscopy Archives
- MedPix
- OBGYN.net Image Library

These are **image libraries/reference collections**, not necessarily ML-ready benchmark datasets. Verify licensing, availability and annotation quality before model training.

See also [Imaging Challenges](../benchmarks/imaging-challenges.md).
