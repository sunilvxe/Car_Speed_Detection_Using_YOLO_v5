# Car Speed Detection Using YOLOv5

🚗 **Real-Time Vehicle Speed Detection using YOLOv5 and OpenCV** 📹

## 📌 **Overview**
This project uses **YOLOv5** (You Only Look Once) for vehicle detection and **OpenCV** for tracking and speed estimation. The detected vehicle speed is displayed in **bold yellow text** on the video.

## 🚀 **Features**
✅ Detects vehicles in a video stream
✅ Tracks moving objects with a simple tracker
✅ Computes vehicle speed using pixel-to-real-world conversion
✅ Displays **bold yellow speed overlay** with smooth anti-aliasing
✅ Supports real-time processing with OpenCV

## 📂 **Project Structure**
```
Yolo_v8/
│── main.py                 # Main script for detection & tracking
│── detected_video.mp4      # Processed output video
│── requirements.txt        # Dependencies
└── input_video # Input video file
```

## 🛠️ **Installation**
Ensure you have Python installed, then run:
```sh
pip install -r requirements.txt
```

## 🏎️ **Run the Project**
```sh
python main.py
```

## 📝 **Code Highlights**
### **Vehicle Speed Calculation**
Speed is calculated based on detected object movement:
```python
speed = real_dist / dt * 3.6 if dt > 0 else 0
```

### **Bold Yellow Text Overlay**
```python
cv2.putText(frame, f'ID {obj_id} {speed:.2f} km/h',
            (int(cx), int(cy)),
            cv2.FONT_HERSHEY_SIMPLEX,
            0.8,  # Font size
            (0, 255, 255),  # Yellow color in BGR
            3,  # Bold text
            cv2.LINE_AA)  # Smooth rendering
```

## 📊 **Output Preview**
The processed video includes **vehicle detections with speed overlays**. The text is **bold & yellow** for better visibility.

## 🤝 **Contributing**
Feel free to fork and improve the project! PRs are welcome. 🚀

## 📜 **License**
This project is open-source under the MIT License.

