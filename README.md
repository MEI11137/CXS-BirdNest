# CXS-BirdNest

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22202440.svg)](https://doi.org/10.5281/zenodo.22202440)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

[中文说明 / Chinese](README_zh-CN.md)

## Overview

CXS-BirdNest is a UAV image dataset for bird-nest detection on overhead transmission lines. It supports research on small- and multi-scale object detection in visually complex power-infrastructure scenes.

The public release provides a directly usable train/validation/test split. Each image has one YOLO-format annotation file with the same filename stem.

## Release at a glance

| Split | Images | Annotation archive | Labels |
| --- | ---: | --- | ---: |
| Train | 4,692 | `labels-train.zip` | 4,692 |
| Validation | 356 | `labels-val.zip` | 356 |
| Test | 356 | `labels-test.zip` | 356 |
| **Total** | **5,404** | **3 archives** | **5,404** |

The release contains 6,148 bounding boxes. It has one category: class `0`, **bird nest**.

## Repository layout

```text
CXS-BirdNest/
├── images0/ ... images53/   # JPEG image storage partitions
├── labels-train.zip         # train_*.txt annotations
├── labels-val.zip           # val_*.txt annotations
├── labels-test.zip          # test_*.txt annotations
├── LICENSE
├── CITATION.cff
├── CHANGELOG.md
├── README.md
└── README_zh-CN.md
```

The numbered `images*` directories are storage partitions for large files. They do **not** define the data split. Split membership is defined by the filename prefix: `train_`, `val_`, or `test_`.

## Download

Images are stored with [Git Large File Storage (Git LFS)](https://git-lfs.com/):

```bash
git lfs install
git clone https://github.com/MEI11137/CXS-BirdNest.git
cd CXS-BirdNest
git lfs pull
```

A standard GitHub source-code archive may contain Git LFS pointer files instead of the full JPEG images.

## Labels and image-label pairing

Extract the split-specific label archives before training or evaluation:

```bash
unzip labels-train.zip -d labels/train
unzip labels-val.zip -d labels/val
unzip labels-test.zip -d labels/test
```

Pair images and labels by filename stem:

```text
train_000001.jpg  <->  train_000001.txt
val_000001.jpg    <->  val_000001.txt
test_000001.jpg   <->  test_000001.txt
```

All 5,404 released images and labels are directly pairable by this rule. Preserve the supplied prefixes and split membership when reproducing results.

## Annotation format

Each YOLO row has one bounding box:

```text
<class_id> <x_center> <y_center> <width> <height>
```

Coordinates are normalized to image width and height.

| Class ID | Class name |
| ---: | --- |
| 0 | bird nest |

## Dataset split

| Split | Images | Filename prefix |
| --- | ---: | --- |
| Train | 4,692 | `train_` |
| Validation | 356 | `val_` |
| Test | 356 | `test_` |

Use the supplied split for comparable experiments. Report any re-splitting, filtering, augmentation, or other transformation with your results.

## Intended use and limitations

The dataset is intended for academic research and education, including bird-nest detection, small- and multi-scale object detection, and computer-vision methods for transmission-line inspection.

Images include varying target scale, complex vegetation and tower backgrounds, partial occlusion, viewpoint changes, and illumination changes. The dataset should not be treated as evidence that a model will generalize to every region, flight configuration, camera system, or inspection workflow.

## Licence

CXS-BirdNest is distributed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/). Reuse, redistribution, and adaptation are permitted with appropriate attribution. See [LICENSE](LICENSE).

## Citation

Please cite the version-specific Zenodo record and report the GitHub release used:

Mei, Y. & Li, R. *CXS-BirdNest Dataset: A Multi-scale UAV Image Dataset for Bird Nest Detection on Overhead Transmission Lines*. Version v2.0.0, Zenodo, https://doi.org/10.5281/zenodo.22202440 (2026).

```bibtex
@dataset{mei_cxs_birdnest_2026,
  author    = {Mei, Yaozhong and Li, Rui},
  title     = {{CXS-BirdNest Dataset}: A Multi-scale UAV Image Dataset for Bird Nest Detection on Overhead Transmission Lines},
  publisher = {Zenodo},
  year      = {2026},
  version   = {v2.1.0},
  doi       = {10.5281/zenodo.22202440},
  url       = {https://doi.org/10.5281/zenodo.22202440}
}
```

The associated research-paper citation will be added after publication.

## Contact

Please use [GitHub Issues](https://github.com/MEI11137/CXS-BirdNest/issues) for questions, corrections, or reuse-related requests.
