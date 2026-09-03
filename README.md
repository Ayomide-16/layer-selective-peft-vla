# Layer-Selective PEFT VLA

This repository explores whether Maximum Mean Discrepancy (MMD)-based layer selection provides a better accuracy and efficiency trade-off for LoRA fine-tuning of the **OpenVLA-7B** model compared to naive uniform-layer LoRA. 

## Experimental Setup
- **Baseline**: Uniform-layer LoRA fine-tuning on OpenVLA-7B.
- **Proposed Method**: MMD-selective LoRA fine-tuning on OpenVLA-7B.
- **Dataset**: [LIBERO-Object](https://github.com/Lifelong-Robot-Learning/LIBERO) (specifically the `libero_object_no_noops` RLDS subset).
- **Core Codebase**: [OpenVLA](https://github.com/openvla/openvla)

## Project Structure
- `openvla/`: Clone of the core OpenVLA repository used for fine-tuning.
- `kaggle_openvla_smoke_test.ipynb`: A Kaggle-ready Jupyter Notebook that verifies the end-to-end data pipeline and fine-tuning setup before full-scale training.

## Usage
To verify the setup on Kaggle:
1. Open a new Kaggle notebook with GPU (T4 x2 or P100) and Internet enabled.
2. Upload `kaggle_openvla_smoke_test.ipynb`.
3. Run the cells in order. The notebook automatically clones this repository, installs the verified dependencies, downloads the `libero_object_no_noops` dataset, and runs a minimal 10-step smoke test.
