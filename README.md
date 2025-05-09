# Evaluating YOLOv8 Models for Efficient Drone Detection

## Project Overview

This project presents a comparative study of two variants of the YOLOv8 model—**YOLOv8-S (Small)** and **YOLOv8-L (Large)**—for Unmanned Aerial Vehicle (UAV) detection, specifically focusing on drone recognition in anti-UAV systems. The goal is to explore the trade-offs between detection accuracy and computational efficiency using:

* **Drone-only dataset**
* **Combined bird + drone dataset**

## Notebooks

The repository contains the following Jupyter Notebooks:

| Notebook           | Dataset                      | Model Used   |
| ------------------ | ---------------------------- | ------------ |
| `Drone_S.ipynb`    | Drone-only images            | YOLOv8 Small |
| `Drone_L.ipynb`    | Drone-only images            | YOLOv8 Large |
| `Combined_S.ipynb` | Combined bird + drone images | YOLOv8 Small |
| `Combined_L.ipynb` | Combined bird + drone images | YOLOv8 Large |

## Research Paper

The project is based on the paper: **"Evaluating YOLOv8 Models for Efficient Drone Detection in Anti-UAV Systems"**. The study highlights the growing need for robust anti-UAV systems and performs detailed evaluations of YOLOv8-S and YOLOv8-L on real-world datasets.

## Datasets

Two datasets were used:

* **Drone Dataset:** Contains annotated drone images.
* **Combined Dataset:** Contains both drone and bird images to test the model's ability to distinguish between drones and visually similar objects.

Dataset source: [Roboflow Drone Detection Dataset](https://universe.roboflow.com/lagari-team/drone-tespit/dataset/3)

## Methodology

* **Model Variants:**

  * **YOLOv8-S:** Optimized for speed and efficiency on low-resource devices.
  * **YOLOv8-L:** Designed for high accuracy, with a deeper architecture.

* **Training Details:**

  * Images resized to 640x640 pixels.
  * Datasets split into training, validation, and test sets.

* **Evaluation Metrics:**

  * Precision
  * Recall
  * F1 Score
  * Mean Average Precision (mAP\@0.5)
  * Accuracy

## Results Overview

**Drone-only Dataset:**

* YOLOv8-S showed superior precision and recall on resource-constrained hardware, making it ideal for real-time detection.
* YOLOv8-L achieved better performance in more complex scenarios but required higher computational resources.

**Combined Dataset:**

* YOLOv8-S excelled in precision when distinguishing drones from birds.
* YOLOv8-L offered balanced results with higher recall and robustness in cluttered environments.

## Hardware Used

* **NVIDIA Tesla T4 (16GB VRAM)**
* **NVIDIA RTX 4050 (6GB VRAM)**

## How to Run

1. Clone the repository.
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Open the desired notebook (e.g., `Drone_S.ipynb`) in Jupyter Lab/Notebook.
4. Follow the notebook cells to reproduce the results.

## Key Findings

* **YOLOv8-S:** Best suited for real-time applications where speed is critical.
* **YOLOv8-L:** Recommended for scenarios prioritizing detection accuracy, especially in diverse and noisy environments.

## Future Work

* Implement ensembling techniques using YOLOv8-S, YOLOv8-M, and YOLOv8-L.
* Explore additional post-processing methods such as Non-Maximum Suppression and Weighted Boxes Fusion to further reduce false positives.

## Authors

* Kushaj Pavankumar Solanki
* Puneet Verma
* Prof. Suresh Dara

## Acknowledgments

* [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
* [Roboflow](https://roboflow.com)

---

*This project contributes to the advancement of real-time anti-UAV detection systems, balancing precision and performance to meet diverse operational requirements.*
