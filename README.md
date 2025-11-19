# KIR Research Computing Training Catalogue

<p align="center">
<img src="./docs/images/third_training_logo.png" alt="drawing" width="500"/>
</p>

## Overview

Central hub for training resources developed by the Research Computing team at the Kennedy Institute of Rheumatology, University of Oxford.

**Live Site:** [https://kir-rescomp.github.io/kir-training-home/](https://kir-rescomp.github.io/kir-training-home/)

## Training Modules

The catalogue links to multiple training modules. Each module is a separate repository with its own documentation site.

| Module | Live Site | GitHub Repository |
|--------|-----------|-------------------|
| Introduction to the Linux Command Line | [Site](https://kir-rescomp.github.io/training-intro-to-linux-cli/) | [Repo](https://github.com/kir-rescomp/training-intro-to-linux-cli) |
| Introduction to Git and GitHub | [Site](https://kir-rescomp.github.io/training-intro-to-git-github/) | [Repo](https://github.com/kir-rescomp/training-intro-to-git-github) |
| Introduction to tmux | [Site](https://kir-rescomp.github.io/training-intro-to-tmux/) | [Repo](https://github.com/kir-rescomp/training-intro-to-tmux) |
| Python Environment Management (In Progress) | [Site](https://kir-rescomp.github.io/training-python-env-management/) | [Repo](https://github.com/kir-rescomp/training-python-env-management) |
| VSCode Remote SSH and Jupyter on Slurm  (In Progress)| [Site](https://kir-rescomp.github.io/training-vscode-jupyter-slurm/) | [Repo](https://github.com/kir-rescomp/training-vscode-jupyter-slurm) |
| Agentic Coding Tools  (In Progress)| [Site](https://kir-rescomp.github.io/training-agentic-coding/) | [Repo](https://github.com/kir-rescomp/training-agentic-coding) |
| Introduction to Apptainer | [Site](https://kir-rescomp.github.io/training-intro-to-apptainer/) | [Repo](https://github.com/kir-rescomp/training-intro-to-apptainer) |
| Introduction to Snakemake | [Site](https://kir-rescomp.github.io/training-intro-to-snakemake/) | [Repo](https://github.com/kir-rescomp/training-intro-to-snakemake) |
| The Basics of Python Packaging | [Site](https://kir-rescomp.github.io/training-basics-python-packaging/) | [Repo](https://github.com/kir-rescomp/training-basics-python-packaging) |
| GPU Profiling | [Site](https://kir-rescomp.github.io/training-gpu-profiling/) | [Repo](https://github.com/kir-rescomp/training-gpu-profiling) |

## Local Development

**Using pip:**
```bash
pip install -r requirements.txt
mkdocs serve
```

**Using pixi (recommended):**
```bash
pixi run serve
```

Visit http://127.0.0.1:8000

## Contributing

To add a new training module, see [CONTRIBUTING.md](./CONTRIBUTING.md).

**Branching:** All contributions should be made on a `<username>-dev` branch (e.g., `jacky-dev`), then submitted as a Pull Request to `main`.

## Structure

This repository contains only the catalogue landing page. Individual training modules are separate repositories linked from the catalogue.

## License

Licensed under GNU General Public License v3.0