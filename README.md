# การวิเคราะห์ปัจจัยพหุที่มีอิทธิพลต่อมลพิษทางอากาศ (PM2.5) ในประเทศไทย

**Multi-Factor Analysis of Air Pollution (PM2.5) in Thailand Using Machine Learning Techniques**

โครงการวิจัยเชิงบูรณาการเพื่อวิเคราะห์และพยากรณ์ความสัมพันธ์เชิงลึกระหว่างปัจจัยทางอุตุนิยมวิทยา กิจกรรมเศรษฐกิจ และความเข้มข้นของฝุ่น PM2.5 ในประเทศไทย

---

## At a Glance

* **รายวิชา:** CSD3201 การพัฒนาโปรแกรมประยุกต์สำหรับอุปกรณ์เคลื่อนที่
* **สถาบัน:** สาขาวิชาวิทยาการคอมพิวเตอร์และนวัตกรรมข้อมูล คณะวิทยาศาสตร์ มหาวิทยาลัยเทคโนโลยีสุรนารี
* **ชุดข้อมูล:** ข้อมูลบูรณาการรายเดือนครอบคลุมระยะเวลา 5 ปี (พ.ศ. 2563-2567) จากเว็บไซต์การกลาง
* **ผลลัพธ์สำคัญ:** ปัจจัยทางอุตุนิยมวิทยา (ปริมาณน้ำฝน ความชื้นสัมพัทธ์ อุณหภูมิ) และ ปัจจัยทางสังคมเศรษฐกิจ (จำนวนประชากร ปริมาณรถยนต์ โรงงาน) มีอิทธิพลต่อความเข้มข้นของ PM2.5 อย่างมีนัยสำคัญ

---

## Table of Contents

- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Dataset & Features](#dataset--features)
- [Technologies & Libraries](#technologies--libraries)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage Guide](#usage-guide)
- [Key Research Findings](#key-research-findings)
- [How to Improve](#how-to-improve)
- [Project Authors](#project-authors)

---

## Project Overview

ในปัจจุบันประเทศไทยกำลังเผชิญกับวิกฤตการณ์ทางสิ่งแวดล้อมจากปัญหาฝุ่นละอองขนาดเล็ก (PM2.5) ที่มีแนวโน้มเพิ่มสูงขึ้นในฤดูหนาว โดยเฉพาะในภาคเหนือ ซึ่งเป็นปัญหาสุขภาพสาธารณะที่สำคัญ

เนื่องจากแหล่งกำเนิดมลพิษมีความซับซ้อนและกระจายตัวอยู่ทั่วประเทศ โครงการนี้จึงใช้เทคนิคการเรียนรู้ของเครื่อง (Machine Learning) เพื่อระบุและวัดปริมาณอิทธิพลของปัจจัยต่างๆ ที่มีความเกี่ยวข้องกับความเข้มข้นของ PM2.5 ข้อมูลที่ได้สามารถนำไปใช้ในการสนับสนุนการตัดสินใจด้านนโยบายสิ่งแวดล้อม

---

## Objectives

1. **Data Integration & Preprocessing:** รวบรวมและทำความสะอาดข้อมูลดิบ (Data Cleaning) จัดการค่าสูญหาย และการกรองข้อมูลที่มีความผิดปกติ

2. **Exploratory Data Analysis (EDA):** ศึกษารูปแบบการกระจายตัวของฝุ่น PM2.5 และวิเคราะห์ความสัมพันธ์สหสัมพันธ์ระหว่างตัวแปรอิสระและตัวแปรเป้าหมาย

3. **Model Development:** พัฒนาและเปรียบเทียบโมเดลการเรียนรู้ของเครื่องเพื่อคาดการณ์ความเข้มข้นของ PM2.5 ด้วยความแม่นยำสูงสุด

4. **Policy Decision Support:** สร้างชุดข้อมูลเชิงประจักษ์เพื่อสนับสนุนการตัดสินใจและวางแผนนโยบายด้านสิ่งแวดล้อ��และสุขภาพสาธารณะ

---

## Dataset & Features

ชุดข้อมูลผ่านการบูรณาการข้อมูลดิบรายเดือนเชิงพื้นที่จากเว็บไซต์ภาคมหาวิทยาลัยและหน่วยงานภาครัฐ

### 1. ข้อมูลคุณลักษณะ (Features)

* `Year` / `Month` / `Province`: ข้อมูลระบุเวลาและเชิงพื้นที่ของการบันทึก

* `Total_Population`: จำนวนประชากรและความหนาแน่นของประชากร ดัชนีชี้วัดกิจกรรมทางเศรษฐกิจและการบริโภค

* `Total_Vehicles`: ปริมาณรถยนต์จดทะเบียนสะสม สะท้อนอัตราการใช้เชื้อเพลิงฟอสซิลที่ส่งผลต่อการปล่อยมลพิษ

* `New_Factories`: จำนวนโรงงานอุตสาหกรรมที่ประกอบกิจการใหม่หรือขยายตัว ดัชนีการปล่อยมลพิษจากภาคอุตสาหกรรม

* `Rainfall`: ปริมาณน้ำฝนสะสม ปัจจัยทางธรรมชาติในการชะล้างฝุ่นละอองในอากาศ

* `Humidity`: ความชื้นสัมพัทธ์ ส่งผลต่อการลดหรือเพิ่มการกระเจริงตัวของฝุ่น

* `Temperature`: อุณหภูมิเฉลี่ย ซึ่งมีความเกี่ยวข้องกับการเคลื่อนตัวของฝุ่นและการเกิดปฏิกิริยาเคมีในอากาศ

### 2. ตัวแปรเป้าหมาย (Target)

* `PM2.5`: ค่าเฉลี่ยความเข้มข้นของฝุ่นละอองขนาดเล็กไม่เกิน 2.5 ไมครอน (วัดเป็นหน่วย µg/m³)

---

## Technologies & Libraries

| หมวดหมู่ | เครื่องมือที่เลือกใช้ |
| :--- | :--- |
| **Language** | Python 3.8+ |
| **Environment** | Jupyter Notebook |
| **Data Processing** | Pandas, NumPy |
| **Data Visualization** | Matplotlib, Seaborn, Plotly |
| **Machine Learning** | Scikit-learn (Linear Regression, Random Forest, Gradient Boosting, SVM) |
| **Statistical Analysis** | SciPy, StatsModels |

---

## Project Structure

```
TH-PM2.5-Machine-Learning-Analysis/
├── Data_Set/
│   ├── Final_AirQuality_Dataset.csv    # ข้อมูลดิบที่รวมรวมจากการ Preprocessing
│   ├── AirQuality_Final.csv            # ข้อมูลสมบูรณ์ที่พร้อมสำหรับการ Train โมเดล
│   ├── Cleaned_PM25_MonthlyV3.csv      # ข้อมูล PM2.5 จำแนกรายเดือนเชิงพื้นที่
│   └── Cleaned_Rainfall_Monthly.csv    # ข้อมูลปริมาณน้ำฝนเชิงสถิติรายเดือน
├── model_results/
│   ├── model_results.pkl               # ตัวแบบที่ผ่านการ Tuning แล้ว
│   └── predictions.csv                 # ผลการทำ Prediction ของชุดข้อมูลทดสอบ
├── TH-PM2.5-ML-Analysis.ipynb          # Jupyter Notebook หลักในการวิเคราะห์และรันโมเดล
├── requirements.txt                    # รายการ Library และ Dependencies
├── .gitignore                          # ไฟล์ตั้งค่าการเชื่อมของ Git
└── README.md                           # เอกสารอธิบายโครงการวิจัยฉบับนี้
```

---

## Installation

### 1. Prerequisites

- Python 3.8 หรือสูงกว่า
- pip หรือระบบจัดการแพ็กเกจ conda

### 2. Setup Step-by-Step

```bash
# 1. Clone Repository
git clone https://github.com/Munumpa/TH-PM2.5-Machine-Learning-Analysis.git
cd TH-PM2.5-Machine-Learning-Analysis

# 2. Create Virtual Environment
python -m venv venv
source venv/bin/activate  # สำหรับ Windows ใช้: venv\Scripts\activate

# 3. Install Dependencies
pip install -r requirements.txt

# 4. Open Jupyter Notebook
jupyter notebook
```

---

## Usage Guide

เปิดไฟล์ `TH-PM2.5-ML-Analysis.ipynb` ผ่านทางหน้าต่าง Jupyter Workspace

ดำเนินการรันคำสั่งตามลำดับโครงสร้างหลักของ Notebook ดังนี้:

1. **Section 1: Data Loading & Exploration** - โหลดและสำรวจชุดข้อมูล

2. **Section 2: Data Preprocessing & Cleaning** - จัดการค่าว่างและการกรองข้อมูลตัวแปรต้น

3. **Section 3: Feature Engineering & Scaling** - สร้างคุณลักษณะใหม่และทำการปรับขนาด

4. **Section 4: Exploratory Data Analysis (EDA)** - วิเคราะห์รูปแบบและหากราฟสหสัมพันธ์

5. **Section 5: Model Training & Hyperparameter Tuning** - เทรนโมเดลและปรับแต่งพารามิเตอร์

6. **Section 6: Predictions & Evaluation Metrics** - ทำการพยากรณ์และประเมินผลการทำงาน

หากต้องการตรวจสอบผลการประเมินแบบ Cross-Validation ให้ตรวจสอบค่าพารามิเตอร์ใน Section 5

---

## Key Research Findings

### Critical Insights จากงานวิจัย

* **อิทธิพลทางฤดูกาล:** ค่าเฉลี่ยความเข้มข้นของฝุ่น PM2.5 ในแต่ละฤดูกาลมีความแตกต่างกันอย่างชัดเจน โดยฤดูหนาวมีค่าสูงสุด เนื่องจากสภาพอากาศและปัจจัยทางธรรมชาติ

* **ความสัมพันธ์ทางธรรมชาติ (สหสัมพันธ์ทางลบ):** ความชื้นสัมพัทธ์ ปริมาณน้ำฝน มีความสัมพันธ์ทางลบกับความเข้มข้นของ PM2.5 ปัจจัยเหล่านี้มีบทบาทสำคัญในการชะล้างฝุ่นออกจากอากาศ

* **ความสัมพันธ์เชิงความร้อน (สหสัมพันธ์ทางบวก):** อุณหภูมิมีความสัมพันธ์เชิงบวกกับความเข้มข้นของ PM2.5 โดยเฉพาะในช่วงฤดูหนาว

* **ขีดความสามารถในการคาดการณ์:** เมื่อนำปัจจัยด้านอุตุนิยมวิทยาและปัจจัยทางสังคมเศรษฐกิจมารวมกัน โมเดลการเรียนรู้ของเครื่องสามารถคาดการณ์ความเข้���ข้นของ PM2.5 ได้ด้วยความแม่นยำที่สูง

---

## How to Improve

1. เพิ่มมิติตัวแปรด้านทิศทางลม ความกดอากาศ และความหนาแน่นของจุดความร้อน เพื่อให้ครอบคลุมปัจจัยทางธรรมชาติและมนุษย์ได้ครบถ้วน

2. นำเทคนิคตัวแบบขั้นสูงกลุ่ม Deep Learning (เช่น LSTM สำหรับข้อมูลอนุกรมเวลา) มาทดสอบและเปรียบเทียบกับโมเดล Machine Learning ดั้งเดิม

3. พัฒนาเว็บแอปพลิเคชันหรือโปรแกรมประยุกต์สำหรับอุปกรณ์เคลื่อนที่เพื่อให้บุคคลทั่วไปสามารถเข้าถึงผลการพยากรณ์ PM2.5 ได้อย่างง่ายดาย

---

## Project Authors

### คณะผู้จัดทำ

(สาขาวิชาวิทยาการคอมพิวเตอร์และนวัตกรรมข้อมูล มหาวิทยาลัยเทคโนโลยีสุรนารี)

* นายนันทพงศ์ พันธ์เนียม | เลขประจำตัว 661222500453
* นายธนากร สินธุสอาด | เลขประจำตัว 661222500703

### อาจารย์ผู้ลงความเห็นและประเมินผลโครงการ

* ดร. กลยณฏฐ์ กหลาบเพชรทอง

Contact Email: tanakorn9687@gmail.com

Project GitHub: [Munumpa Profile](https://github.com/Munumpa)

---

## License

This project is open-source and registered under the MIT License.

Last Updated: Aug 17, 2026
