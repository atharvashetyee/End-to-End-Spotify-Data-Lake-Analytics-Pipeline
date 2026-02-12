🎧 Spotify Data Lake & Analytics Pipeline
Project Overview
This project demonstrates a Serverless Data Lakehouse architecture built on AWS to analyze global Spotify track data. Instead of traditional static reporting, this pipeline leverages cloud-native services to ingest raw data, automate metadata discovery, and provide high-performance SQL analytics.

🏗️ Architecture
The project follows a modern Decoupled Storage & Compute model:

Storage: Raw Spotify dataset stored in Amazon S3 (CSV/Parquet).

Cataloging: AWS Glue Crawlers automatically infer the schema and manage the Data Catalog.

Analytics Layer: Amazon Athena serves as the serverless query engine, processing SQL queries directly against S3.

Visualization: Power BI connects via ODBC/JDBC to provide interactive business intelligence and trend analysis.

🛠️ Tech Stack
Cloud Infrastructure: AWS (S3, Glue, IAM, CloudWatch)

Query Engine: Amazon Athena (SQL-on-S3)

Metadata Management: AWS Glue Data Catalog

Business Intelligence: Microsoft Power BI

Data Formats: CSV, optimized for Parquet

📊 Key Insights from Dashboard
Popularity Trends: Tracking how song popularity shifts across decades (Release Year vs. Popularity).

Artist Dominance: Visualizing top artists by follower count and genre distribution using Treemaps.

Audio Intelligence: Analyzing the relationship between track duration and user engagement.

🚀 Challenges Overcome
IAM Governance: Successfully resolved iam:PassRole and AccessDeniedException by implementing fine-grained Identity-Based policies.

Cloud Logging: Configured CloudWatch logging for Glue Crawlers to debug execution failures in real-time.

Cross-Platform Connectivity: Configured the Simba Athena ODBC Driver to bridge the gap between AWS and Power BI Desktop.

📈 Potential Impact
This architecture is highly scalable. By converting files to Parquet and implementing S3 Partitioning, query costs can be reduced by up to 90%, making it a production-ready solution for large-scale streaming data analysis.
