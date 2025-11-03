# Crop-and-weed-detection-sing-YOLO-model
AI Based Selective Spraying System which detects that whether it is crop or weed
# Crop and Weed Detection Using YOLOv8 🌾🔍

This project aims to detect crops and weeds in farmland images using a YOLOv8 deep learning model. 
It supports smart agriculture by enabling targeted pesticide spraying only on weeds, reducing cost and environmental impact.

---

## 🚜 Project Background
Weeds consume essential nutrients, water, and sunlight meant for crops, reducing agricultural productivity.  
Farmers typically remove weeds using pesticides which may affect crop quality and human health.

This system identifies weeds separately and ensures pesticides are applied only where needed ✅

---

## 🧠 Tech Stack & Tools Used
| Component | Technology Used |
|----------|------------------|
| Model | YOLOv8 |
| Language | Python |
| Platform | Google Colab |
| Imaging | OpenCV |
| Dataset | Custom Crop/Weed Dataset |
| Annotation | Roboflow |

---

## 📁 Dataset
The dataset contains:
✅ 1300 images  
✅ YOLO format labels  
✅ 512×512 resolution  
✅ Crops and different weeds

---

## 🔧 Model Training

Model Performance (Results)
MetricScorePrecision0.84Recall0.85mAP500.90mAP50-950.63
🔹 Good detection accuracy
🔹 Works in real farmland conditions

🖼 Sample Outputs
📌 See folder → results/detection_samples/

📌 How to Run Inference
from ultralytics import YOLO
model = YOLO("weights/best.pt")
model.predict(source="test.jpg", save=True)


🏢 Internship Details
FieldDetailsStudent NameKakde Pavan BalasahebRoll No.10Course & YearTY Diploma - E&TCCollegeBhivarabai Sawant Polytechnic (JSPM)OrganizationUmiConverge TechnologyProject DurationSept 2025 – Nov 2025DomainArtificial Intelligence in Agriculture

🏁 Conclusion
The project successfully detects weeds in crop fields and helps automate weed removal.
This can greatly reduce pesticide usage and enable sustainable farming 🚜🌱

⭐ Future Scope
✅ Drone-based Weed Spraying
✅ Mobile App Integration
✅ Real-time Field Detection

✅ Project Completed Successfully 👍

---
