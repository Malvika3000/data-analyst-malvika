# data-analyst-malvika
Vancouver Water Quality Analytics – AWS Cloud Portfolio

The project I have created for the City of Vancouver is my Data Analytics Platform (DAP) on the cloud. In this project, I use several AWS services in order to build a scaled, secure, and efficient environment to manage and analyze water quality data.

Project 1: Data Ingestion & Profiling with AWS
Project Title: Vancouver Water Quality -Data Ingestion & Profiling
Objective: To support better decision making choose better water quality datasets and to profile them.
Dataset: Vancouver Open Data Portal
Tools & Services: Amazon S3, EC2, AWS Glue DataBrew, PowerShell

Key Steps:

Created PowerShell automation to upload raw datasets to S3.

In order to visualize the high level architecture, I used Draw.io

Created separate S3 buckets for cooling towers, decorative features and treatment systems respectively and I ran a number of profiling jobs in AWS Glue DataBrew.

Figure 1
AWS Glue DataBrew Recipe Jobs OverView

![image alt](https://github.com/Malvika3000/data-analyst-malvika/blob/1d39672164978946a06dd97a749c93d6c3f741f0/1.%20data%20analysis.png)

Profiling Results:

Missing values identified in Legionella, pH, and Chlorine Levels
Incorrect formats and duplicate records were detected
To get around this issue I used DataBrew transformations.


Project 2: Data Cleaning & Transformation
The Project Title: Water Quality Dataset – Cleaning and Storage Optimization.
The aim is to format and clean datasets and to unify storage for analysis.
Tools & Services: AWS Glue DataBrew, S3, Parquet & Snappy compression, Lifecycle Rules

Key Steps:

Renamed columns by removing spaces and camel cased them (to "Cooling Tower ID" → "CoolingTowerID")
Removed delimiter and corrected it from , to ;
Replaced missing values with defaults or imputed averages
CSV (User folder) and Parquet (System folder) stored datasets.
Applied S3 Lifecycle Rules for Glacier Instant Retrieval

Figure 2
S3 Buckets User Folder and System folder


Figure 3
Inside the system folder

Figure 4
Inside the User folder


Project 3: Data Analysis Using Amazon Athena

Project Title: Athena SQL Analytics – Water Temperature Trends
Objective: Using SQL queries analyze temperature trends.
Tools & Services: Amazon Athena, AWS Glue Catalog, S3

Key Queries
Basic Query – Average Temperature
Figure 5

Advanced Query – Min + Avg Temperature
Figure 6
Min & Avg Temperature Query 


Grouped Query – Average Temperature by Location
Figure 7 
Grouped Avg Temp by Location





Project 4: Data Security & Compliance
Securing City of Vancouver Water Data is the project title.
Goal: To encrypt data with AWS in-built tools like Encryption and Redundancy
Tools & Services: AWS KMS, S3 Encryption, Versioning, Cross-Bucket Replication

Security Measures:

Created Customer Managed Key (CMK) in KMS
Figure 8
KMS Console Showing the symmetric key created for encryption


Enabled SSE with KMS on S3

Figure 9
S3 Properties showing KMS-based server-side encryption enabled for bucket

Activated Versioning

Figure 10
S3 Bucket Properties versioning enabled for change tracking and object recovery


Set up Replication Rule

Figure 11
Replication rule configuration for automated cross-bucket backup



Project 5: Data Governance and Quality Check
Project Title: Data Quality Evaluation via AWS Glue
Objective: Validate data using rule-based governance setup
Tools & Services: AWS Glue Studio (Visual ETL), S3, Conditional Routing

Steps:

Defined rules for completeness, uniqueness, and freshness

Figure 12
Ruleset editor view with schema and rules

Used ETL flow to route passed vs failed records

Figure 13
ETL flow showing both routing paths


Figure 14
S3: Passed Folder content


Figure 15
S3: Failed Folder content


Project 6: Monitoring and Logging
Project Title: Monitoring Water Data Platform
Objective: Track system health and usage, trigger alerts for anomalies
Tools & Services: Amazon CloudWatch, CloudTrail, SNS

Steps:

Built a CloudWatch dashboard

Figure 16
CloudWatch metric widget setup showing bucket size growth over time

Created alarm + SNS topic
Figure 17
Alarm setup displaying limit configurations and SNS topic for alerts.

Final CloudWatch dashboard view
Figure 18
CloudWatch Dashboard displaying metric and alarm

Enabled CloudTrail for auditing

Figure 19
CloudTrail showing the active trail (vwqs-tra-malvi) and logging status.

