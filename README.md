# Automated Synthesis of Facial Mechanisms for Conversational Animatronic Robots

<p align="center">
  <a href="https://zzongzheng0918.github.io/automated-facial-mechanisms-synthesis/"><img src="https://img.shields.io/badge/Project%20Page-Website-2f80ed?style=for-the-badge&logo=githubpages&logoColor=white" alt="Project Page"></a>
  <a href="https://arxiv.org/abs/2607.11688"><img src="https://img.shields.io/badge/arXiv-2607.11688-b31b1b?style=for-the-badge&logo=arxiv&logoColor=white" alt="arXiv:2607.11688"></a>
  <a href="https://huggingface.co/datasets/Zzz0918/mechanical-head-mouth-calibration"><img src="https://img.shields.io/badge/Dataset-Hugging%20Face-ffcc4d?style=for-the-badge&logo=huggingface&logoColor=black" alt="Dataset"></a>
</p>

<h3 align="center">
  <strong>Accepted to RSS 2026 &nbsp;&nbsp;·&nbsp;&nbsp; Best Paper Finalist</strong>
</h3>

The project studies how to design and calibrate expressive facial mechanisms for conversational animatronic robots. In addition to the paper and dataset, we have open-sourced the complete SolidWorks assembly models for seven robot heads, so that future researchers and builders can study how the mechanisms are physically arranged and adapt the designs for their own work.

> **Hardware release:** The complete models for **BaiShe, Elf, Jack, Luke, Rose, XiaoQing, and XuXian** are available in the [`hardware/`](hardware/) directory.

## Overview

Conversational robots need faces that are expressive, compact, and mechanically feasible. This work focuses on automatically synthesizing facial mechanisms and connecting the mechanical design to data-driven calibration signals such as motor commands, landmarks, and blendshape coefficients.

This repository is intended to serve as a lightweight entry point for the project:

- released dataset pointer
- complete SolidWorks models for seven robot-head mechanisms
- documentation for reproducing or extending the system

## Diverse Facial Mechanism Synthesis

<p align="center">
  <img src="assets/images/diverse-facial-mechanism-synthesis.png" alt="Eight synthesized robotic head mechanisms: Yoda, Luke, Rose, Jack, Elf, Xuxian, Bai Suzhen, and Xiaoqing" width="100%">
</p>

<p align="center">
  <em>Automated mechanism synthesis across eight diverse facial morphologies: Yoda, Luke, Rose, Jack, Elf, Xuxian, Bai Suzhen, and Xiaoqing. Complete CAD models for seven of these heads are released below.</em>
</p>

## Dataset

The released dataset contains **4993 aligned samples** captured from a mechanical-head mouth system. Each sample includes:

- a monocular camera image
- raw paired PWM motor commands
- normalized motor commands
- MediaPipe mouth/jaw blendshape coefficients
- normalized mouth-region landmark coordinates
- metadata, schema, and manifest files

The dataset is available at:

https://huggingface.co/datasets/Zzz0918/mechanical-head-mouth-calibration

The dataset is aligned by `sample_id`:

```text
sample_id = i  <=>  images/i.jpg  <=>  row sample_id=i in every CSV
```

## Open-Source Complete Head Models

We have open-sourced the complete SolidWorks assembly models for the following robot heads. Each folder contains the top-level assemblies and their referenced part files:

- [BaiShe](hardware/BaiShe/)
- [Elf](hardware/elf/)
- [Jack](hardware/jack/)
- [Luke](hardware/luke/)
- [Rose](hardware/rose/)
- [XiaoQing](hardware/XiaoQing/)
- [XuXian](hardware/XuXian/)

These files are meant to help readers understand:

- how the facial mechanism components are arranged inside the head
- how mouth, jaw, and surrounding facial structures are mechanically organized
- how compact internal layouts can support conversational facial motion
- how to adapt the design ideas to other animatronic or robotic heads

The complete models are provided for research and educational use. They are intended as assembly and design references rather than ready-to-manufacture production files.

## Repository Structure

```text
.
+-- README.md
+-- scalable_conversational_faces.pdf
+-- assets/
+-- docs/
+-- hardware/
+-- scripts/
+-- src/
+-- examples/
+-- requirements.txt
```

Key organization:

- `assets/`: teaser images, figures, and lightweight visual assets
- `docs/`: additional documentation and mechanism notes
- `hardware/`: complete SolidWorks assemblies and referenced parts for seven robot heads
- `scripts/`: data processing, calibration, and visualization scripts
- `src/`: core implementation
- `examples/`: minimal examples for running the released code

## Getting Started

```bash
git clone https://github.com/ZZongzheng0918/automated-facial-mechanisms-synthesis.git
cd automated-facial-mechanisms-synthesis

conda create -n facial-mechanisms python=3.10
conda activate facial-mechanisms
pip install -r requirements.txt
```

More detailed installation and usage instructions will be added as the code release is finalized.

## Citation

If you find this work useful, please cite:

```bibtex
@article{zhang2026automated,
  title   = {Automated Synthesis of Facial Mechanisms for Conversational Animatronic Robots},
  author  = {Zhang, Zongzheng and Lin, Zi and Yang, Jiawen and Peng, Ziqiao and Lao, Junyan and Cheng, Lin and Xu, Huazhe and Zhao, Hang and Zhao, Hao},
  journal = {arXiv preprint arXiv:2607.11688},
  year    = {2026}
}
```

## License

Code, dataset, and hardware-reference licenses will be specified before the final public release.

If you use the dataset, please also refer to the license and metadata on the Hugging Face dataset page.

