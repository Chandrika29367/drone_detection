# Deep Learning-Based Aerial Object Detection and Drone Classification

This project implements a **two-stage deep learning framework** for detecting airborne objects and classifying drone types in real-time using **YOLOv8** and **ResNet-DeiT**.

---

## Stage 1: YOLOv8

- Detects airborne objects such as drones, birds, airplanes, and helicopters.  
- Outputs bounding boxes with confidence scores for each detected object.

## Stage 2: ResNet-DeiT

- Classifies the type of drone (e.g., DJI Phantom, DJI Mavic, DJI Inspire).  
- Ensures accurate identification for enhanced airspace security.

---

## Key Features

- Detects multiple airborne objects in images or video streams.  
- Classifies drones into specific models after detection.  
- Provides real-time alert notifications for detected drones.  
- Robust under varied lighting, motion blur, and altitude conditions.  
- Scalable for real-world airspace monitoring and automated surveillance.

---

## Tools & Libraries

- **Python 3.12**  
- **Ultralytics YOLOv8 (v8.4.27)**  
- **PyTorch 2.10**  
- **ResNet-DeiT** for drone classification  
- **OpenCV, NumPy, Pandas**  
- **Streamlit** (for real-time visualization)  
- **Twilio API** (for automated SMS alerts)  

---

## Datasets

| Dataset | Source | Resolution | Classes | Images |
|---------|--------|------------|--------|--------|
| Aerial Object Detection (AOD) | Kaggle | 640×640 | Drone, Bird, Aircraft, Helicopter | 15,000 |
| Drone Classification | Kaggle | 480p–1080p | DJI Phantom, DJI Mavic, DJI Inspire | 8,002 |

- Images converted to **YOLO text format** for model compatibility.  
- Dataset split: **70% training, 20% validation, 10% testing**.  
- Data augmentation applied to improve model generalization.

## Project Structure
AOD4-YOLOv8/

├── detection.ipynb # Detects aerial objects with YOLOv8

├── classification.ipynb # Classifies drone type with ResNet-DeiT

├── data.yaml # YOLOv8 dataset configuration

├── requirements.txt # Python dependencies

├── README.md

└── runs/ # YOLOv8 output (weights, logs)


---

## Methodology

1. **Preprocessing**  
   - Normalize images to 640×640.  
   - Apply data augmentation.  
   - Convert annotations to YOLO format.

2. **Detection (YOLOv8)**  
   - Detect drones, birds, helicopters, and airplanes in images or video frames.

3. **Drone Classification (ResNet-DeiT)**  
   - Classify drone models after detection.

4. **Visualization & Alerts**  
   - Display results with bounding boxes and confidence scores using Streamlit.  
   - Send real-time SMS alerts via Twilio API.

---

## Performance

- **YOLOv8 + ResNet-DeiT achieved:**  
  - mAP@0.5: 96.76%  
  - High precision and recall across challenging scenarios (low light, motion blur, high altitude).  
- Outperforms Faster R-CNN and EfficientDet-D1 in real-world aerial detection tests.

---

## References

- [AOD4 Dataset on Kaggle](https://www.kaggle.com/datasets)  
- [Drone Type Classification Dataset on Kaggle](https://www.kaggle.com/datasets)
---


