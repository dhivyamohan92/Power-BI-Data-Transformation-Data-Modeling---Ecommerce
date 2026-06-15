# 📊 Project Title: E-Commerce Sales Data Transformation & Data Modeling Using Power BI

A Power BI project that transforms raw E-Commerce sales data into a clean, structured, and analysis-ready data model through data preparation, transformation, aggregation, and relationship modeling.

---

# 📑 Table of Contents

* Project Overview
* Data Sources & Architecture
* Data Transformation (ETL)
* Data Model & DAX
* Dashboard Features
* Key Insights
* How To Use

---

# 🎯 Project Overview

## Business Problem

E-Commerce businesses generate large amounts of transactional data from customer orders, product sales, and sales targets. Raw datasets often contain inconsistencies and require transformation before meaningful business analysis can be performed.

## Objective

The objective of this project is to prepare, clean, transform, integrate, and model E-Commerce sales data using Power BI and Power Query Editor. The final data model enables accurate reporting, aggregation, and business analysis.

## Target Audience

* Business Analysts
* Sales Managers
* Data Analysts
* Students Learning Power BI
* Business Intelligence Professionals

---

# 🗃️ Data Sources & Architecture

## Source Systems

The project uses three CSV files:

### List of Orders

Contains customer and order information:

* Order ID
* Order Date
* Customer Name
* City
* State

### Order Details

Contains product-level transaction details:

* Order ID
* Category
* Sub-Category
* Quantity
* Amount
* Profit

### Sales Target

Contains category-wise monthly sales targets:

* Category
* Month of Order Date
* Target

---

## Data Volume

| Dataset        | Records                  |
| -------------- | ------------------------ |
| List of Orders | 500 (after row limiting) |
| Order Details  | 1500                     |
| Sales Target   | 36                       |

---

## Storage Mode

**Import Mode**

All datasets were imported into Power BI Desktop and transformed using Power Query Editor.

---

# ⚙️ Data Transformation (ETL)

## Tool Used

**Power Query Editor**

## Key Cleanups & Transformations

### Data Import

* Imported List of Orders.csv
* Imported Order Details.csv
* Imported Sales Target.csv

### Row Limiting

* Restricted List of Orders to the first 500 rows.

### Data Type Conversion

* Order Date → Date
* Amount → Fixed Decimal Number
* Target → Fixed Decimal Number

### Text Formatting

* Converted Customer Name to Proper Case for consistent capitalization.

### Custom Column Creation

#### Location

Merged City and State columns.

Formula:

```text
Location = [City] & ", " & [State]
```

Example:

```text
Chennai, Tamil Nadu
```

#### Profit Margin

Created using:

```text
Profit Margin = Profit / Amount
```

Formatted as Percentage.

### Conditional Column

Created Profit Status column:

```text
Profit < 0  → Loss
Profit = 0  → Break-Even
Profit > 0  → Profit
```

### Data Integration

Merged:

* List of Orders
* Order Details

Join Key:

```text
Order ID
```

Output Table:

```text
Orders Data
```

### Data Quality Validation

* Checked for missing values using Column Quality.
* Checked for duplicate records.
* No missing values or duplicate records were found in the final filtered dataset.

### Sorting & Filtering

* Sorted Orders Data by Order Date (Descending).
* Filtered records for Tamil Nadu analysis.

### Aggregation

Created summary tables for:

* Total Order Count
* Average Profit by Category
* Total Amount by Sub-Category
* Total Target by Month

---

# 🧠 Data Model & DAX

## Model Type

**Relational Data Model**

## Fact Table

### Order Details

Contains transactional sales information:

* Order ID
* Category
* Sub-Category
* Quantity
* Amount
* Profit

## Dimension Tables

### List of Orders

Contains:

* Order ID
* Customer Name
* City
* State
* Order Date

### Sales Target

Contains:

* Category
* Month of Order Date
* Target

---

## Relationships

### Relationship 1

```text
List of Orders[Order ID]
        ↓
Order Details[Order ID]
```

Cardinality:

```text
One-to-Many
```

### Relationship 2

```text
Order Details[Category]
        ↓
Sales Target[Category]
```

Cardinality:

```text
Many-to-One
```

All relationships were validated using **Manage Relationships** and set as Active.

---

## Calculated Columns

### Profit Margin

```text
Profit Margin = Profit / Amount
```

### Profit Status

```text
IF Profit < 0 → Loss
IF Profit = 0 → Break-Even
IF Profit > 0 → Profit
```

---

# 🖥️ Dashboard Features

## Page 1: Data Preparation Overview

Displays:

* Imported datasets
* Data transformation workflow
* Data quality validation summary

## Page 2: Aggregation Analysis

Displays:

* Total Orders
* Average Profit by Category
* Total Amount by Sub-Category
* Monthly Sales Targets

## Page 3: Data Model View

Displays:

* Table relationships
* Data model structure
* Active relationship connections

---

## Design Features

* Clean and structured layout
* Consistent formatting
* Interactive filtering capabilities
* Business-oriented data model

---

# 💡 Key Insights

## Trend A

The merged Orders Data table provides a complete view of customer orders and product transactions, enabling unified business analysis.

## Trend B

Category-level profit analysis helps identify product categories contributing the highest profitability.

## Trend C

Sub-category aggregation highlights the top revenue-generating product groups.

## Recommendation

Organizations should maintain structured relationships between sales, customer, and target datasets to improve reporting accuracy and support data-driven decision-making.

---

# 🚀 How To Use

## Prerequisites

Ensure the following are installed:

* Power BI Desktop
* Windows 10/11

---

## Open the Project

1. Download or clone the repository.
2. Open the `.pbix` file in Power BI Desktop.
3. Verify data source file paths.
4. Click **Refresh** to load data.

---

## Data Refresh

If dataset locations change:

```text
Home → Transform Data → Data Source Settings
```

Update the CSV file locations and refresh the report.

---

# 👩‍💻 Author

**Dhivya Mohan**

Aspiring Data Analyst | Power BI Developer

### Skills Demonstrated

* Power BI
* Power Query Editor
* Data Cleaning
* Data Transformation
* Data Modeling
* Data Aggregation
* Business Intelligence Reporting

---

# 📌 Version History

## Version 1.0

* Imported datasets
* Applied Power Query transformations
* Created custom and conditional columns
* Merged datasets using joins
* Performed aggregations
* Created data model relationships
* Completed project documentation

---

# 🙏 Acknowledgments

* Microsoft Power BI
* Power Query Editor
* E-Commerce Sales Dataset
* Data Analytics (DA) Module 2 Assignment
* Power BI Learning Community
* Open-source Data Analytics Resources
