
# Vehicle Detection and Traffic Counting Using YOLOv8 and ByteTrack

## 1. Introduction

This project develops an AI-based traffic monitoring system that detects, tracks, classifies, and counts vehicles in traffic videos using YOLOv8, ByteTrack, and OpenCV.

## 2. Objectives

- Detect vehicles in traffic videos.
- Classify cars, motorcycles, buses, and trucks.
- Track vehicles using unique tracking IDs.
- Count vehicles crossing a virtual counting line.
- Reduce duplicate counting.
- Export traffic counting results.

## 3. Technologies

- Python
- YOLOv8 (Ultralytics)
- ByteTrack
- OpenCV
- Google Colab
- Pandas and NumPy

## 4. Methodology

The system follows these steps:

1. Load a pretrained YOLOv8n model.
2. Read the input traffic video.
3. Detect vehicles in each frame.
4. Track vehicles using ByteTrack.
5. Detect vehicle crossings over a virtual line.
6. Apply duplicate-count filtering.
7. Export the processed video and CSV results.

The project uses pretrained YOLOv8 weights. No custom model training or fine-tuning was performed.

## 5. Experimental Results

The final V5.1 system was evaluated using a 13.62-second traffic video.

| Vehicle Type | Manual Count | AI Count |
|---|---:|---:|
| Car | 7 | 6 |
| Motorcycle | 41 | 39 |
| Truck | 1 | 1 |
| Bus | 1 | 0 |
| **Total** | **50** | **46** |

- Absolute counting error: **8%**
- Aggregate count agreement: **92%**

The reported agreement measures the difference between total vehicle counts. It does not represent object detection accuracy, precision, or recall.

## 6. How to Run

1. Open Google Colab.
2. Upload `Vehicle_Counting_V5_1_Code_Only.ipynb`.
3. Enable T4 GPU if available.
4. Run the notebook cells in order.
5. Upload a traffic video when prompted.
6. Review and download the output files.

## 7. Limitations

- Some vehicles may be missed or misclassified.
- Occlusion and tracking ID switches can affect counting.
- Results depend on camera position and counting-line placement.
- Evaluation was conducted on a short traffic video.

## 8. References

- [Ultralytics YOLOv8](https://docs.ultralytics.com/models/yolov8/)
- [Ultralytics Object Tracking](https://docs.ultralytics.com/modes/track/)
- [COCO Dataset](https://cocodataset.org/)
- [ByteTrack Paper](https://arxiv.org/abs/2110.06864)

## 9. Project Status

Final academic project version: V5.1

This repository contains an AI-based vehicle detection, tracking, and traffic counting implementation.
