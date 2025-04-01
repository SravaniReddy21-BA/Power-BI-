# 📊 **Healthcare KPIs Dashboard**

## 🚀 **Project Overview**
The **Healthcare KPIs Dashboard** is an interactive and insightful data visualization project built using **Power BI**. It provides a comprehensive view of key performance indicators (KPIs) in a healthcare environment, enabling hospital administrators, clinicians, and decision-makers to monitor and analyze critical metrics such as patient admissions, readmission rates, length of stay, and overall operational performance.

This dashboard supports data-driven decision-making by offering actionable insights to improve patient care, optimize hospital resources, and enhance operational efficiency.

---
![image](https://github.com/user-attachments/assets/41122303-fa68-41b6-bfee-c02e57d290aa)


## 🔎 **Key Features**
- **KPI Cards**: High-level view of essential metrics including:
  - Total Patients
  - Total Rooms
  - Readmission Rate
  - Average Length of Stay (ALOS)
- **Admission Type Analysis**: Visual breakdown of **Emergency**, **Elective**, and **Urgent** admissions.
- **Readmission Trends**: Line chart visualization tracking readmission rates over time.
- **Medical Condition Insights**: Analysis of patient distribution based on medical conditions.
- **Revenue Overview**: Analysis of total billing amounts by insurance providers.
- **Patient Demographics**: Gender-based distribution of patients.
- **Interactive Filters and Slicers**: 
  - Filter data by **Date of Admission**
  - Analyze by **Hospital**
  - Drill down by **Doctor**
  - View specific data using **Medical Condition** or **Admission Type**

---

## 🛠️ **Tools and Technologies Used**
- **Power BI**: For data visualization and interactive dashboards.
- **DAX (Data Analysis Expressions)**: For creating measures and calculated columns.
- **Excel**: Data source for cleaning and structuring healthcare data.
- **SQL (Optional)**: For advanced data processing (if used during data preparation).
- **GitHub**: For version control and project sharing.

---

## 📥 **Data Overview**
The dataset consists of healthcare records with fields including:
- **Patient Name**
- **Age**
- **Gender**
- **Blood Type**
- **Medical Condition**
- **Admission Type** (Emergency/Elective/Urgent)
- **Date of Admission**
- **Discharge Date**
- **Doctor**
- **Hospital**
- **Billing Amount**
- **Insurance Provider**
- **Readmitted Status**
- **Length of Stay**

---

## 📈 **KPIs and Measures**
Here are the key measures created using DAX:

1. **Total Patients**:  
```dax
Total Patients = COUNTROWS('healthcare_dataset')
```

2. **Readmission Rate**:  
```dax
Readmission Rate = DIVIDE(
    COUNTROWS(FILTER('healthcare_dataset', 'healthcare_dataset'[Readmitted] = "Yes")),
    COUNTROWS('healthcare_dataset'),
    0
)
```

3. **Average Length of Stay (ALOS)**:  
```dax
ALOS = AVERAGE('healthcare_dataset'[Length of Stay])
```

4. **Total Billing Amount**:  
```dax
Total Billing Amount = SUM('healthcare_dataset'[Billing Amount])
```

---

## 💡 **How to Use the Dashboard**
1. **Filter by Date Range**: Use the **Date of Admission** slicer to view trends over a specific time frame.
2. **Analyze by Hospital or Doctor**: Select a particular hospital or doctor to compare performance.
3. **Explore Admission Types**: See how many patients were admitted as **Emergency**, **Elective**, or **Urgent** cases.
4. **Drill-Through Functionality**: Right-click on visual elements to view detailed patient-level data.
5. **Identify Trends**: Analyze readmission rates over time using the **Readmission Trends** chart.

---

## 📦 **Installation and Usage**
1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/Healthcare-KPIs-Dashboard.git
    ```
2. **Open in Power BI**:
    - Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
    - Open the `.pbix` file using Power BI Desktop.
3. **Explore the Dashboard**:
    - Interact with slicers, charts, and filters.
    - Analyze insights and export reports if needed.

---

## 📜 **Future Enhancements**
- Integrate real-time data using APIs.
- Add predictive analytics using machine learning.
- Develop role-based access for different stakeholders (e.g., Admins, Doctors, Executives).
- Implement mobile-friendly visualizations for better accessibility.

---

## 🤝 **Contributing**
Contributions are welcome! If you'd like to improve the dashboard, follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m "Added new feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

---

## 📧 **Contact**
If you have any questions or feedback, feel free to contact me via GitHub(github.com/SravaniReddy21-BA) or LinkedIn(https://www.linkedin.com/in/sravss/).
