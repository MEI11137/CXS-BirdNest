# CXS-BirdNest

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22020726.svg)](https://doi.org/10.5281/zenodo.22020726)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## CXS-BirdNest: A Multi-scale UAV Image Dataset for Bird Nest Detection on Overhead Transmission Lines

**CXS-BirdNest** is a multi-scale UAV image dataset developed for bird-nest detection on overhead transmission lines.

The complete CXS-BirdNest dataset constructed in this study consists of **5,402 annotated UAV images**. To facilitate reproducibility and public access, this repository provides a **public reproducibility subset containing 2,081 UAV images and their corresponding annotations**, selected from the complete dataset.

The publicly released subset is intended to support the reproduction and evaluation of the methodology presented in the associated study.

---

## Dataset Overview

### Complete CXS-BirdNest Dataset

The complete CXS-BirdNest dataset contains:

- **5,402 annotated UAV images**
- Bird-nest bounding-box annotations
- Multi-scale bird-nest targets
- UAV imagery from overhead transmission-line inspection scenarios

### Public Reproducibility Subset

The publicly released subset contains:

- **2,081 UAV images** selected from the complete dataset
- Corresponding bird-nest bounding-box annotations
- YOLO-format annotation files
- Training, validation, and test split information
- Dataset documentation and related reproducibility resources

> **Note:** The complete CXS-BirdNest dataset consists of 5,402 annotated UAV images.  
> The 2,081 images provided in this repository constitute the publicly available reproducibility subset.

---

## Annotation Format

Bird-nest bounding-box annotations are provided in **YOLO format**.

Each annotation follows the format:

```text
<class_id> <x_center> <y_center> <width> <height>
