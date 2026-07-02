# Data sources and attribution

## Generic Object Decoding dataset

The neuroimaging analyses in this repository are based on data derived from:

**Generic Object Decoding**

- Kamitani Lab
- Tomoyasu Horikawa
- Yukiyasu Kamitani
- Figshare record:
  https://figshare.com/articles/dataset/Generic_Object_Decoding/7387130
- Official project page:
  https://kamitanilab.github.io/GenericObjectDecoding/
- Licence displayed on Figshare: Creative Commons Attribution 4.0
  International (CC BY 4.0)

## Scientific reference

Horikawa, T., & Kamitani, Y. (2017). Generic decoding of seen and imagined
objects using hierarchical visual features. *Nature Communications, 8*,
15037.

## Project-specific derived files

The notebooks were developed using a separately prepared project package
containing:

- a consolidated dataframe with activation maps, ImageNet class labels and
  14 project-defined superclasses;
- visual-ROI masks;
- voxel coordinates;
- an aligned anatomical T1 image;
- legacy Subject 1 MATLAB data;
- training and test image identifiers.

These derived files are required to reproduce the notebooks exactly, but are
not distributed in this repository. Their expected names and local directory
structure are documented in `data/README.md`.

## Visual images

The project-ready local dataframe may include third-party stimulus images.
The official GOD project does not host the experimental images on its server
for copyright reasons. No visual stimuli are included in this repository.

Users must obtain any required images from the appropriate original source
and comply with the relevant terms of use.
