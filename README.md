# YOLOv9 for Fire Detection in Industrial Environments  

This repository hosts the source code and supporting materials for a study focused on fire, smoke, and invisible fire detection in industrial environments. The study includes two algorithms and a proposed model designed to enhance real-time hazard detection and integrate IoT-based safety mechanisms.

---

## Overview  

1. **Algorithm 1**: **YOLOv9-Based Detection of Fire, Smoke, and Invisible Fire Hazards in Industrial Video Surveillance**  
   - **Status**: Fully implemented, trained, and evaluated.  
   - **Purpose**: Provides high-accuracy real-time detection of fire and smoke hazards.  

2. **Algorithm 2**: **YOLOv9 with Enhanced IoT Integration for Fire and Smoke Detection**  
   - **Status**: Conceptual design, yet to be implemented.  
   - **Purpose**: Integrates YOLOv9 with IoT devices for improved detection reliability and actionable safety measures.  

3. **Proposed Model**: **Real-Time Deployment Pipeline for YOLOv9 with IoT Sensor Integration**  
   - **Status**: A proposed framework for future implementation.  
   - **Purpose**: To deploy YOLOv9 in real-world industrial environments with enhanced IoT integration.

---

## Datasets  

The first algorithm utilized the following open-source datasets, which collectively include over 13,000 labeled images of fire, smoke, and invisible fire scenarios:  

1. [Fire and Smoke Set 2](https://universe.roboflow.com/dworf-nekitaec-0rxxs/set-2-rlbmu)  
2. [Smoke and Fire](https://universe.roboflow.com/detection-e83li/smokeandfire)  
3. [Fire and Smoke Detection](https://universe.roboflow.com/fire-detector-cqdzi/fire-and-smoke-b5lli/dataset/1)  

### Preprocessing  
- **Augmentation Techniques**: Resizing, flipping, noise injection.  
- **Splitting**: Ensured robust model performance across training, validation, and test datasets.  

---

## Code  

This repository provides code for the following tasks:  

1. **Training**: Train YOLOv9 with the specified datasets for fire and smoke detection.  
2. **Validation**: Evaluate performance metrics such as precision, recall, and mAP.  
3. **Inference**: Detect hazards in real-time using video streams.  

### Getting Started  

1. Clone the repository:  
   ```bash
   git clone https://github.com/YourUsername/yolov9-industrial-detection
   cd yolov9-industrial-detection
 

2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```  

3. Configure dataset paths in `data.yaml`.  

4. Train the model:  
   ```bash
   python train.py --data data.yaml --cfg yolov9.yaml --weights '' --epochs 250
   ```  

5. Test the model:  
   ```bash
   python test.py --data data.yaml --weights best.pt
   ```  

6. Run inference:  
   ```bash
   python detect.py --source video.mp4 --weights best.pt
   ```  

This implementation is based on [YOLOv9](https://github.com/WongKinYiu/yolov9), a state-of-the-art object detection framework.

---

## Results  

### Algorithm 1 Performance  
The YOLOv9 model achieved significant accuracy in detecting fire, smoke, and invisible fires:  

| Metric      | Precision | Recall | mAP@0.5 | mAP@0.5-0.95 |  
|-------------|-----------|--------|---------|--------------|  
| YOLOv9      | 0.906     | 0.864  | 0.884   | 0.732        |  

These results underline its reliability and potential for deployment in industrial environments.  

---

## Future Work  

### Algorithm 2: YOLOv9 with Enhanced IoT Integration  
This algorithm envisions the integration of IoT sensors (e.g., thermal cameras, gas detectors, and smoke alarms) with YOLOv9 for:  
- **False Alarm Reduction**: Sensor data validation for detection accuracy.  
- **Invisible Fire Detection**: Multi-sensor fusion to identify undetectable hazards.  
- **Automated Safety Protocols**: Triggering alarms and initiating safety measures in real-time.  

### Proposed Model: Real-Time Deployment Pipeline  
This model outlines a scalable framework for deploying YOLOv9 in industrial settings:  
- **Edge Computing**: Processes video streams locally for low-latency hazard detection.  
- **IoT Sensor Integration**: Combines video analytics with real-time sensor data.  
- **Automated Responses**: Initiates actions such as activating sprinklers or shutting down equipment during emergencies.  

---

## References  

The datasets and methodologies were developed and implemented using resources from:  
- [Fire and Smoke Set 2](https://universe.roboflow.com/dworf-nekitaec-0rxxs/set-2-rlbmu)  
- [Smoke and Fire Dataset](https://universe.roboflow.com/detection-e83li/smokeandfire)  
- [Fire and Smoke Detection Dataset](https://universe.roboflow.com/fire-detector-cqdzi/fire-and-smoke-b5lli/dataset/1)  
- [YOLOv9 GitHub Repository](https://github.com/WongKinYiu/yolov9)  

For more details, refer to these datasets and the YOLOv9 framework.

---

## Contact  

For further information, feel free to reach out:  
- **deepthumar81@gmail.com**  
