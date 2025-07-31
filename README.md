# 🚦 Road Sign Detection Using YOLOv8

A real-time road sign detection system using YOLOv8 and Roboflow dataset. This project helps identify road signs and enhances safety by providing alerts for missed signs.

## 🔧 Tech Stack

- Python
- YOLOv8 (Ultralytics)
- OpenCV
- Roboflow
- Torch, torchvision

## 🗂️ Dataset

The dataset was obtained and preprocessed using Roboflow, containing 91 road sign categories.

Folder structure:
```
📁 train/
📁 valid/
📁 test/
```

## 📌 Model Training

Model used: `yolov8n.pt` (Nano model from Ultralytics)

```python
from ultralytics import YOLO

model = YOLO("yolov8n.pt")  # Or use yolov8s.pt or yolov8m.pt
model.train(data="custom_data.yaml", epochs=50)
```

⚠️ **Note:**  
The original `dataset.yaml` and trained model weights (`best.pt`) were deleted after training.  
You can regenerate them from Roboflow or retrain using the code in `roboflow.ipynb`.

## 🔍 Installation

```bash
pip install torch torchvision torchaudio opencv-python ultralytics
```

## 🖼️ Example Output

![Detection Example](images/sample_output.jpg)

## 📁 File Descriptions

| File | Description |
|------|-------------|
| `roboflow.ipynb` | Training notebook using Roboflow + YOLOv8 |
| `images/` | Sample predictions and visualizations |
| `README.md` | Project description |
| `requirements.txt` | Required dependencies |

## 👩‍💻 Author

**Jeevitha**  
🔗 [GitHub - j-jeevitha](https://github.com/j-jeevitha)