# 🌍 TH-PM2.5-Machine-Learning-Analysis

**Thai PM2.5 Air Quality Prediction using Machine Learning**

วิเคราะห์และพยากรณ์ระดับมลพิษทางอากาศ PM2.5 ในประเทศไทย ด้วยการใช้เทคนิค Machine Learning

---

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Dataset](#dataset)
- [Technologies](#technologies)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Author](#author)

---

## 📊 Project Overview

โปรเจกต์นี้เป็นการศึกษา **การวิเคราะห์ปัจจัยพหุที่มีอิทธิพลต่อมลพิษทางอากาศ (PM2.5)** ในประเทศไทย 
โดยใช้เทคนิคการเรียนรู้ของเครื่อง (Machine Learning) เพื่อ:

✅ ระบุปัจจัยหลักที่มีผลต่อระดับ PM2.5  
✅ สร้างโมเดลพยากรณ์ที่มีความแม่นยำสูง  
✅ วิเคราะห์แนวโน้มมลพิษอากาศในประเทศไทย  
✅ เตรียมข้อมูลเพื่อการตัดสินใจด้านนโยบายสิ่งแวดล้อม

---

## 🎯 Objectives

1. **Data Collection & Preprocessing**
   - รวบรวมข้อมูล PM2.5 จากหลายพื้นที่ในประเทศไทย
   - ทำความสะอาดข้อมูล (Data Cleaning)
   - จัดการค่าที่ขาดหายไป (Missing Values)

2. **Exploratory Data Analysis (EDA)**
   - วิเคราะห์การกระจายตัวของข้อมูล
   - ระบุความสัมพันธ์ระหว่างตัวแปร
   - สร้างกราฟและภาพประกอบ

3. **Feature Engineering**
   - คัดเลือกลักษณะข้อมูลที่สำคัญ
   - สร้างลักษณะข้อมูลใหม่ที่เป็นประโยชน์
   - ปรับขนาดข้อมูล (Scaling & Normalization)

4. **Model Development**
   - ทดลองใช้อัลกอริทึมต่างๆ เช่น:
     - Linear Regression
     - Random Forest
     - Gradient Boosting
     - Support Vector Machine
   - ประเมินประสิทธิภาพโมเดล
   - ปรับแต่งไฮเปอร์พารามิเตอร์ (Hyperparameter Tuning)

5. **Model Evaluation & Validation**
   - ใช้เมตริกต่างๆ: MSE, RMSE, R², MAE
   - Cross-Validation
   - การทดสอบกับชุดข้อมูลทดสอบ

---

## 📁 Dataset

- **Source**: ข้อมูล PM2.5 จากประเทศไทย
- **Size**: ตั้งแต่ปีกี่ถึงปีกี่ (ระบุตามข้อมูลจริง)
- **Features**: ตัวแปรต้น เช่น ความชื้น อุณหภูมิ ความกดอากาศ ฯลฯ
- **Target**: PM2.5 (ค่าความเข้มข้นของฝุ่นละอองขนาดเล็ก)
- **Location**: `/Data_Set/` directory

---

## 🛠 Technologies & Libraries

| Category | Tools |
|----------|-------|
| **Language** | Python 3.8+ |
| **Notebook** | Jupyter Notebook |
| **Data Processing** | pandas, numpy |
| **Data Visualization** | matplotlib, seaborn, plotly |
| **Machine Learning** | scikit-learn |
| **Statistical Analysis** | scipy, statsmodels |

---

## 📂 Project Structure

```
TH-PM2.5-Machine-Learning-Analysis/
├── Data_Set/                          # ชุดข้อมูล
│   ├── raw_data.csv                   # ข้อมูลดิบ
│   └── processed_data.csv             # ข้อมูลที่ประมวลผลแล้ว
│
├── re prove/                          # ผลลัพธ์และทดลอง
│   ├── model_results.pkl
│   └── predictions.csv
│
├── TH-PM2.5-ML-Analysis.ipynb         # Notebook หลัก
├── requirements.txt                   # Dependencies
├── .gitignore                         # Git ignore configuration
└── README.md                          # ไฟล์นี้
```

---

## 🚀 Installation

### Prerequisites
- Python 3.8 หรือสูงกว่า
- pip หรือ conda

### Setup

1. **Clone Repository**
```bash
git clone https://github.com/Munumpa/TH-PM2.5-Machine-Learning-Analysis.git
cd TH-PM2.5-Machine-Learning-Analysis
```

2. **Create Virtual Environment** (Recommended)
```bash
# Using venv
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# หรือ using conda
conda create -n pm25_ml python=3.9
conda activate pm25_ml
```

3. **Install Dependencies**
```bash
pip install -r requirements.txt
```

4. **Run Jupyter Notebook**
```bash
jupyter notebook
```

---

## 📖 Usage

### Step-by-Step Guide

1. **Open Notebook**
   - เปิดไฟล์ `TH-PM2.5-ML-Analysis.ipynb` ใน Jupyter Notebook

2. **Run All Cells**
   - กดปุ่ม "Cell" → "Run All" หรือ Shift+Ctrl+Enter

3. **Explore Results**
   - ดูผลการวิเคราะห์ และกราฟ
   - ตรวจสอบประสิทธิภาพโมเดล

### Key Sections

```
1. Data Loading & Exploration
2. Data Preprocessing & Cleaning
3. Feature Engineering
4. Exploratory Data Analysis (EDA)
5. Model Training & Evaluation
6. Predictions & Visualization
```

---

## 📊 Results

### Model Performance Metrics

| Model | RMSE | MAE | R² Score |
|-------|------|-----|----------|
| Linear Regression | - | - | - |
| Random Forest | - | - | - |
| Gradient Boosting | - | - | - |
| SVM | - | - | - |

*Note: ให้อัปเดตผลลัพธ์จริงจากโปรเจกต์ของคุณ*

### Key Findings

- ปัจจัยหลักที่มีผลต่อ PM2.5:
  - [ปัจจัยที่ 1]
  - [ปัจจัยที่ 2]
  - [ปัจจัยที่ 3]

- แนวโน้มมลพิษ:
  - [สรุปผล 1]
  - [สรุปผล 2]

---

## 📈 Visualization Examples

### PM2.5 Distribution
![Distribution](https://via.placeholder.com/500x300?text=PM2.5+Distribution)

### Feature Correlation
![Correlation](https://via.placeholder.com/500x300?text=Feature+Correlation)

### Model Performance
![Performance](https://via.placeholder.com/500x300?text=Model+Performance)

---

## 🔍 How to Improve

- [ ] เพิ่มข้อมูลจากแหล่งข้อมูลอื่น
- [ ] ทดลองใช้ Deep Learning Models
- [ ] Ensemble Methods
- [ ] Real-time prediction API

---

## 📚 References

- [Scikit-learn Documentation](https://scikit-learn.org/)
- [Pandas Documentation](https://pandas.pydata.org/)
- [Thailand Air Quality Data](https://www.thaiaqi.com/)

---

## 👨‍💻 Author

**Munumpa**  
📧 Email: [your-email@example.com]  
🔗 GitHub: [@Munumpa](https://github.com/Munumpa)  
📌 Portfolio: [your-portfolio-link]

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🤝 Contributing

Pull requests are welcome! ยินดีรับ Pull Requests และ Issues

---

**Last Updated:** August 2026  
⭐ If you find this helpful, please star the repository!