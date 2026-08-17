# การวิเคราะห์ปัจจัยพหุที่มีอิทธิพลต่อมลพิษทางอากาศ (PM2.5) ในประเทศไทยด้วยเทคนิคการเรียนรู้ของ Machine Learning

**Multi-Factor Analysis of Air Pollution (PM2.5) Inflation in Thailand Using Machine Learning Techniques**  
โครงการวิจัยเชิงบูรณาการเพื่อวิเคราะห์และพยากรณ์ความสัมพันธ์เชิงลึกระหว่างดานประชากรศาสตร์ การคมนาคม อุตสาหกรรม และภูมิอากาศ ต่อการสะสมตัวของฝุ่นละอองขนาดเล็กไม่เกิน 2.5 ไมครอน (PM2.5) ในประเทศไทย

---

## 📌 At a Glance
* **รายวิชา:** CSD3201 การพัฒนาโปรแกรมประยุกต์สำหรับอุปกรณ์เคลื่อนที่
* **สถาบัน:** สาขาวิชาวิทยาการคอมพิวเตอร์และนวัตกรรมข้อมูล คณะวิทยาศาสตร์และเทคโนโลยี มหาวิทยาลัยราชภฏสวนสนนทา
* **ชุดข้อมูล:** ข้อมูลบูรณาการรายเดือนครอบคลุมระยะเวลา 5 ปี (พ.ศ. 2563-2567) จากเว็บไซต์หน่วยงานภาครัฐ 4 แหล่ง
* **ผลลัพธ์สำคัญ:** ปัจจัยทางอุตุนิยมวิทยา (ปริมาณน้ำฝน ความชื้นสัมพัทธ์ ความเร็วลม) มีความสัมพันธ์ทางลบอย่างมีนัยสำคัญกับการสะสมตัวของฝุ่น ในขณะที่อุณหภูมิและปัจจัยเมือง (ประชากร, รถยนต์, โรงงานใหม่) เป็นตัวแปรเร่งปฏิกิริยาหลักในชั้นบรรยากาศ

---

