🌾 Crop and Weed Detection Using YOLOv8
AI-based Precision Spraying System for Sesame Crop Farming
📌 Problem Statement

Weeds are unwanted plants that grow along with crops and consume essential resources such as water, nutrients, land area, and sunlight.
This leads to reduction in crop productivity and farmers commonly remove weeds using pesticides.

❌ When pesticides are sprayed over the entire field:

They may stick to crops

Cause harmful effects on human health

Increase cost due to wastage

Pollute soil and environment

✅ Therefore, a smart AI system is needed which can:

✔ Detect only weeds
✔ Spray pesticides only on detected weed areas
✔ Protect crop quality
✔ Reduce pesticide usage and cost
✔ Improve yield in a sustainable manner

🎯 Project Aim

"To develop an automated system that detects weeds separately from sesame crops and enables targeted pesticide spraying only on weeds to reduce chemical usage and increase crop productivity." 

Project5_Ag_Crop and weed detec…

📊 Dataset Creation Process

This dataset was fully manually created on farmland:

Step	Work Done	Final Count
1️⃣ Data Collection	Photos captured of sesame crops & multiple weed types using a mobile camera	589 images
2️⃣ Data Cleaning	Removed irrelevant, blurry & low-quality images	546 usable images
3️⃣ Image Processing	Resized from 4000×3000 → 512×512×3 for faster training	546 processed images
4️⃣ Data Augmentation	Keras ImageDataGenerator used to increase dataset size	1300 total images
5️⃣ Manual Labeling	Bounding boxes drawn manually for 2 classes: crop, weed	1300 label files

✅ Labels are in YOLO format (one .txt per image)

📌 Reference: Official file uploaded by user 

Project5_Ag_Crop and weed detec…

✅ Dataset Information
Attribute	Details
Crop Targeted	Sesame Crop 🌿
Total Images	1300
Classes	Crop (0), Weed (1)
Image Type	512×512 RGB
Annotation	YOLO Bounding Box
✅ Dataset Split Used
Subset	Images	Purpose
Train	1191	Model training
Validation	468	Tuning & validation
Test	241	Final evaluation
📂 Dataset Access (Drive)

Large dataset stored in Google Drive:
🔗 https://drive.google.com/drive/folders/1gXHhca3nVFl0ESO4osN1hAzSkSknRA9D?usp=sharing

Dataset folder structure:
Crop_weed_model2
├──weight/best.pt+last.pt
├──result.csv+args.yaml
└──more
dataset/
├── train/images + labels
├── val/images + labels
└── test/images + labels
result/
└──detection_result.zip
data.aml

🧠 Model Used

⚡ YOLOv8 (Ultralytics)
Reason for selection:

✅ Fast real-time detection
✅ High accuracy
✅ Best performance on small objects like weeds

🚀 Training Details
Parameter	Value
Model	YOLOv8n.pt
Epochs	50
Image Size	512
Batch Size	8

Command:

from ultralytics import YOLO
model = YOLO("yolov8n.pt")
model.train(data="data/data.yaml", epochs=50, imgsz=512)

✅ Output Results
Metric	Score
Precision	0.84
Recall	0.85
mAP50	0.90
mAP50-95	0.63

💡 Indicates strong detection quality under real farm conditions

✅ Sample outputs in folder: /results/detection_samples/

▶ Testing / Inference
model = YOLO("weights/best.pt")
model.predict(source="test.jpg", save=True)


Prediction results saved in:

runs/detect/predict/

🏆 Key Outcomes

✔ Accurate weed-crop separation
✔ Helps reduce chemical waste
✔ Improves food quality & yield
✔ Can integrate with spraying robots/drones
✔ Provides smart farming at low cost

🏢 Internship Details
Field	Details
Student	Kakde Pavan Balasaheb
Roll No.	10
Dept.	E&TC (TY Diploma)
College	Bhivarabai Sawant Polytechnic
Organization	UniConverge Technology
Duration	Sept 2025 – Nov 2025
📝 Documents Available
File	Folder
Internship Report (DOCX / PDF)	docs/
Presentation (PPT)	docs/
Code Notebook	notebooks/
Model Weights	weights/
Sample Predictions	results/detection_samples/
🔮 Future Scope

🚜 Drone-based weed spraying
📡 Live real-time field detection
🌾 Support for multiple crop types

✅ Conclusion

This project proves that AI can solve major agricultural problems
by detecting weeds & enabling selective pesticide spraying 🌱

➡ Saves money
➡ Improves crop yield
➡ Protects environment ✅

🌾 AI for Smarter & Safer Farming 🚜

✅ This version now includes EVERY actual detail from your official problem document!
✅ 100% ready for GitHub + Internship evaluation submission
