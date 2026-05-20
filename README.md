<h1 align="center">Waste-Segmentation-CNN</h1>

<p align="center">
  <strong>Smart waste classification and route optimization prototype.</strong><br>
  Combines a CNN-style image classifier, Flask web interface, bin status simulation, route logic, report, presentation, and RAPTOR flowchart.
</p>


<p align="center">
  <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/AjaySoni-Dev/Waste-Segmentation-CNN?style=social">
  <img alt="GitHub forks" src="https://img.shields.io/github/forks/AjaySoni-Dev/Waste-Segmentation-CNN?style=social">
</p>

<p align="center">
  <img alt="status: prototype" src="https://img.shields.io/badge/status-prototype-blue">
  <img alt="stack: Python / Notebook" src="https://img.shields.io/badge/stack-Python%20/%20Notebook-informational">
  <img alt="license: MIT" src="https://img.shields.io/badge/license-MIT-green">

</p>

<p align="center">
  <a href="#overview">Overview</a> ·
  <a href="#implemented-components">Implemented Components</a> ·
  <a href="#repository-structure">Repository Structure</a> ·
  <a href="#run-locally">Run Locally</a> ·
  <a href="#limitations">Limitations</a>
</p>

---

## Overview

**Waste-Segmentation-CNN** is a student prototype for intelligent waste management. The repository focuses on three connected ideas:

1. classify waste images,
2. track simulated bin status,
3. generate a simple collection route based on bin conditions.

The uploaded repository contains a notebook-based Flask interface, documentation files, a project presentation, a report, and a RAPTOR flowchart. It is best described as a **working educational prototype** rather than a finished production waste-management platform.

## Implemented Components

| Component | Current Implementation |
|---|---|
| Image classification | `web_interface.ipynb` defines a CNN model structure and image transformation flow using PyTorch/TorchVision. |
| Web interface | Flask routes are created inside the notebook for upload/classification and API-style status calls. |
| Bin monitoring | Simulated bin status logic is included in the notebook. |
| Route optimization | Basic route-selection logic is implemented for demonstration. |
| Documentation | Includes report PDF, PPTX presentation, and RAPTOR flowchart file. |
| Educational explanation | The report and slides explain the waste management problem, objectives, architecture, and future direction. |

## Repository Structure

| File | Purpose |
|---|---|
| `web_interface.ipynb` | Main notebook containing Flask app, CNN model structure, classification route, bin status route, and route logic. |
| `project-report.pdf` | Project report explaining problem, objectives, methodology, and proposed system. |
| `project-ppt.pptx` | 16-slide project presentation. |
| `flow-chart.rap` | RAPTOR flowchart file for logic representation. |
| `README.md` | Original project documentation. |
| `LICENSE` | MIT license. |

## How It Works

```text
Image is uploaded
        ↓
Notebook web interface receives image
        ↓
Image is transformed for model input
        ↓
CNN-style model produces a class prediction
        ↓
Bin status is updated/simulated
        ↓
Route endpoint returns a simple optimized collection path
```

## Run Locally

Install the required libraries:

```bash
pip install torch torchvision flask pillow numpy nest_asyncio
```

Open the notebook:

```bash
jupyter notebook web_interface.ipynb
```

Run the cells in order. The notebook starts a Flask app from inside the notebook environment.

## Limitations

- The current repo does not include a full training dataset.
- The CNN model is defined for demonstration; production accuracy depends on real training data and saved weights.
- Flask inside a notebook is useful for demos but should be moved into a standalone `app.py` for a cleaner project.
- Route optimization is simplified and not connected to real maps or live IoT sensors.
- RAPTOR, report, and PPT files are valuable for presentation, but the codebase needs more modular Python files for long-term maintainability.

## Recommended Improvements

- Convert the notebook into a proper Flask project structure.
- Add dataset download instructions or sample images.
- Save and load trained model weights.
- Add screenshots of the web interface.
- Add a `requirements.txt` file.
- Separate classification, bin monitoring, and routing into modules.

## License

This project is licensed under the MIT License.
