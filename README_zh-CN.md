# CXS-BirdNest

[English](README.md)

## 数据集概述

CXS-BirdNest 是面向架空输电线路鸟巢检测的无人机图像数据集，可用于复杂电力基础设施场景中的小目标与多尺度目标检测研究。

本公开版本提供可直接使用的训练、验证和测试划分；每张图像均有一个文件名主干相同的 YOLO 格式标注文件。

## 发布内容一览

| 划分 | 图像数 | 标注压缩包 | 标注文件数 |
| --- | ---: | --- | ---: |
| 训练集 | 4,692 | `labels-train.zip` | 4,692 |
| 验证集 | 356 | `labels-val.zip` | 356 |
| 测试集 | 356 | `labels-test.zip` | 356 |
| **合计** | **5,404** | **3 个压缩包** | **5,404** |

本版本包含 6,148 个边界框，仅含一个类别：类别 `0`，即**鸟巢**。

## 仓库结构

```text
CXS-BirdNest/
├── images0/ ... images53/   # JPEG 图像存储分区
├── labels-train.zip         # train_*.txt 标注
├── labels-val.zip           # val_*.txt 标注
├── labels-test.zip          # test_*.txt 标注
├── LICENSE
├── CITATION.cff
├── CHANGELOG.md
├── README.md
└── README_zh-CN.md
```

编号形式的 `images*` 目录仅用于分散存储大体积文件，**不**代表训练、验证或测试划分。划分由文件名前缀 `train_`、`val_` 和 `test_` 决定。

## 下载

图像通过 [Git Large File Storage (Git LFS)](https://git-lfs.com/) 管理：

```bash
git lfs install
git clone https://github.com/MEI11137/CXS-BirdNest.git
cd CXS-BirdNest
git lfs pull
```

直接下载 GitHub 源码压缩包时，可能只会获得 Git LFS 指针文件，而不是完整 JPEG 图像。

## 标注与图像配对

训练或评估前，请解压三个标注压缩包：

```bash
unzip labels-train.zip -d labels/train
unzip labels-val.zip -d labels/val
unzip labels-test.zip -d labels/test
```

图像与标注按相同文件名主干直接配对：

```text
train_000001.jpg  <->  train_000001.txt
val_000001.jpg    <->  val_000001.txt
test_000001.jpg   <->  test_000001.txt
```

全部 5,404 张图像和标注均可按此规则一一对应。复现实验时请保留给定的文件名前缀与数据划分。

## 标注格式

YOLO 标注中每行对应一个边界框：

```text
<class_id> <x_center> <y_center> <width> <height>
```

坐标均相对于图像宽度和高度归一化。

| 类别 ID | 类别名称 |
| ---: | --- |
| 0 | bird nest（鸟巢） |

## 数据划分

| 划分 | 图像数 | 文件名前缀 |
| --- | ---: | --- |
| 训练集 | 4,692 | `train_` |
| 验证集 | 356 | `val_` |
| 测试集 | 356 | `test_` |

为便于结果比较，建议使用本仓库提供的划分。若重新划分、筛选、增强或以其他方式转换数据，请在报告结果时明确说明。

## 适用范围与局限性

本数据集面向学术研究和教学，可用于鸟巢检测、小目标与多尺度目标检测，以及输电线路巡检相关的计算机视觉研究。

图像包含目标尺度变化、植被和杆塔等复杂背景、局部遮挡、视角变化与光照变化等实际挑战。本数据集不能直接代表模型在所有地理区域、飞行配置、相机系统或巡检流程中的泛化能力。

## 许可协议

CXS-BirdNest 采用 [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) 发布。在适当署名的前提下，允许复用、再分发和改编。完整条款见 [LICENSE](LICENSE)。

## 引用方式

使用本数据集时，请引用对应版本的 Zenodo 记录，并报告实验所用的 GitHub 发布版本：

Mei, Y. & Li, R. *CXS-BirdNest Dataset: A Multi-scale UAV Image Dataset for Bird Nest Detection on Overhead Transmission Lines*. Version v2.0.0, Zenodo, https://doi.org/10.5281/zenodo.22202440 (2026).

```bibtex
@dataset{mei_cxs_birdnest_2026,
  author    = {Mei, Yaozhong and Li, Rui},
  title     = {{CXS-BirdNest Dataset}: A Multi-scale UAV Image Dataset for Bird Nest Detection on Overhead Transmission Lines},
  publisher = {Zenodo},
  year      = {2026},
  version   = {v2.0.0},
  doi       = {10.5281/zenodo.22202440},
  url       = {https://doi.org/10.5281/zenodo.22202440}
}
```

关联研究论文正式发表后，将在此补充论文引用信息。

## 联系方式

如有问题、勘误或数据复用相关需求，请通过仓库的 [GitHub Issues](https://github.com/MEI11137/CXS-BirdNest/issues) 提交。
