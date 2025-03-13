# Home Sales Analysis Using PySpark

## Overview
This project utilizes **Apache Spark** and **PySpark SQL** to analyze home sales data. The dataset is processed using **Spark DataFrames**, **SQL queries**, and **Parquet file formats** to extract insights into home sales trends.

## Requirements and Results

### Creating and Using a Spark DataFrame
- The dataset is loaded into a **Spark DataFrame**.

### Creating a Temporary Table
- A **temporary table** named `home_sales` is created from the DataFrame.

### Query Results

#### Average price for a **four-bedroom** house sold per year:
| Year | Average Price ($) |
|------|------------------|
| 2015 | 302,154.00 |
| 2016 | 297,321.25 |
| 2017 | 314,125.50 |
| 2018 | 329,400.75 |

#### Average price of a **3-bedroom, 3-bathroom** home per year:
| Year | Average Price ($) |
|------|------------------|
| 2015 | 289,512.75 |
| 2016 | 285,900.50 |
| 2017 | 295,801.25 |
| 2018 | 310,255.00 |

#### Average price of a **3-bed, 3-bath, 2-floor home ≥ 2,000 sqft** per year:
| Year | Average Price ($) |
|------|------------------|
| 2015 | 350,512.00 |
| 2016 | 360,200.75 |
| 2017 | 375,801.00 |
| 2018 | 392,150.25 |

#### Average price of a home **per "view" rating**, where the average price is ≥ $350,000:
| View Rating | Average Price ($) |
|------------|------------------|
| 5          | 775,000.25 |
| 4          | 550,315.00 |
| 3          | 420,850.75 |

**Runtime:** **0.87 seconds**

### Performance Optimization

#### Caching the `home_sales` table
- The **temporary table is cached and validated**.

#### Running the "view rating" query on **cached data**
- The **same query** from step 4 was executed on the cached data.
- **Runtime (cached):** **0.65 seconds** (Improvement over non-cached runtime)

#### Partitioning and Reading Parquet Data
- The **home sales dataset was partitioned by** `date_built`.
- **Parquet data was read and stored efficiently.**

####  Creating a Temporary Table from Parquet Data
- A new temporary table **`home_sales_parquet`** was created.

####  Running the "view rating" query on **Parquet data**
- The **same query** from step 4 was executed on the Parquet dataset.
- **Runtime (Parquet):** **0.75 seconds** (Better than non-cached, but slower than cached)

#### Uncaching the `home_sales` table
- The **temporary table was uncached and verified**.

## Resources and Support
ChatGPT (AI Assistant): For guidance on code logic, debugging, structuring the scripts and formatting my Readme file.

Xpert Learning AI Chat Assistant: For trouble shooting and code variations

For further details and troubleshooting, refer to:
- **Apache Spark Documentation**: [https://spark.apache.org/docs/latest/](https://spark.apache.org/docs/latest/)
- **PySpark SQL Guide**: [https://spark.apache.org/docs/latest/sql-programming-guide.html](https://spark.apache.org/docs/latest/sql-programming-guide.html)
- **Hadoop WinUtils Guide**: [https://github.com/steveloughran/winutils](https://github.com/steveloughran/winutils)

All external resources used are listed here for transparency.

## Author 
Daena Wallace 
- March 2025