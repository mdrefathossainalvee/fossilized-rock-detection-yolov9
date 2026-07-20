# Fossilized Rock Detection using YOLOv9

A deep learning-based object detection model for detecting **Fossilized Rock** objects using **YOLOv9** trained on a custom Roboflow dataset.

---

## Project Overview

This project implements an object detection model capable of detecting fossilized rocks from images. The model was trained using the YOLOv9 framework on a custom dataset prepared with Roboflow.

The objective of this project is to provide an efficient detection system that can assist researchers, students, and geological applications in automatically locating fossilized rocks within images.

---

## Features

- Custom YOLOv9 Object Detection
- Trained on Roboflow Dataset
- Fast inference
- Bounding Box Detection
- Confidence Score Prediction
- Easy deployment
- COCO checkpoint initialization

---

## Dataset Information

| Property | Value |
|----------|--------|
| Dataset | Fossilized Rock Detection |
| Images | **2,286** |
| Classes | 1 |
| Class Name | Fossilized rock |
| Annotation Tool | Roboflow |
| Dataset Version | 1 |

---

## Model Information

| Property | Value |
|----------|--------|
| Framework | YOLOv9 |
| Platform | Roboflow |
| Model Type | Roboflow 3.0 Object Detection (Fast) |
| Checkpoint | COCO |
| Model Version | rock-detection-vosuz/1 |
| Updated | February 7, 2026 |

---

## Training Metrics

### Test Set Performance

| Metric | Score |
|---------|-------|
| mAP@50 | **18.6%** |
| Precision | **24.0%** |
| Recall | **18.2%** |
| F1 Score | **20.7%** |

---

## Training Curves

The training process includes monitoring of:

- Box Loss
- Classification Loss
- Distribution Focal Loss (DFL)
- Precision
- Recall
- Validation Loss
- mAP@50
- mAP@50-95

Example training visualization:

```
results.png
```

---

## Prediction Example

Example inference output:

```json
{
  "predictions": [
    {
      "x": 137,
      "y": 96.5,
      "width": 264,
      "height": 181,
      "confidence": 0.679,
      "class": "Fossilized rock",
      "class_id": 0,
      "detection_id": "9933e36b-6dcc-43aa-bfa0-33ed98906495"
    }
  ]
}
```

---

## Project Structure

```
fossilized-rock-detection-yolov9/
│
├── dataset/
│   ├── train/
│   ├── valid/
│   └── test/
│
├── weights/
│   └── best.pt
│
├── runs/
│   └── detect/
│
├── results.png
├── predict.py
├── train.py
├── requirements.txt
├── data.yaml
└── README.md
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/yourusername/fossilized-rock-detection-yolov9.git

cd fossilized-rock-detection-yolov9
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Training

```bash
python train.py
```

or using YOLOv9

```bash
python train.py \
--data data.yaml \
--weights yolov9-c.pt \
--epochs 100 \
--img 640
```

---

## Inference

Run prediction

```bash
python detect.py \
--weights weights/best.pt \
--source image.jpg
```

---

## Example Output

Detected Object

```
Class:
Fossilized rock

Confidence:
67.9%

Bounding Box:
x = 137
y = 96.5
width = 264
height = 181
```

---

## Applications

- Geological Surveys
- Paleontology Research
- Educational Projects
- Fossil Identification
- Rock Classification Systems
- Museum Digitization
- Field Exploration

---

## Performance Analysis

The model successfully learns the target object but demonstrates relatively modest detection performance on the test dataset.

Observed metrics:

- Precision: 24.0%
- Recall: 18.2%
- mAP@50: 18.6%

Possible improvements include:

- Increasing dataset size
- Improving annotation quality
- Applying stronger data augmentation
- Training for additional epochs
- Hyperparameter optimization
- Multi-scale training
- Higher-resolution images
- Better class balancing

---

## Technologies Used

- Python
- YOLOv9
- Roboflow
- PyTorch
- OpenCV
- NumPy

---

## Citation

If you use this project in your research, please cite this repository.

```
@software{fossilized-rock-detection,
title={Fossilized Rock Detection using YOLOv9},
author={Your Name},
year={2026}
}
```

---

## License

This project is released under the MIT License.

---

## Acknowledgements

- Roboflow
- YOLOv9
- PyTorch
- COCO Dataset
