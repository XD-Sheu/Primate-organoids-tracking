## Primate Cortical Organoid Time-Lapse Tracking

This repository contains trained machine learning models, cell tracking datasets, and metadata derived from two-month continuous time-lapse recordings of primate (human and chimpanzee) cortical organoids. 

To accommodate the coarse imaging intervals (30–50 minutes) required to minimize phototoxicity during long-term recording, cell lineage tracking was performed using the [ELEPHANT](https://github.com/elephant-track) platform. 
Models were generated via incremental deep learning and rounds of manual proofreading to ensure a relatively unbiased lineage mapping.

## Repository Contents

* *`*.pth` (Trained Models):* Fully trained 3D U-Net convolutional neural network weights for nuclear detection and optical flow estimation, optimized specifically for longitudinal organoid time-lapse data.
* *`*.mastodon` (Tracking Data):* Project files containing the human-validated cell lineage tracking trees and spatial coordinates.
* *`*.xml` (Metadata):* Configuration files required to link the Mastodon tracking data to the raw HDF5 imaging datasets.


## Raw Imaging Datasets

Due to file size constraints, the raw 4D time-lapse imaging datasets are hosted externally via Google Drive in `.h5` (HDF5) format. 

* [Human Cortical Organoid Raw Dataset (.h5)](link1)
* [Chimpanzee Cortical Organoid Raw Dataset (.h5)](link2)

*Note: Download the corresponding `.xml` files from this repository and place them in the same local directory as the `.h5` files to properly initialize the datasets for viewing in Mastodon.*


## Software Requirements

To utilize these resources, the following software is required:
1. [Fiji (ImageJ)](https://imagej.net/software/fiji/)
2. [Mastodon](https://github.com/mastodon-sc/mastodon) (Installed as a Fiji plugin)
3. [ELEPHANT Client & Server](https://elephant-track.github.io/) (Required only if running further predictions or incremental training with the provided `.pth` weights)
   
For the foundational tracking platform methodology, please cite:
> Sugawara, K., Çevrim, Ç., & Averof, M. (2022). Tracking cell lineages in 3D by incremental deep learning. *eLife*, 11, e69380. PMID: [34989675](https://pubmed.ncbi.nlm.nih.gov/34989675/)


For any questions regarding the dataset and methodology, please contact:
* **Dr. Ikuo K. Suzuki** (suzuki.ikuo@ikuosuzuki-lab.com)
* **Dr. X D. Sheu** (zxhutokyo@gmail.com)
