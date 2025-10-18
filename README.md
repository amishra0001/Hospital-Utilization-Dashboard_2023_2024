# 🏥 **Hospital Utilization Dashboard (Power BI)**

---

## 📘 **Overview**
This Power BI project analyzes **hospital utilization data (2023–2024)**, focusing on **patient activity, admissions, ER visits**, and **key operational metrics**.  
The dashboard provides an interactive view of healthcare performance, helping analysts and hospital leaders identify **trends, inefficiencies, and opportunities for improvement**.

---

## 📊 **What This Dashboard Shows**

- 🧍‍♂️ Patient load and admissions over time  
- 🏨 Hospitals with the highest **bed occupancy rates**  
- ⏱️ Trends in **average length of stay (LOS)**  
- 🔁 **Readmission rate** patterns by hospital and payer  
- 💰 Breakdown of **payer mix** (Medicare, Medicaid, Private, Self-Pay)

---

## 📈 **Key Metrics**

| **Metric** | **Description** |
|-------------|----------------|
| **Total Patients** | Monthly patient volume |
| **ER Visits** | Number of emergency room visits |
| **Admissions** | Inpatient admissions |
| **Discharges** | Patients discharged |
| **Average LOS** | Average days per patient stay |
| **Bed Occupancy Rate** | % of hospital beds occupied |
| **Readmission Rate** | % of patients readmitted |
| **Payer Type** | Type of insurance coverage |

---

## 🧾 **About the Data**

- **Filename:** `hospital_utilization_2023_2024.csv`  
- **Size:** ~50,000 records  
- **Period Covered:** Jan 2023 – Dec 2024  
- **Granularity:** Monthly per hospital  
- **Columns:**  
  `Hospital_ID`, `Hospital_Name`, `State`, `Month`, `Year`,  
  `Total_Patients`, `ER_Visits`, `Inpatient_Admissions`, `Discharges`,  
  `Average_Length_of_Stay`, `Bed_Occupancy_Rate`, `Readmission_Rate`, `Payer_Type`

---

## 📊 **Dashboard Highlights**

### 🧭 **Page 1 – Executive Summary**
- KPI Cards: Total Patients, ER Visits, Admissions, Avg LOS, Bed Occupancy, Readmission Rate  
- Monthly patient trends *(line chart)*  
- Top 10 hospitals by patient count *(bar chart)*  
- State-level overview *(map visualization)*  

### ⚙️ **Page 2 – Operational Insights**
- LOS vs Occupancy comparison  
- Readmission correlation *(scatter chart)*  
- Conditional formatting → 🔴 *Red for high LOS (>6)*  

### 💳 **Page 3 – Payer Mix**
- Donut chart showing payer breakdown  
- Admissions & readmissions by payer type  

### 🏥 **Page 4 – Hospital Comparison**
- Slicers: *Year, State, Hospital Name*  
- Monthly trend for selected hospital  
- LOS, Occupancy, and Readmission details  

---

## 💡 **Insights You Can Gain**

✅ Hospitals consistently operating at **high occupancy**  
✅ How **average LOS impacts readmissions**  
✅ **Seasonal patterns** in patient volume  
✅ Which **payer types drive the highest admissions**

---

## 🧰 **Tools & Technologies**

- 🟦 **Power BI Desktop** – Data modeling & visualization  
- 🟩 **Power Query** – ETL & transformation  
- 📊 **Microsoft Excel / CSV** – Data storage  
- ⚙️ **DAX** – KPI & calculated measures  
- 🧾 **GitHub** – Version control & documentation  

---

## 🧮 **Sample DAX Measures**

```DAX
-- Total Patients
Total Patients = SUM(Hospital_Utilization[Total_Patients])

-- Total ER Visits
Total ER Visits = SUM(Hospital_Utilization[ER_Visits])

-- Total Admissions
Total Admissions = SUM(Hospital_Utilization[Inpatient_Admissions])

-- Total Discharges
Total Discharges = SUM(Hospital_Utilization[Discharges])

-- Average Length of Stay
Avg LOS = AVERAGE(Hospital_Utilization[Average_Length_of_Stay])

-- Average Bed Occupancy Rate
Avg Bed Occupancy = AVERAGE(Hospital_Utilization[Bed_Occupancy_Rate])

-- Average Readmission Rate
Avg Readmission Rate = AVERAGE(Hospital_Utilization[Readmission_Rate])

-- Patients by Payer Type
Patients by Payer = SUM(Hospital_Utilization[Total_Patients])
🎨 Conditional Formatting Rules have been applied to visualize clearly. 

🧩 Dynamic Filters (Slicers)
Year

State

Hospital Name

Payer Type
