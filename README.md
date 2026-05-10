# MarineDebris-Net: Real-Time Underwater Trash Detection

[![YOLOv8](https://img.shields.io/badge/Model-YOLOv8-blue.svg)](https://ultralytics.com)
[![Python](https://img.shields.io/badge/Python-3.12-yellow.svg)](https://www.python.org/)

An end-to-end Computer Vision pipeline to detect and localize 15 categories of marine pollutants. This project uses a **YOLOv8 (Nano)** architecture to achieve high-speed inference, making it suitable for deployment on autonomous underwater vehicles (AUVs).

## Performance Summary
* **Inference Speed:** 2.3ms (~434 FPS) on NVIDIA Tesla T4 GPU.
* **Global mAP@50:** 0.60 (60%).
* **Best Performing Classes:** Cellphones (99%), Plastic Bags (95%), Fishing Nets (86%).

## Tech Stack
- **Framework:** Ultralytics YOLOv8
- **Language:** Python 3.12
- **Libraries:** PyTorch, OpenCV, Matplotlib, YAML
- **Platform:** Google Colab (GPU Accelerated)

## Results
Training was conducted over 20 epochs using transfer learning from COCO-pretrained weights.

| Metric | Value |
| :--- | :--- |
| **Precision (P)** | 0.591 |
| **Recall (R)** | 0.606 |
| **mAP50** | 0.600 |
| **Inference Latency** | 2.3ms |

### Key Insights
- **Class Imbalance:** The model excels at identifying bulky items (Tires, Bags) but requires more data for smaller categories like 'metal' and 'sunglasses'.
- **Real-Time Readiness:** The ultra-low latency allows for temporal consistency across video frames, enabling tracking in live streams.

## Repository Structure
- `Marine_Pollution_YOLOv8.ipynb`: The complete training & inference pipeline.
- `marine_pollution.yaml`: Dataset configuration file.


