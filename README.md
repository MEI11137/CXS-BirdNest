# CXS-BirdNest

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22020726.svg)](https://doi.org/10.5281/zenodo.22020726)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Version](https://img.shields.io/badge/version-v1.0.1-blue.svg)](https://github.com/MEI11137/CXS-BirdNest/releases/tag/v1.0.1)

## CXS-BirdNest: A Multi-scale UAV Image Dataset for Bird Nest Detection on Overhead Transmission Lines

**CXS-BirdNest** is a multi-scale UAV image dataset constructed for bird-nest detection on overhead transmission lines using unmanned aerial vehicle (UAV) imagery.

The complete CXS-BirdNest dataset constructed in this study consists of **5,402 annotated UAV images**. To facilitate reproducibility and public access, this repository provides a **public reproducibility subset containing 2,081 UAV images and their corresponding annotations**, selected from the complete dataset.

The publicly released subset is intended to facilitate the reproduction and evaluation of the methodology presented in the associated study and to support further research on UAV-based transmission-line inspection, bird-nest detection, small-object detection, and multi-scale object detection.

---

## Dataset Overview

### Complete CXS-BirdNest Dataset

The complete CXS-BirdNest dataset consists of:

- **5,402 annotated UAV images**
- Bird-nest bounding-box annotations
- Bird-nest targets at multiple scales
- UAV imagery from overhead transmission-line inspection scenarios
- Images containing complex backgrounds and diverse bird-nest appearances
- Data designed for bird-nest detection and related object-detection research

The complete dataset serves as the primary dataset constructed for the associated research.

### Public Reproducibility Subset

To facilitate reproducibility and public access, a subset of the complete CXS-BirdNest dataset has been publicly released.

The public reproducibility subset contains:

- **2,081 UAV images** selected from the complete dataset
- Corresponding bird-nest bounding-box annotations
- Annotations in **YOLO format**
- Dataset documentation and related reproducibility resources

> **Important:**  
> The complete CXS-BirdNest dataset contains **5,402 annotated UAV images**, whereas this repository publicly releases a **2,081-image reproducibility subset** selected from the complete dataset.

No predefined training, validation, or test split is imposed in this public release.

---

## Dataset Characteristics

CXS-BirdNest focuses on bird-nest detection in UAV imagery acquired from overhead transmission-line inspection scenarios.

The dataset contains bird-nest targets at different scales and under varying visual conditions. It is designed to reflect challenges commonly encountered during UAV-based power-line inspection, including:

- Small bird-nest targets
- Multi-scale target distribution
- Complex natural backgrounds
- Transmission-line infrastructure interference
- Variations in UAV imaging distance and viewpoint
- Different bird-nest appearances and surrounding environments

These characteristics make CXS-BirdNest suitable for evaluating object-detection methods under practical UAV inspection conditions.

---

## Annotation Format

Bird-nest bounding-box annotations are provided in **YOLO format**.

Each annotation follows the standard format:

```text
<class_id> <x_center> <y_center> <width> <height>
```

where:

- `class_id` represents the object category;
- `x_center` represents the normalized horizontal coordinate of the bounding-box center;
- `y_center` represents the normalized vertical coordinate of the bounding-box center;
- `width` represents the normalized width of the bounding box;
- `height` represents the normalized height of the bounding box.

The bounding-box coordinates are normalized relative to the width and height of the corresponding UAV image.

---

## Dataset Structure

The public release contains UAV images and their corresponding YOLO-format annotation files.

A typical organization of the released resources is:

```text
CXS-BirdNest/
├── images/
│   └── ...
├── labels/
│   └── ...
├── README.md
└── LICENSE
```

Some dataset resources may be distributed as compressed archives.

Please refer to the files included in the corresponding GitHub release for the exact organization of a specific version.

---

## Dataset Partitioning

No predefined training, validation, or test split is imposed in the current public release.

Researchers may organize or partition the **2,081-image public reproducibility subset** according to the requirements of their experimental protocols.

When reporting experimental results obtained using CXS-BirdNest, users are encouraged to clearly describe the dataset partitioning strategy used in their experiments to facilitate fair comparison and reproducibility.

---

## Reproducibility

The publicly released **2,081-image subset** is derived from the complete **5,402-image CXS-BirdNest dataset**.

This subset is released to facilitate:

- Reproduction and evaluation of the methodology presented in the associated study
- Evaluation of bird-nest detection algorithms
- Comparison of object-detection approaches
- Research on small-object detection
- Research on multi-scale object detection
- Development of UAV-based transmission-line inspection methods
- Further research on computer vision for power infrastructure inspection

The public release does not impose a predefined training, validation, or test partition. Researchers may define appropriate experimental splits according to their research objectives and should report those settings when publishing results based on the dataset.

---

## Intended Use

CXS-BirdNest is intended primarily for academic research and educational purposes.

Potential applications include:

- Bird-nest detection on overhead transmission lines
- UAV-based transmission-line inspection
- Intelligent power infrastructure inspection
- Small-object detection
- Multi-scale object detection
- UAV image analysis
- Object detection
- Computer vision for power infrastructure
- Automated inspection of overhead transmission lines

Researchers may use the publicly released subset to develop, train, validate, benchmark, or evaluate object-detection methods under the terms of the applicable license.

---

## Data Availability

The complete CXS-BirdNest dataset constructed in this study consists of **5,402 annotated UAV images**.

To facilitate reproducibility and public access, a **public reproducibility subset containing 2,081 UAV images and their corresponding annotations** has been made openly available through this GitHub repository and Zenodo.

### Zenodo Dataset Record

- **Dataset:** CXS-BirdNest
- **Version:** v1.0.1
- **Publisher:** Zenodo
- **Publication year:** 2026
- **DOI:** [10.5281/zenodo.22020726](https://doi.org/10.5281/zenodo.22020726)

The Zenodo record provides a persistent and citable archive of the publicly released CXS-BirdNest reproducibility subset.

---

## GitHub Release

The current public dataset release is:

**CXS-BirdNest Dataset v1.0.1**

Release tag:

```text
v1.0.1
```

The GitHub release corresponds to the publicly archived dataset version associated with the Zenodo record.

GitHub repository:

https://github.com/MEI11137/CXS-BirdNest

---

## Citation

If you use **CXS-BirdNest** or its publicly released reproducibility subset in your research, please cite the dataset and, when available, the associated research paper.

### Dataset Citation

**CXS-BirdNest: A Multi-scale UAV Image Dataset for Bird Nest Detection on Overhead Transmission Lines.**  
Version v1.0.1. Zenodo, 2026.

**DOI:** [10.5281/zenodo.22020726](https://doi.org/10.5281/zenodo.22020726)

### BibTeX

```bibtex
@dataset{cxs_birdnest_2026,
  title     = {{CXS-BirdNest}: A Multi-scale UAV Image Dataset for Bird Nest Detection on Overhead Transmission Lines},
  publisher = {Zenodo},
  year      = {2026},
  version   = {v1.0.1},
  doi       = {10.5281/zenodo.22020726},
  url       = {https://doi.org/10.5281/zenodo.22020726}
}
```

The author information should follow the creator metadata registered in the Zenodo record.

The citation information for the associated research paper will be added after publication.

---

## License

The publicly released CXS-BirdNest dataset is licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0) License**.

Under CC BY 4.0, users are permitted to share and adapt the publicly released dataset, including redistribution and use in derivative works, provided that appropriate credit is given to the dataset creators and the applicable license terms are followed.

For academic use, users are encouraged to cite the CXS-BirdNest dataset and the associated research publication.

Full license information:

https://creativecommons.org/licenses/by/4.0/

The full license text is also provided in the `LICENSE` file of this repository.

---

## Version Information

Current public release:

```text
CXS-BirdNest v1.0.1
```

Future revisions or extensions of the publicly released dataset may be published as new versions.

For reproducibility, researchers should report the specific version of CXS-BirdNest used in their experiments.

---

## Associated Publication

CXS-BirdNest was constructed in connection with research on multi-scale bird-nest detection in UAV imagery of overhead transmission lines.

The bibliographic information and DOI of the associated research paper will be added here after publication.

When the associated paper becomes available, users of the dataset are encouraged to cite both the dataset record and the corresponding research paper.

---

## Data Usage and Attribution

When using the publicly released CXS-BirdNest subset, users should:

1. Cite the CXS-BirdNest Zenodo dataset record.
2. Cite the associated research paper once it becomes available.
3. Clearly report the dataset version used in their experiments.
4. Clearly describe any dataset partitioning or preprocessing strategy used.
5. Indicate whether the original annotations were modified.
6. Follow the attribution requirements of the CC BY 4.0 license.

---

## Disclaimer

CXS-BirdNest is released primarily for academic research and educational purposes.

Users are responsible for ensuring that their use, redistribution, or adaptation of the dataset complies with the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license and any applicable laws, regulations, institutional policies, or ethical requirements.

---

## Contact

For questions, suggestions, or issues related to CXS-BirdNest, please use the **GitHub Issues** section of this repository.

Repository:

https://github.com/MEI11137/CXS-BirdNest

---

## Acknowledgment

If CXS-BirdNest contributes to your research, please consider citing the dataset and the associated research publication.

We hope that CXS-BirdNest can support further research on UAV-based transmission-line inspection, bird-nest detection, small-object detection, multi-scale object detection, and intelligent power infrastructure inspection.
