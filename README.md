# SSIS Contoso Sales ETL Analysis
This repository features a robust ETL (Extract, Transform, Load) solution developed using **SQL Server Integration Services (SSIS)**.
The project processes large-scale retail data from the **ContosoRetailDW** database to generate actionable insights into sales performance.

## Project Overview
The objective of this project is to automate the extraction and transformation of retail data across five critical dimensions. 
The workflow is designed to ensure data integrity while optimizing for performance through advanced SSIS transformations.

### Tech Stack
* **ETL Tool:** SQL Server Integration Services (SSIS)
* **Database:** SQL Server (ContosoRetailDW)
* **IDE:** Visual Studio / SQL Server Data Tools (SSDT)

---

##  Workflow Architecture

### 1. Control Flow
The package utilizes a sequential Control Flow to manage task dependencies, ensuring that data is processed in a logical order.
* **Tasks included:** Product Analysis, Brand Analysis, Channel Analysis, Category Analysis, and Sales Overtime.

### 2. Data Flow Highlights
Each Data Flow Task is optimized with specific transformations:

| Analysis Module | Key Transformations Used |
| :--- | :--- |
| **Product Analysis** | Lookup (DimProduct), Aggregate, Derived Column, Sort. |
| **Brand Analysis** | OLE DB Source, Lookup, Aggregate, Sort. |
| **Category Analysis** | Multicast, multiple Aggregates, Merge Join, Derived Column. |
| **Channel Analysis** | Multicast, Aggregate, Sort, Merge Join. |
| **Sales Overtime** | Source, Aggregate, Sort, Destination. |

---

## Visualizations

### Control Flow Execution
![Control Flow](./Images/Control%20Flow.png)

### Data Flow Logic (Examples)
| Category Analysis | Brand Analysis |
| :--- | :--- |
| ![Category](./Images/Category%20Analysis.png) | ![Brand](./Images/Brand%20Analysis.png) |

---
