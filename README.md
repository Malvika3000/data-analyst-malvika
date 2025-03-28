# 📘 Vancouver Water Quality Analytics – AWS Cloud Portfolio
The City of Vancouver's complete Data Analytics Platform (DAP) deployment on AWS is displayed in this portfolio.  Using different AWS services, it adheres to a consistent methodology that includes exploratory data analysis, descriptive analysis, data wrangling, and data quality control.

![image alt](https://github.com/user-attachments/assets/b5006368-aa91-4dcd-84b0-80bedce6577d)

## 🔍 Exploratory Data Analysis (EDA)
**Project Decription**: In order to investigate missing data, data structure, and correlation patterns, the cooling tower, decorative water feature, and building water treatment datasets underwent initial profiling.

**Objective**: to use AWS Glue DataBrew to identify trends and quality problems and comprehend the structure and quality of water data from several facilities.

**Dataset**:Three datasets of water quality CSV files from the Vancouver Open Data Portal

**Methodology**:  
- Uploaded datasets into S3 using PowerShell via EC2

- Visualized architecture using Draw.io

- Created profiling jobs using AWS Glue DataBrew

- Analyzed correlation, duplication, and missing values

**Tools and Technology:**
Glue Studio, Glue Crawlers, Glue Data Catalog, S3, Parquet

**Deliverables**
- Architecture Overview
  ![image alt](https://github.com/Malvika3000/data-analyst-malvika/blob/99de12d1b64683502c680db824d1490841b12047/11.%20draw.io.png)
- Crawler Output
  ![image alt](https://github.com/Malvika3000/data-analyst-malvika/blob/99de12d1b64683502c680db824d1490841b12047/12.%20crawler.png)
- Visual Pipeline
  ![image alt](https://github.com/Malvika3000/data-analyst-malvika/blob/99de12d1b64683502c680db824d1490841b12047/13.%20visual%20pipeline%20ss.png)