## 📑 Table of Contents
- [Project Overview](#-project-overview)
- [Objectives](#-objectives)
- [Dataset & Features](#-dataset--features)
- [Technologies & Libraries](#-technologies--libraries)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage Guide](#-usage-guide)
- [Key Research Findings](#-key-research-findings)
- [How to Improve](#-how-to-improve)
- [Project Authors](#-project-authors)

---

## 🔍 Project Overview
ในปัจจุบันประเทศไทยกำลังเผชิญกับวิกฤตการณ์ทางสิ่งแวดล้อมจากปัญหาฝุ่นละออง PM2.5 ซึ่งส่งผลกระทบอย่างรุนแรงต่อสุขภาวะของประชาชนในระยะยาว เพิ่มความเสี่ยงโรคระบบทางเดินหายใจและหลอดเลือดหัวใจ รวมถึงส่งผลกระทบเชิงลบต่อระบบเศรษฐกิจและการท่องเที่ยว 

เนื่องจากแหล่งกำเนิดมลพิษมีความซับซ้อนและกระจายตัวอยู่ทั่วประเทศ โครงการวิจัยนี้จึงมุ่งเน้นการใช้แนวทางวิทยาการข้อมูล (Data Science) และการเรียนรู้ของเครื่อง (Machine Learning) มาวิเคราะห์ความสัมพันธ์เชิงลึกโดยพิจารณาทั้งในมุมของ **"ตัวก่อ"** (กิจกรรมเมือง) และ **"ตัวช่วยชะล้าง"** (ปัจจัยทางธรรมชาติ) ไปพร้อมกันเพื่อความเข้าใจที่ครอบคลุมและแม่นยำ

---

## 🎯 Objectives
1. **Data Integration & Preprocessing:** รวบรวมและทำความสะอาดข้อมูลดิบ (Data Cleaning) จัดการค่าสูญหาย และลดความสับสนของข้อมูลอุตุนิยมวิทยาผ่านกระบวนการ Data Preprocessing อย่างเป็นระบบ
2. **Exploratory Data Analysis (EDA):** ศึกษารูปแบบการกระจายตัวของฝุ่น PM2.5 และวิเคราะห์สัมประสิทธิ์สหสัมพันธ์ (Correlation) ร่วมกับปัจจัยเมืองและภูมิอากาศ
3. **Model Development:** พัฒนาและเปรียบเทียบโมเดลการเรียนรู้ของเครื่องเพื่อคาดการณ์ความเข้มข้นของมลพิษทางอากาศ
4. **Policy Decision Support:** สร้างชุดข้อมูลเชิงประจักษ์เพื่อสนับสนุนการตัดสินใจและวางนโยบายการจัดการสิ่งแวดล้อมเชิงพื้นที่

---

## 📊 Dataset & Features
ชุดข้อมูลผ่านการบูรณาการข้อมูลดิบรายเดือนเชิงพื้นที่จากเว็บไซต์ภาครัฐอย่างน้อย 4 แหล่งข้อมูล ได้แก่ **กรมควบคุมมลพิษ, กรมอุตุนิยมวิทยา, กรมการขนส่งทางบก และกรมโรงงานอุตสาหกรรม**

### 1. ข้อมูลคุณลักษณะ (Features)
* `Year` / `Month` / `Province`: ข้อมูลระบุเวลาและเชิงพื้นที่
* `Total_Population`: จำนวนประชากรและความหนาแน่น ดัชนีชี้วัดกิจกรรมทางเศรษฐกิจและการขยายตัวของการก่อสร้าง
* `Total_Vehicles`: ปริมาณรถยนต์จดทะเบียนสะสม สะท้อนอัตราการใช้เชื้อเพลิงฟอสซิลที่ก่อให้เกิดไอเสีย
* `New_Factories`: จำนวนโรงงานอุตสาหกรรมที่ประกอบกิจการใหม่หรือขยายตัว ดัชนีการปลดปล่อยมลพิษจากปล่องควัน
* `Rainfall`: ปริมาณน้ำฝนสะสม ปัจจัยทางธรรมชาติในการชะล้างฝุ่นละอองในอากาศ

### 2. ตัวแปรเป้าหมาย (Target)
* `PM2.5`: ค่าเฉลี่ยความเข้มข้นของฝุ่นละอองขนาดเล็กไม่เกิน 2.5 ไมครอน

---

## 🛠 Technologies & Libraries
| หมวดหมู่ | เครื่องมือที่เลือกใช้ |
| :--- | :--- |
| **Language** | Python 3.8+ |
| **Environment** | Jupyter Notebook |
| **Data Processing** | Pandas, NumPy |
| **Data Visualization** | Matplotlib, Seaborn, Plotly |
| **Machine Learning** | Scikit-learn (Linear Regression, Random Forest, Gradient Boosting, SVM) |
| **Statistical Analysis** | SciPy, StatsModels |

---

## 📂 Project Structure
```text
TH-PM2.5-Machine-Learning-Analysis/
├── Data_Set/                           # ไดเรกทอรีเก็บข้อมูลโครงการ
│   ├── Final_AirQuality_Dataset.csv    # ข้อมูลดิบที่รวมรวมจากการ Preprocessing
│   ├── AirQuality_Final.csv            # ข้อมูลสมบูรณ์ที่พร้อมสำหรับการ Train โมเดล
│   ├── Cleaned_PM25_MonthlyV3.csv      # ข้อมูล PM2.5 จำแนกรายเดือนเชิงพื้นที่
│   └── Cleaned_Rainfall_Monthly.csv    # ข้อมูลปริมาณน้ำฝนเชิงสถิติรายเดือน
├── re prove/                           # โมเดลและผลลัพธ์การทดลอง
│   ├── model_results.pkl               # ตัวแบบที่ผ่านการ Tuning แล้ว
│   └── predictions.csv                 # ผลการทำ Prediction ของชุดข้อมูลทดสอบ
├── TH-PM2.5-ML-Analysis.ipynb          # Jupyter Notebook หลักในการวิเคราะห์และรันโมเดล
├── requirements.txt                    # รายการ Library และ Dependencies
├── .gitignore                          # ไฟล์ตั้งค่าการสัญจรของ Git
└── README.md                           # เอกสารอธิบายโครงการวิจัยฉบับนี้
💻 Installation
1. Prerequisites
Python 3.8 หรือสูงกว่า
pip หรือระบบจัดการแพ็กเกจ conda
2. Setup Step-by-Step
# 1. Clone Repository
git clone [https://github.com/Munumpa/TH-PM2.5-Machine-Learning-Analysis.git](https://github.com/Munumpa/TH-PM2.5-Machine-Learning-Analysis.git)
cd TH-PM2.5-Machine-Learning-Analysis

# 
```2. Create Virtual Environment
python -m venv venv
source venv/bin/activate  # สำหรับ Windows ใช้: venv\Scripts\activate

# 3. Install Dependencies
pip install -r requirements.txt

# 4. Open Environment
jupyter notebook
📖 Usage Guide
เปิดไฟล์ TH-PM2.5-ML-Analysis.ipynb ผ่านทางหน้าต่าง Jupyter Workspace
ดำเนินการรันคำสั่งตามลำดับโครงสร้างหลักของ Notebook ดังนี้:
Section 1: Data Loading & Exploration
Section 2: Data Preprocessing & Cleaning (การจัดการค่าว่างและการกรองข้อมูลตัวแปรต้น)
Section 3: Feature Engineering & Scaling
Section 4: Exploratory Data Analysis (EDA) เพื่อหากราฟสหสัมพันธ์
Section 5: Model Training & Hyperparameter Tuning
Section 6: Predictions & Evaluation Metrics
หากต้องการตรวจสอบผลการประเมินแบบ Cross-Validation ให้ตรวจสอบค่าพารามิเตอร์ใน Section 5
📈 Key Research Findings
> ### ⚠️ Critical Insights จากงานวิจัย
>
> * **อิทธิพลทางฤดูกาล:** ค่าเฉลี่ยความเข้มข้นของฝุ่น PM2.5 ในแต่ละฤดูกาลมีความแตกต่างกันอย่างมีนัยสำคัญทางสถิติกดระดับ 0.05 โดย **"ฤดูร้อน" มีค่าเฉลี่ยความเข้มข้นสูงที่สุดและเกินค่ามาตรฐาน**
> * **ความสัมพันธ์ทางธรรมชาติ (สหสัมพันธ์ทางลบ):** ความชื้นสัมพัทธ์ ปริมาณน้ำฝน และความเร็วลม มีความสัมพันธ์ทางลบกับฝุ่น PM2.5 เนื่องจากเป็นปัจจัยช่วยกระจายและชะล้างมลพิษ
> * **ความสัมพันธ์เชิงความร้อน (สหสัมพันธ์ทางบวก):** อุณหภูมิมีความสัมพันธ์ทางบวกกับระดับความเข้มข้นของ PM2.5 (ยกเว้นในช่วงฤดูหนาว)
> * **ขีดความสามารถในการคาดการณ์:** เมื่อนำปัจจัยด้านอุตุนิยมวิทยาและปัจจัยเมืองมาวิเคราะห์ร่วมกันผ่านตัวแบบสถิติและการเรียนรู้ของเครื่อง จะสามารถร่วมกันคาดการณ์และอธิบายความแปรผันของความเข้มข้น PM2.5 ได้ถึง **61.2%**
🔍 How to Improve
1

เพิ่มมิติตัวแปรด้านทิศทางลม ความกดอากาศ และความหนาแน่นของจุดความร้อน (Hotspots) จากภาคเกษตรกรรมและป่าไม้12

นำเทคนิคตัวแบบขั้นสูงกลุ่ม Deep Learning (เช่น LSTM สำหรับข้อมูลอนุกรมเวลา) มาทดสอบเพื่อเปรียบเทียบประสิทธิภาพ234

พัฒนาเว็บแอปพลิเคชันหรือโปรแกรมประยุกต์สำหรับอุปกรณ์เคลื่อนที่เพื่อพยากรณ์และเตือนภัยกลุ่มเสี่ยง (เช่น ผู้สูงอายุ) ในพื้นที่นิคมอุตสาหกรรมแบบ Real-time34
👥 Project Authors
คณะผู้จัดทำ (สาขาวิชาวิทยาการคอมพิวเตอร์และนวัตกรรมข้อมูล)3
นายนันทพงศ์ พันธ์เนียม | เลขประจำตัว 661222500453
นายธนากร สินธุสอาด | เลขประจำตัว 661222500703
อาจารย์ผู้ลงความเห็นและประเมินผลโครงการ5
กลยณฏฐ์ กหลาบเพชรทอง
📧 Contact Email: tanakorn9687@gmail.com

🔗 Project GitHub: Munumpa Profile
📄 License
This project is open-source and registered under the MIT License.
Last Updated: Aug 17, 2026
