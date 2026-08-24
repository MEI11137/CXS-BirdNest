# CXS-BirdNest

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22076927.svg)](https://doi.org/10.5281/zenodo.22076927)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Version](https://img.shields.io/badge/version-v2.0.0-blue.svg)](https://github.com/MEI11137/CXS-BirdNest/releases/tag/v2.0.0)

## A multi-scale UAV dataset for bird-nest detection on overhead transmission lines

CXS-BirdNest supports research on UAV-based bird-nest detection in overhead transmission-line inspection imagery. The dataset contains small- and medium-scale targets acquired under varying observation distances and complex backgrounds.

## Release contents

GitHub release `v2.0.0` contains the complete original, unaugmented image collection and the available annotation archives.

| Resource | Quantity | Description |
| --- | ---: | --- |
| Original UAV image files | 3,552 | Original, unaugmented images |
| Small-scale image group | 2,385 | Images assigned to the small-scale group by the dataset authors |
| Medium-scale image group | 1,167 | Images assigned to the medium-scale group by the dataset authors |
| YOLO annotation files | 5,402 | Labels for the final experimental dataset after training-set augmentation |
| Annotation archives | 8 | `labels1.zip` to `labels8.zip` |

The dataset is organized at two levels. The 3,552 original files preserve the unaugmented image collection, while the 5,402 annotation files document the final experimental dataset obtained after applying augmentation to the training subset. This organization retains the original observations and the labels used in the reported experimental protocol.

## Dataset characteristics

The released imagery reflects practical challenges in UAV transmission-line inspection, including:

- changes in bird-nest scale caused by observation distance;
- complex vegetation and transmission-tower backgrounds;
- partial occlusion by conductors and tower components;
- variations in viewpoint, illumination, and local image contrast;
- limited target pixels in distant-view images.

The image collection was acquired using a DJI Mavic 2 Enterprise Advanced platform. The dataset is intended for bird-nest detection, small- and multi-scale object detection, and computer-vision research related to power-infrastructure inspection.

## Repository structure

The original images are divided across multiple directories to keep individual GitHub folders manageable. Annotation files are distributed as compressed archives.

```text
CXS-BirdNest/
|-- images/
|-- images1/
|-- ...
|-- images37/
|-- labels1.zip
|-- labels2.zip
|-- ...
|-- labels8.zip
|-- CHANGELOG.md
|-- LICENSE
`-- README.md
```

Directory names are storage partitions and do not represent predefined training, validation, or test subsets.

## Annotation format

Bird-nest bounding boxes are stored in YOLO text format:

```text
<class_id> <x_center> <y_center> <width> <height>
```

Coordinates are normalized by image width and height. The dataset uses one detection category for bird nests. Annotation was performed with LabelImg v1.8.6 by two annotators and was followed by a complete self-check and stratified sample review.

## Dataset partitioning

To reproduce the experimental protocol used in the associated study, the 3,552 original images were first stratified by target scale and divided into training, validation, and test subsets at a ratio of 8:1:1.

| Scale group | Training | Validation | Test | Total |
| --- | ---: | ---: | ---: | ---: |
| Small scale | 1,908 | 238 | 239 | 2,385 |
| Medium scale | 934 | 117 | 116 | 1,167 |
| **Total** | **2,842** | **355** | **355** | **3,552** |

Data augmentation was then applied only to the training subset, increasing the number of training samples from 2,842 to 4,692. The validation and test subsets remained unchanged at 355 images each, resulting in a final experimental dataset of 5,402 samples. Splitting the original images before augmentation prevents augmented variants of the same source image from entering different subsets and preserves the independence of model evaluation.

## Download

Image files are managed with [Git Large File Storage](https://git-lfs.com/). Install Git LFS before cloning the repository:

```bash
git lfs install
git clone https://github.com/MEI11137/CXS-BirdNest.git
cd CXS-BirdNest
git lfs pull
```

A normal GitHub source-code archive may contain Git LFS pointer files rather than the image binaries. Cloning with Git LFS is therefore the recommended download method.

## Version and archival status

- **GitHub v2.0.0:** complete original image collection and the currently available annotation archives.
- **Zenodo v2.0.0:** version-specific record available at [10.5281/zenodo.22076927](https://doi.org/10.5281/zenodo.22076927).
- **All Zenodo versions:** linked through the concept DOI [10.5281/zenodo.22020725](https://doi.org/10.5281/zenodo.22020725).

Researchers should cite the version-specific DOI corresponding to the dataset version used in their experiments.

## Citation

When using the dataset, cite the archived Zenodo record and report the exact GitHub release used.

Mei, Y. & Li, R. *CXS-BirdNest Dataset: A Multi-scale UAV Image Dataset for Bird Nest Detection on Overhead Transmission Lines*. Version v2.0.0, Zenodo, https://doi.org/10.5281/zenodo.22076927 (2026).

```bibtex
@dataset{mei_cxs_birdnest_2026,
  author    = {Mei, Yaozhong and Li, Rui},
  title     = {{CXS-BirdNest Dataset}: A Multi-scale UAV Image Dataset for Bird Nest Detection on Overhead Transmission Lines},
  publisher = {Zenodo},
  year      = {2026},
  version   = {v2.0.0},
  doi       = {10.5281/zenodo.22076927},
  url       = {https://doi.org/10.5281/zenodo.22076927}
}
```

The citation for the associated research article will be added after publication.

## Intended use and reproducibility

CXS-BirdNest is released for academic research and education under the terms of the license. Users may develop and evaluate object-detection methods, study small- and multi-scale targets, or investigate UAV-based transmission-line inspection.

For direct comparison with the associated study, users are encouraged to follow the scale-stratified partitioning and training-only augmentation protocol described above. Any alternative partitioning, preprocessing, or augmentation strategy should be reported with the resulting experimental findings.

## License

The released dataset is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/). Redistribution and adaptation are permitted provided that appropriate credit is given. See [LICENSE](LICENSE) for the complete terms.

## Contact

Please use the repository's [GitHub Issues](https://github.com/MEI11137/CXS-BirdNest/issues) page for questions, corrections, or reuse-related requests.
