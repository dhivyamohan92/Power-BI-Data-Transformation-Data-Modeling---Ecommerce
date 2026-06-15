# Power BI Assignment 1 – Data Transformation & Data Modeling

## Project Title

E-Commerce Sales Data Transformation and Data Modeling using Power BI

## Overview

This project demonstrates the process of importing, cleaning, transforming, integrating, aggregating, and modeling E-commerce sales data using Power BI and Power Query Editor. The objective is to prepare raw sales data for business analysis by applying data preparation techniques and establishing relationships between multiple datasets.

---

## Description

The project uses three datasets: List of Orders, Order Details, and Sales Target. Various data transformation techniques were performed including row limiting, data type conversion, text formatting, custom column creation, conditional column creation, table merging, sorting, filtering, and aggregation. Data modeling was implemented by creating relationships between tables using Order ID and Category fields.

The final output is a clean, structured, and analysis-ready Power BI data model that supports reporting and business decision-making.

---

# Getting Started

## Dependencies

Before running this project, ensure the following requirements are met:

* Windows 10 or later
* Power BI Desktop
* CSV Dataset Files

  * List of Orders.csv
  * Order Details.csv
  * Sales Target.csv

---

## Installing

### Step 1: Download the Project

Clone or download the repository:

```bash
git clone 
```https://github.com/dhivyamohan92/Power-BI-Data-Transformation-Data-Modeling---Ecommerce

### Step 2: Open Power BI File

Open the `.pbix` file using Power BI Desktop.

### Step 3: Verify Dataset Paths

If required:

* Update CSV file locations
* Refresh the data source connections

---

## Executing Program

### Open the Project

1. Launch Power BI Desktop.
2. Open the provided `.pbix` file.
3. Click **Refresh** to load data.

### Power Query Transformations Performed

* Imported datasets
* Restricted List of Orders to first 500 rows
* Converted data types
* Formatted Customer Name column
* Created Location column
* Created Profit Margin column
* Created Profit Status column
* Merged tables using Order ID
* Sorted and filtered records
* Performed grouping and aggregation
* Created relationships between tables

### Refresh Data

```text
Home → Refresh
```

---

# Help

## Common Issues

### Data Source Not Found

If Power BI cannot locate the CSV files:

1. Go to Transform Data.
2. Open Data Source Settings.
3. Update the file paths.
4. Refresh the dataset.

### Relationship Errors

If relationships become inactive:

1. Open Model View.
2. Select Manage Relationships.
3. Verify:

   * Matching columns
   * Correct cardinality
   * Active relationship status

### Data Type Errors

Ensure:

* Order Date = Date
* Amount = Fixed Decimal Number
* Target = Fixed Decimal Number

---

# Authors

### Contributor

Dhivya Mohan

GitHub Profile:
@Dhivya Mohan

---

# Version History

## Version 0.2

* Added data modeling relationships
* Implemented aggregations
* Added custom and conditional columns
* Improved data quality validation

## Version 0.1

* Initial project setup
* Imported datasets
* Performed basic transformations

---

# License

This project is created for educational and academic purposes.

---

# Acknowledgments

Special thanks to:

* Power BI Desktop
* Microsoft Power Query Editor
* E-Commerce Sales Dataset
* Course Instructors and Mentors

Resources referenced:

* Power BI Documentation
* Power Query Documentation
* GitHub README Best Practices


---

## Project Structure

```text
PowerBI-Assignment-1/
│
├── Dataset/
│   ├── List of Orders.csv
│   ├── Order Details.csv
│   └── Sales Target.csv
│
├── PowerBI/
│   └── PowerBI_Assignment_1.pbix
│
├── Documentation/
│   ├── Project_Report.pdf
│   ├── Data_Model_View.png
│   └── Screenshots/
│
└── README.md
```

---

## Key Skills Demonstrated

* Data Import and Preparation
* Data Cleaning and Validation
* Data Transformation
* Custom and Conditional Columns
* Data Integration using Joins
* Data Aggregation and Summarization
* Data Modeling and Relationship Management
* Business Data Interpretation

---

## Project Outcome

Successfully transformed raw E-commerce sales data into a structured Power BI data model by applying data preparation, cleaning, integration, aggregation, and relationship modeling techniques. The final model supports efficient reporting and business analysis.
