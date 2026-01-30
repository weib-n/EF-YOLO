# EF-YOLO: Early Fire Detection Network Based on SPD-Conv and DP-FSE Modules

<div align="center">

![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLO-v8-blue)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

</div>

## 📖 Introduction (简介)

This is the official implementation of the paper **"EF-YOLO: Early Fire Detection Network Based on SPD-Conv and DP-FSE Modules"**.

Early fire detection is challenging due to the extremely small proportion of fire targets in images and the high uncertainty of smoke shapes. Standard YOLO architectures often lose critical information of tiny fire spots during downsampling. 

**EF-YOLO** addresses these limitations by introducing three core improvements:

1.  **SPD-Conv (Space-to-Depth Convolution):** Replaces traditional strided convolutions in the backbone to prevent the loss of fine-grained information for small targets.
2.  **DP-FSE (Dual-Path Feature Stimulation and Enhancement):** A novel module in the Neck that uses dual-path pooling (Average & Max) to enhance the perception of flame edges and thin smoke.
3.  **P2 Detection Head:** Adds a high-resolution detection head (160x160) to significantly improve the recall rate of tiny fire spots (as small as 4x4 pixels).

---

## 🛠️ Architecture (网络架构)

The EF-YOLO architecture improves upon YOLOv8 by restructuring the feature extraction and fusion paths.

> *[Please upload your architecture diagram (Figure 1 from your paper) to the 'docs' folder and update this link]*
> ![EF-YOLO Architecture](./docs/architecture.png)

---

## 📦 Installation (安装)

```bash
# Clone the repository
git clone [https://github.com/weib-n/EF-YOLO.git](https://github.com/weib-n/EF-YOLO.git)
cd EF-YOLO

# Install dependencies
pip install -r requirements.txt
