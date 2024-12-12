![License](https://img.shields.io/badge/license-MIT-blue.svg)

# 🌌 Data Management and Warehousing Project

## 📄 Overview

This project focuses on designing and implementing efficient data warehousing solutions for healthcare data. Three different warehouse schemas are explored: **Snowflake Schema**, **Galaxy Schema**, and **Star Schema**. The goal is to manage patient records, diagnoses, treatments, prescriptions, and billing information effectively. Each schema offers unique benefits for different analytical and performance needs.

## 🚀 Project Objectives

- Design and implement Snowflake, Galaxy, and Star schemas.
- Ensure efficient storage and retrieval of healthcare data.
- Compare the performance and efficiency of different schema designs.
- Provide reusable scripts and schema diagrams for future projects.
- Facilitate healthcare data analysis for decision-making and reporting.

## 📂 Repository Structure

```bash
├── Snowflake_Schema.pdf
│   └── Diagram and details of the Snowflake schema design.
│
├── Galaxy_Schema.pdf
│   └── Diagram and details of the Galaxy schema design.
│
├── Star_Schema.pdf
│   └── Diagram and details of the Star schema design.
│
├── DataWarehouseReport.pdf
│   └── Comprehensive report outlining methodologies and findings.
│
└── README.md
    └── Project documentation.
```

## 🌐 Data Source

**Dataset:** Healthcare Transactional Data  
The dataset includes patient information, medical staff details, appointments, diagnoses, treatments, prescriptions, and billing records.

## 📊 Schema Designs

### 1. 📚 Snowflake Schema

**Description:**  
A normalized schema that reduces redundancy by splitting tables into multiple dimensions.

- **Tables:**
  - `Patients` and `Patient_Contact`
  - `Medical_Staff` and `Staff_Contact`
  - `Appointments`, `Diagnoses`, `Treatments`, `Prescriptions`, `Billing`

**Pros:**
- Reduces data redundancy.
- Easier updates with normalized structure.

**Cons:**
- Complex queries due to multiple joins.
- Slower performance for large-scale analysis.

### 2. 📚 Galaxy Schema

**Description:**  
A hybrid schema combining features of star and snowflake schemas.

- **Tables:**
  - `Patients` (includes contact info)
  - `PatientVisits` (consolidates appointments, diagnoses, treatments, prescriptions)
  - `Billing`

**Pros:**
- Balanced approach to redundancy and storage efficiency.
- Flexible for analyzing multiple processes.

**Cons:**
- Some redundancy in `PatientVisits`.
- Limited flexibility for future breakdowns.

### 3. 📚 Star Schema

**Description:**  
A denormalized schema with a central fact table linked to dimension tables.

- **Tables:**
  - `FactTable`
  - `PATIENTS`, `MEDICALSTAFF`, `APPOINTMENTS`, `DIAGNOSES`, `TREATMENTS`, `PRESCRIPTIONS`, `BILLING`

**Pros:**
- Fast query performance with minimal joins.
- Ideal for large-scale analytical queries.

**Cons:**
- Increased data redundancy.
- Complex updates due to denormalization.

## 📊 Implemented Schema

**Chosen Schema:** Star Schema  
The Star Schema was selected for its fast query performance, making it suitable for large-scale healthcare data analysis. The central `FactTable` links all patient interactions, simplifying analysis across multiple dimensions.

## 💻 How to Run the Project

### Clone the Repository:

```bash
git clone https://github.com/nawaf-alageel/Data-Warehouse-Project.git
```

### Navigate to the Project Directory:

```bash
cd Data-Warehouse-Project
```

### Install Dependencies:

```bash
pip install pandas numpy sqlalchemy matplotlib
```

## 📝 Contributors

- **Mohammed Khalid Altufayhi**  
- **Anas Mohammed Alsubhi**  
- **Faisal Hammad Alomari**  
- **Nawaf Abdulrahman Alageel**  
- **Albadar Ibrahim Almaymani**  

## 📜 License

This project is licensed under the MIT License.

### MIT License

```
Copyright (c) 2024 Data Warehouse Project Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 💬 Feedback and Contributions

- **Contributions:** Feel free to fork the repository and submit pull requests.  
- **Issues:** If you encounter any problems or have feature requests, please open an issue.
