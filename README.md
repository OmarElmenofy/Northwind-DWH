# Northwind-DWH
This repository provides a comprehensive guide to designing a dimensional data warehouse model using the Northwind dataset. It includes key interpretations and aligns with specific business requirements defined by stakeholders, aiming to deliver meaningful insights into different areas of the business.

# Northwind Data Warehouse with SSIS ETL
This repository contains a complete data warehousing solution based on the Northwind transactional database. The project includes dimensional modeling, ETL processes implemented in SQL Server Integration Services (SSIS), and SQL scripts for creating and populating both the OLTP and Data Warehouse schemas.

# Objective
To demonstrate the process of designing and building a data warehouse using best practices in dimensional modeling and ETL development. The project supports analytical reporting on orders, customers, products, suppliers, and employees.

**Note:** All data in the OLTP system was generated using AI tools for training and demonstration purposes. It is entirely fictional and localized to reflect entities in Egypt. It does not represent any real individuals, businesses, or transactions.

# Technologies Used
- SQL Server 2019
- SQL Server Integration Services (SSIS)
- SQL Server Management Studio (SSMS)
- Visual Studio with SSIS Projects extension
# Schema Overview
## OLTP Source (Normalized)
The OLTP system is modeled after the original Northwind database and adapted to simulate localized business operations in Egypt. It includes:
- Customers
- Employees
- Orders and Order Details
- Products, Categories, Suppliers
- Shippers, Regions, Territories
**Disclaimer:** The data is artificially generated for the purpose of this educational project. It does not reflect real entities or transactions.

# Data Warehouse (Star Schema)
##Fact Table
**FactOrders:** Measures related to sales performance, delivery, freight, and returns
##Dimension Tables
- DimCustomer
- DimProduct
- DimEmployee
- DimSupplier
- DimShippers
- DimAddress
- DimDate
The model uses surrogate keys, handles slowly changing dimensions (Type 2), and integrates date intelligence features.

# ETL Architecture
## The ETL process is implemented in SSIS and includes:
- Data extraction from the OLTP schema
- Lookup operations for surrogate key assignment
- Type 2 SCD implementation for dimension history
- Data transformation and cleansing
- Loading into staging, dimension, and fact tables
Each SSIS package is designed to load a specific target (e.g., DimCustomer, FactOrders) and can be executed independently or as part of a scheduled pipeline.

# Requirements
- Microsoft SQL Server 2019 or later
- Visual Studio with the SSIS Projects extension installed
- SQL Server Management Studio (SSMS)
