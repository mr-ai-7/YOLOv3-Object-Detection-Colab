# YOLOv3-Object-Detection-Colab
# 🎯 YOLOv3 Object Detection in Google Colab

This repository demonstrates how to implement **YOLOv3-based object detection** for **static videos** using OpenCV and Python inside **Google Colab**. It supports detection of common objects using the **COCO dataset** and generates a processed video with bounding boxes and class labels.

---

## 📁 Repository Name

**YOLOv3-Object-Detection-Colab**

---

## 📌 Features

- ✅ Real-time object detection using **YOLOv3**
- ✅ Class-wise **Non-Maximum Suppression (NMS)** to filter overlapping boxes
- ✅ Bounding box annotation with **confidence scores**
- ✅ Output visualization and video generation using **FFmpeg**
- ✅ Works seamlessly in **Google Colab**

---

## 🧠 Technologies Used

- Python
- OpenCV
- NumPy
- YOLOv3 (Darknet)
- FFmpeg (for video conversion)
- Google Colab (runtime environment)

---

## 🎥 Sample Output

The pipeline processes a video frame-by-frame, detects objects with YOLOv3, and displays/exports the result with bounding boxes and labels.

---

## 🛠️ How It Works

### 1️⃣ Load YOLOv3 Model

```python
yolo = cv2.dnn.readNetFromDarknet("yolov3.cfg", "yolov3.weights")
```

### 2️⃣ Read and Process Video

```python
cap = cv2.VideoCapture("video.mp4")
```

### 3️⃣ Perform Object Detection

```python
blob = cv2.dnn.blobFromImage(...)
yolo.setInput(blob)
layer_outputs = yolo.forward(...)
```

### 4️⃣ Apply Class-wise NMS

```python
cv2.dnn.NMSBoxes(...)
```

### 5️⃣ Display and Save Output

```python
cv2.rectangle(...)  # Draw bounding box
out.write(frame)    # Save frame to video
```

---

## 📂 Folder Structure

```
├── yolov3.cfg
├── yolov3.weights
├── coco.names
├── video3.mp4
├── output.avi
├── output.mp4
└── YOLOv3_Object_Detection.ipynb
```

---

## 📦 Requirements

Ensure these files are available:
- `yolov3.cfg`
- `yolov3.weights` (can be downloaded from official YOLO site)
- `coco.names`
- Sample video file (`video3.mp4`)

---

## 🚀 Run in Google Colab

Just upload all the required files and run the notebook line by line. The 10th frame will be shown as a preview, and the processed video will be available in MP4 format.

---
