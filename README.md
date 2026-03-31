📟 #PCB Defect Detection with YOLOv8n

Detection and localization of six types of PCB defects using the lightweight YOLOv8n model.

This project aims to automate printed circuit board (PCB) inspection, reducing manual effort and improving defect detection accuracy in manufacturing workflows.

📌 Overview
🔍 Object detection model: YOLOv8n
🧩 Task: Multi-class defect detection
🖼 Dataset: DeepPCB (~700 annotated images)
⚡ Focus: Speed, efficiency, and real-time inference
🐞 Detected Defects

The model detects the following defect classes:

Class	Description
missing_hole	Missing drilled hole
mouse_bite	Edge erosion or irregular cuts
open_circuit	Broken connection
short	Unintended connection
spur	Small copper protrusion
spurious_copper	Unwanted copper residue
📊 Dataset

We use the DeepPCB dataset, which contains annotated PCB images with labeled defects.

🔗 https://www.kaggle.com/datasets/akhatova/pcb-defects

🖼 Results

Replace this image with your actual model output.

✨ Features
✅ XML → YOLO format conversion
✅ Training pipeline using YOLOv8n
✅ Visualization of annotations and predictions
✅ Inference on custom images
✅ Dataset statistics (class distribution, bbox sizes)
🛠 Installation
git clone https://github.com/tonusername/pcb-defect-detection-yolov8.git
cd pcb-defect-detection-yolov8
pip install -r requirements.txt
🚀 Usage
1. Train the model
yolo detect train data=data.yaml model=yolov8n.pt epochs=50 imgsz=640
2. Run inference
yolo detect predict model=runs/detect/train/weights/best.pt source=path/to/image.jpg
3. Visualize results

Predictions will be saved in:

runs/detect/predict/
📈 Example Metrics (to update)
Metric	Value
mAP@0.5	XX%
Precision	XX%
Recall	XX%
📁 Project Structure
pcb-defect-detection-yolov8/
│── data/
│── notebooks/
│── scripts/
│── runs/
│── data.yaml
│── requirements.txt
│── README.md
🔧 Requirements
Python 3.8+
PyTorch
Ultralytics YOLOv8

Install dependencies:

pip install -r requirements.txt
💡 Future Improvements
📦 Train with larger datasets
🎯 Hyperparameter tuning
⚙️ Deploy as a web app (Streamlit / FastAPI)
🧪 Model comparison (YOLOv5, YOLOv9, etc.)
📜 License

This project is licensed under the MIT License.

🙌 Acknowledgments
DeepPCB dataset creators
Ultralytics YOLOv8
