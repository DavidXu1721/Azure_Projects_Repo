# Azure Data Fundamentals (DP-900) | Cloud Data Project

## Project Overview

This project was completed as part of the **Azure Data Fundamentals (DP-900)** training course, providing practical experience with cloud computing, data storage, data ingestion, and analytics using Microsoft Azure services.

The project explored how different Azure technologies can be used to manage **relational, non-relational, and analytical data workloads**, with a focus on processing and analysing datasets such as retail transactions, sales records, customer information, and inventory data.

## Technologies & Tools

- **Microsoft Azure** - Cloud computing infrastructure and services
- **Azure SQL Database** - Relational database management and SQL querying
- **Azure Storage Account** - Non-relational storage, including Blob Storage
- **Azure Cosmos DB** - NoSQL database for flexible, semi-structured data
- **Microsoft Fabric Lakehouse** - Data storage, processing, and analytics
- **Microsoft Fabric Eventstreams** - Real-time data ingestion and event processing
- **SQL** - Data querying, filtering, aggregation, and joining

## Key Learning Areas

### 1. Cloud Computing Fundamentals

- Explored cloud service models: **IaaS, PaaS, and SaaS**.
- Understood public, private, and hybrid cloud environments.
- Examined cloud scalability, availability, cost efficiency, and pay-as-you-go pricing.
- Developed familiarity with Azure resources, storage services, and cloud infrastructure.

### 2. Relational Data - Azure SQL Database

- Explored how structured data is organised into relational tables.
- Understood primary keys, foreign keys, and relationships between datasets.
- Practised SQL techniques to retrieve, filter, sort, and aggregate data.
- Used relational data concepts to explore business questions involving sales, customers, and products.

### 3. Non-Relational Data - Azure Storage & Cosmos DB

- Explored Azure Storage Accounts for storing unstructured and semi-structured data.
- Learned how Azure Blob Storage supports scalable file and object storage.
- Investigated Azure Cosmos DB for managing flexible NoSQL data, including JSON documents.
- Compared relational and non-relational storage models and their appropriate use cases.

### 4. Analytical Workloads - Microsoft Fabric Lakehouse

- Explored Microsoft Fabric as a unified platform for data engineering and analytics.
- Learned how a Lakehouse combines flexible data lake storage with structured analytical capabilities.
- Investigated data ingestion through **Eventstreams** for real-time event data.
- Explored alternative ingestion approaches, including file uploads, batch ingestion, and data pipelines.
- Used analytical concepts to understand how large datasets can support reporting and business decision-making.

## Practical SQL Skills

The following examples demonstrate SQL techniques applicable to retail and sales datasets.

**SELECT and WHERE - Retrieve and filter sales records**

```sql
SELECT ProductID, Quantity, TotalAmount
FROM Sales
WHERE TotalAmount > 100;
```

**ORDER BY - Identify high-value transactions**

```sql
SELECT ProductID, TotalAmount
FROM Sales
ORDER BY TotalAmount DESC;
```

**GROUP BY - Calculate total sales by product**

```sql
SELECT ProductID, SUM(TotalAmount) AS TotalSales
FROM Sales
GROUP BY ProductID
ORDER BY TotalSales DESC;
```

**JOIN - Combine customer and sales information**

```sql
SELECT
    c.CustomerName,
    SUM(s.TotalAmount) AS TotalSpent
FROM Customers AS c
INNER JOIN Sales AS s
    ON c.CustomerID = s.CustomerID
GROUP BY c.CustomerID, c.CustomerName
ORDER BY TotalSpent DESC;
```

*Note: These are illustrative queries using example table and column names.*

## Data Ingestion & Analytics Workflow

1. **Data Sources:** Retail sales, customer records, inventory datasets, and event data.
2. **Data Ingestion:** Import data through file uploads, pipelines, or Microsoft Fabric Eventstreams.
3. **Data Storage:** Use Azure SQL Database, Azure Storage, Cosmos DB, or Fabric Lakehouse depending on data structure and requirements.
4. **Data Processing:** Organise, query, and transform datasets using SQL and analytical tools.
5. **Data Analysis:** Explore sales performance, customer spending, product trends, and business metrics.

## Skills Demonstrated

- Understanding of Azure cloud computing and data service models.
- Knowledge of relational, non-relational, and analytical workloads.
- Familiarity with multiple Azure database and storage technologies.
- Understanding of batch and real-time data ingestion methods.
- Practical SQL querying using `SELECT`, `WHERE`, `ORDER BY`, `GROUP BY`, and `JOIN`.
- Ability to apply cloud data concepts to business analytics scenarios.

## Project Outcome

This training project strengthened my foundational understanding of the Azure data ecosystem and how different cloud services support data storage, ingestion, processing, and analysis.

It also developed my SQL skills and introduced practical approaches to extracting meaningful insights from business datasets, providing a foundation for further learning in **data analytics, data engineering, and cloud-based data solutions**.

---

**Course:** Azure Data Fundamentals (DP-900)  
**Project Type:** Hands-on Training / Cloud Data Fundamentals  
**Platform:** Microsoft Azure & Microsoft Fabric
