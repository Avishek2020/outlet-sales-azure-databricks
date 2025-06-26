# 🛒 Azure SQL to ADLS Data Pipeline using Databricks

## 📌 Business Requirements

1. The **sales outlet data** is available in an **Azure SQL Database**. We need to:
   - Connect to this data using **Databricks**
   - **Transform** and **clean** the data
   - **Store the output in ADLS** (Azure Data Lake Storage) as **CSV files**

2. The output data will be consumed by **business users** and **data scientists**, who need the data in **CSV format** for further use.

---

## ⚙️ Databricks Pipeline Steps

1. 🔗 **Connect** to Azure SQL Database using JDBC in Databricks  
2. 🧹 **Perform cleaning operations** on the raw data  
3. 📊 (Optional) **Generate insights** from the cleaned data  
4. ☁️ **Mount ADLS/Blob Storage** to Databricks and **store the results as CSV**

---

## 📈 KPI Insights Required

| KPI # | Description                              |
|-------|------------------------------------------|
| 1     | Top outlet sales                         |
| 2     | Top outlet sales by location             |
| 3     | Top outlet sales by outlet type          |
| 4     | Top items by total sales                 |
| 5     | Top outlet sales by outlet size          |

---

## 🧩 Notes

- Make sure to whitelist the Databricks public IP (e.g., `3.253.190.226`) in the Azure SQL firewall.
- Use `.option("driver", "com.microsoft.sqlserver.jdbc.SQLServerDriver")` for JDBC.
- Store final CSVs in ADLS path: `
