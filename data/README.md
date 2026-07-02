# Local data setup

The dataset is **not included in this GitHub repository**.

The notebooks expect the required files to be placed locally inside this
directory:

```text
data/
├── god_with_superclass.pkl
├── roi_masks.npz
├── voxel_coords.npz
├── Subject1.mat
├── Subject1_T1wAligned.nii
├── imageID_training.csv
└── imageID_test.csv
```

The repository `.gitignore` excludes all files in `data/`, except this README
and `.gitkeep`, so the local dataset will not be uploaded accidentally.

## Expected files

### `god_with_superclass.pkl`

Project-specific pandas dataframe used by the main classification notebooks.

Expected content:

- 1,200 fMRI samples;
- one 4,466-element activation vector per sample;
- 150 fine-grained ImageNet object classes;
- 14 semantic superclasses;
- stimulus identifiers, class names and project labels;
- in the local project copy, the dataframe may also contain a `stimulus`
  column with visual images.

Expected columns:

```text
activation_map_id
activation_map
stimulus
imagenet_class_wnid
imagenet_class_name
superclass
```

This exact pickle is a **project-prepared derivative** and is not one of the
standard filenames distributed directly through Figshare.

### `roi_masks.npz`

Boolean masks, each with length 4,466, for the following visual regions:

```text
V1, V2, V3, V4, FFA, PPA, LOC, LVC, HVC, VC
```

### `voxel_coords.npz`

Voxel coordinates for the 4,466 selected features, stored as:

```text
x, y, z
```

### `Subject1.mat`

Legacy preprocessed Subject 1 data used by the supporting anatomical and
visualization notebook.

### `Subject1_T1wAligned.nii`

Aligned T1-weighted anatomical reference used to map ROI and voxel-level
importance results into anatomical space.

### `imageID_training.csv` and `imageID_test.csv`

Image identifiers used by the supporting MATLAB-data loader.

## Underlying dataset

The project is based on the **Generic Object Decoding (GOD)** dataset:

- Authors: Kamitani Lab, Tomoyasu Horikawa and Yukiyasu Kamitani
- Dataset record:
  https://figshare.com/articles/dataset/Generic_Object_Decoding/7387130
- Licence shown on the official Figshare record: CC BY 4.0
- Project page:
  https://kamitanilab.github.io/GenericObjectDecoding/

The corresponding paper is:

> Horikawa, T., & Kamitani, Y. (2017). Generic decoding of seen and imagined
> objects using hierarchical visual features. Nature Communications, 8,
> 15037.

## Obtaining the files

The exact project-ready files listed above must be obtained separately from
the original project materials or reconstructed from the GOD dataset using
the same preprocessing and superclass-labelling pipeline.

The official Figshare dataset contains the underlying preprocessed fMRI data,
but it does not necessarily use the same project-specific filenames or
consolidated dataframe structure.

## Visual-stimulus note

The official GOD project states that the visual images used in the
experiments are not hosted on its server for copyright reasons. Therefore,
this repository does not distribute the local pickle or any embedded
stimulus images.

Keep any stimulus-containing dataset local and verify the applicable source
or ImageNet terms before sharing it elsewhere.
