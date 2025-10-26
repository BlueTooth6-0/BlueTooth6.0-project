# 📜 Scripts Overview

This folder contains the main executable Python scripts for this open-source BLE localization platform.  
Each script focuses on a specific part of the workflow — from data preprocessing and model inference to conversion and evaluation.

---

## 📁 File Summary

| Script | Description |
|--------|--------------|
| `preprocess_ble_data.py` | Converts raw BLE data (RSSI, IQ samples, etc.) into standardized input tensors. Handles normalization and encoding. |
| `test_inference.py` | Loads trained models and performs inference on given input files. Outputs predicted distances or environment classes. |
| `evaluate_metrics.py` | Compares model predictions against ground truth. Supports metrics such as RMSE, MAE, Accuracy, and Confusion Matrix. |
| `convert_to_onnx.py` | Converts PyTorch `.pt` models into ONNX format for cross-platform deployment. |
| `deploy_model.py` | Example deployment script that runs inference with ONNX Runtime or PyTorch backend. |
| `utils/` | (Optional subfolder) Shared helper functions such as logging, data parsing, or metric calculation. |

---

## ⚙️ Installation

Before running the scripts, make sure dependencies are installed:

```bash
pip install -r ../requirements.txt
