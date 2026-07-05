# Automated Synthesis of Facial Mechanisms for Conversational Animatronic Robots

<p align="center">
  <a href="https://zzongzheng0918.github.io/automated-facial-mechanisms-synthesis/"><img src="https://img.shields.io/badge/Project%20Page-Website-2f80ed?style=for-the-badge&logo=githubpages&logoColor=white" alt="Project Page"></a>
  <a href="https://arxiv.org/"><img src="https://img.shields.io/badge/arXiv-coming%20soon-b31b1b?style=for-the-badge&logo=arxiv&logoColor=white" alt="arXiv"></a>
  <a href="https://huggingface.co/datasets/Zzz0918/mechanical-head-mouth-calibration"><img src="https://img.shields.io/badge/Dataset-Hugging%20Face-ffcc4d?style=for-the-badge&logo=huggingface&logoColor=black" alt="Dataset"></a>
</p>

<h3 align="center">
  🎉 <strong>Accepted to RSS 2026</strong>
</h3>

The project studies how to design and calibrate expressive facial mechanisms for conversational animatronic robots. In addition to the paper and dataset, this repository will provide reference materials for several robot-head internal 3D architectures and assembly layouts, so that future researchers and builders can better understand how the mechanisms are physically arranged.

## Overview

Conversational robots need faces that are expressive, compact, and mechanically feasible. This work focuses on automatically synthesizing facial mechanisms and connecting the mechanical design to data-driven calibration signals such as motor commands, landmarks, and blendshape coefficients.

This repository is intended to serve as a lightweight entry point for the project:

- paper and project links
- released dataset pointer
- 3D assembly diagrams for robot-head internal mechanisms
- documentation for reproducing or extending the system

## Resources

- **Paper PDF:** [scalable_conversational_faces](https://github.com/ZZongzheng0918/automated-facial-mechanisms-synthesis/blob/main/scalable_conversational_faces.pdf)
- **Dataset:** [Mechanical Head Mouth Calibration Dataset](https://huggingface.co/datasets/Zzz0918/mechanical-head-mouth-calibration)
- **Project page:** coming soon
- **arXiv:** coming soon

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

## 3D Mechanism References

Besides the dataset, this repository will include reference materials for several robot-head internal 3D architectures and assembly layouts.

These files are meant to help readers understand:

- how the facial mechanism components are arranged inside the head
- how mouth, jaw, and surrounding facial structures are mechanically organized
- how compact internal layouts can support conversational facial motion
- how to adapt the design ideas to other animatronic or robotic heads

The 3D references are provided for research and educational use. They are intended as assembly and design references rather than ready-to-manufacture production files.

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

Planned organization:

- `assets/`: teaser images, figures, and lightweight visual assets
- `docs/`: additional documentation and mechanism notes
- `hardware/`: 3D assembly references and internal architecture diagrams
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
@inproceedings{zhong2026automated,
  title     = {Automated Synthesis of Facial Mechanisms for Conversational Animatronic Robots},
  author    = {TBD},
  booktitle = {Robotics: Science and Systems (RSS)},
  year      = {2026}
}
```

## License

Code, dataset, and hardware-reference licenses will be specified before the final public release.

If you use the dataset, please also refer to the license and metadata on the Hugging Face dataset page.

## Acknowledgements

We thank the collaborators and contributors who supported the design, fabrication, data collection, and evaluation of the conversational animatronic robot platform.
