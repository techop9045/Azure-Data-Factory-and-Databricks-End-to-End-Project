# Azure Data Factory and Databricks End-to-End Project

[![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com/)
[![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)](https://databricks.com/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Apache Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=for-the-badge&logo=apache-spark&logoColor=white)](https://spark.apache.org/)

## 📋 Overview

An end-to-end data engineering solution implementing the **Medallion Architecture** (Bronze-Silver-Gold) for processing and analyzing trip transaction data using Azure cloud services. This project automates data ingestion, transformation, and analytics workflows with built-in monitoring and email notifications.

## 🎯 Project Impact

- **Automated Data Pipeline**: Seamless data flow from Azure SQL Database to structured storage layers
- **Real-Time Processing**: Continuous data ingestion and transformation for up-to-date insights
- **Business Intelligence**: Advanced analytics on customer behavior, driver performance, and operational metrics
- **Scalability**: Cloud-native architecture handles growing data volumes efficiently
- **Data Quality**: Medallion Architecture ensures progressive data refinement and validation

## 🏗️ Architecture

<img width="667" height="333" alt="image" src="https://github.com/user-attachments/assets/0c76e063-6fc7-4441-9b38-74d4161e497b" />

```
Azure SQL Database → ADF → Bronze Layer (Raw Data) 
                             ↓
                    Silver Layer (Cleaned & Transformed)
                             ↓
                    Gold Layer (Business Insights)
                             ↓
                    Hive Metastore + Email Notifications
```

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| **Languages** | Python, SQL, PySpark |
| **Data Integration** | Azure Data Factory (ADF) |
| **Data Storage** | Azure Data Lake Storage Gen2 (ADLS) |
| **Data Processing** | Azure Databricks (Apache Spark) |
| **Database** | Azure SQL Database |
| **Orchestration** | ADF Pipelines, Logic Apps |
| **Storage Format** | Delta Lake |

## ✨ Key Features

### Delta Lake Benefits
- ✅ **ACID Transactions** - Reliable data operations with atomicity and consistency
- 📚 **Data Versioning** - Track changes and enable time travel queries
- 🔒 **Schema Enforcement** - Ensure data quality and consistency
- ⚡ **Optimized Performance** - Advanced indexing for faster queries

### Pipeline Capabilities
- 📥 **Full & Incremental Loads** - Efficient data synchronization
- 🔄 **Automated Scheduling** - Hands-free pipeline execution
- 📧 **Email Notifications** - Real-time alerts via Logic Apps
- 📊 **Monitoring Dashboard** - Track pipeline health and performance

## 📊 Use Cases

1. **Ride Analytics**
   - Identify top-rated drivers and peak demand periods
   - Track trip delays and payment statuses
   - Analyze customer travel patterns

2. **Driver Performance**
   - Highest number of trips per driver
   - Driver ratings and customer satisfaction metrics

3. **Financial Insights**
   - Highest-spending customers
   - Fare trends and revenue analysis
   - Distance-based pricing optimization

## 🚀 Quick Start

### Prerequisites
- Azure Subscription ([Free Account](https://azure.microsoft.com/free/))
- Azure CLI (optional)
- Basic knowledge of SQL and Python

### Setup Steps

1. **Create Azure Resources**
   ```bash
   - Resource Group
   - Azure SQL Database
   - Azure Data Lake Storage Gen2
   - Azure Databricks Workspace
   - Azure Data Factory
   ```

2. **Configure Data Source**
   - Upload sample CSV files to Bronze folder
   - Execute PySpark script to populate Azure SQL Database
   - Configure firewall rules for Databricks access

3. **Set Up Databricks**
   - Create compute cluster
   - Import notebooks (Bronze/Silver/Gold zones)
   - Configure ADLS access credentials

4. **Build ADF Pipeline**
   - Create dataflows for data extraction
   - Configure incremental load filters
   - Set up Logic Apps for email notifications

5. **Execute & Monitor**
   - Run the pipeline manually or schedule
   - Monitor execution in ADF dashboard
   - Verify data in each layer (Bronze → Silver → Gold)

## 📁 Project Structure

```
├── Bronze_Zone/
│   └── Delta_Lake_Validation.py      # Raw data validation
├── Silver_Zone/
│   ├── Customer_Dimension.py         # Customer dimension table
│   ├── Driver_Dimension.py           # Driver dimension table
│   ├── Date_Dimension.py             # Date dimension table
│   ├── Trip_Transaction_Fact.py      # Trip fact table
│   └── Rewards_Points_Fact.py        # Rewards fact table
├── Gold_Zone/
│   └── Final_Reports.py              # Business insights & analytics
└── PySpark_upload_data_to_DB_Script.py
```

## 📚 Data Flow

1. **Bronze Layer** - Raw data ingestion from Azure SQL Database in Delta format
2. **Silver Layer** - Data cleansing, transformation, and creation of fact/dimension tables
3. **Gold Layer** - Aggregated analytics and business insights stored in Hive Metastore

## 🔐 Best Practices Implemented

- Multi-Factor Authentication (MFA) enabled
- Least privilege access control
- Budget alerts and cost monitoring
- Soft delete disabled for real-time access
- Secrets management for credentials
- Resource naming conventions

## 📖 Learn More

### Official Documentation
- [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/)
- [Azure Databricks](https://docs.microsoft.com/azure/databricks/)
- [Delta Lake](https://docs.delta.io/)
- [PySpark](https://spark.apache.org/docs/latest/api/python/)

### Tutorials & Guides
- [Medallion Architecture](https://www.databricks.com/glossary/medallion-architecture)
- [Azure Logic Apps](https://docs.microsoft.com/azure/logic-apps/)
- [ADLS Gen2 Best Practices](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-best-practices)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## 📝 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- Built with Azure cloud services
- Powered by Apache Spark and Delta Lake
- Inspired by modern data engineering practices

---

**Note**: Remember to delete Azure resources after use to avoid unnecessary charges. Always monitor your Azure cost analysis dashboard.
