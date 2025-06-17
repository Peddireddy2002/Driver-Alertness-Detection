# 🚗 Driver Alertness Detection

This project aims to detect driver alertness in real-time using computer vision and machine learning techniques. It helps improve road safety by identifying signs of drowsiness or distraction and alerting the driver before incidents occur.

---

📊 **Dataset Overview**  
The dataset consists of video frames/images of drivers exhibiting various states.

**Features Include:**  
- **Facial Landmarks**: Eye aspect ratio (EAR), blink frequency  
- **Head Poses**: Yaw, pitch, roll  
- **Eye and Mouth Movements**: Open/close states, yawning detection  
- **Target Variable**: Alertness state (Alert, Drowsy, Distracted)

---

🧹 **Data Preprocessing & Feature Extraction**

- **Frame Extraction** from video clips into individual images  
- **Face Detection** using Haar cascades / Dlib  
- **Landmark Detection** to compute eye and mouth metrics  
- **Feature Computation**:  
  - Eye Aspect Ratio (for blink detection)  
  - Mouth opening ratio (for yawning)  
  - Head pose angles (from landmarks)  
- **Data Cleaning**: Filtered frames without face detection

---

📈 **Exploratory Data Analysis (EDA)**

- Visualized EAR and mouth ratio distributions across alertness states  
- Examined threshold values for blinks and yawns  
- Plotted time-series plots of EAR during alerts vs. drowsiness  
- Analyzed head pose angle distributions to detect distraction patterns

---

🤖 **Model Building & Evaluation**

**Classification Algorithms Used:**  
- Random Forest  
- Support Vector Machine (SVM)  
- Multi-Layer Perceptron (MLP)  

**Evaluation Strategy:**  
- Split dataset into train/test sets  
- Measured performance using:  
  - Accuracy  
  - Precision / Recall / F1-Score  
  - Confusion Matrix  
- Deployed early-warning logic based on sliding-window EAR thresholds

---

✅ **Results & Insights**

- **Best Model Accuracy**: ~88% (Random Forest)  
- EAR thresholds successfully detected fatigue-related blinks  
- **Important Features Highlighted:**  
  - Eye Aspect Ratio (EAR)  
  - Mouth opening ratio (yawn detection)  
  - Head pose roll/pitch  
- **Real-World Impact:**  
  - Built a proactive alert system for driver safety  
  - Useful in fleet monitoring and consumer driving assistants

---

🛠️ **Tools & Technologies**

- **Python**  
- **OpenCV**, **Dlib** – Face detection & landmark extraction  
- **Pandas**, **NumPy** – Data handling  
- **Scikit-learn** – Modeling & evaluation  
- **Matplotlib**, **Seaborn** – Visualization  
- **Jupyter Notebook / scripts**

---

📚 **Conclusion**

This project showcases a fully functional pipeline to detect driver drowsiness and distraction using interpretable facial features. By integrating computer vision and ML, it offers a scalable solution to enhance vehicular safety.

---

📌 **Future Improvements**

- Use deep learning for more robust face and fatigue detection (e.g., CNNs, LSTM)  
- Implement a real-time alert system (e.g., audio / visual cues triggered during driving)  
- Test and refine with real-world driving data  
- Optimize performance for edge deployment (e.g., Raspberry Pi, NVIDIA Jetson)
