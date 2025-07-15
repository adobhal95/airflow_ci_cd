# airflow_ci_cd
## GCP Stock Market Data Pipeline
This project implements an end-to-end data pipeline on Google Cloud Platform (GCP) to fetch daily stock market data for Apple (AAPL) using the Yahoo Finance API, process it with Apache Spark on Dataproc Serverless, store it in Google Cloud Storage and BigQuery, and orchestrate the entire workflow using Cloud Composer (Managed Airflow). Finally, it includes email notification for pipeline success.

### 🚀 Architecture Overview
The pipeline leverages fully managed and serverless GCP services for scalability, reliability, and ease of operation.

1. **Yahoo Finance API:** Source of raw stock price and volume data.
2. **Cloud Composer (Apache Airflow):** Orchestrates the entire data pipeline, defining tasks, dependencies, and scheduling.
3. **Google Cloud Storage (GCS):** Acts as a data lake, storing raw JSON data and processed CSV files.
4. **Dataproc Serverless:** Provides on-demand, serverless Spark compute for data transformation (JSON to structured CSV).
5. **BigQuery:** A highly scalable, serverless data warehouse for storing the final processed data, ready for analytics and dashboarding.

### ✨ Features
1. **Automated Data Ingestion:** Daily fetching of Apple stock data.
2. **Event-Driven Processing:** Utilizes Airflow Sensors to wait for API availability.
3. **Serverless Data Processing:** Leverages Dataproc Serverless for scalable Spark transformations without cluster management.
4. **Scalable Data Lake:** Stores raw and processed data in GCS.
5. **Analytical Data Warehouse:** Loads clean data into BigQuery for fast querying.
6. **Robust Orchestration:** Managed Airflow (Cloud Composer) for workflow scheduling, monitoring, and error handling.
7. **Cross-Service Integration:** Demonstrates seamless integration between various GCP services.
8. **Notifications:** Automatic email notifications for pipeline status.
9. **Modular Design:** Separates concerns into distinct Airflow tasks and Python functions.
   
### ☁️ Google Cloud Services Used
1. Cloud Composer (Apache Airflow)
2. Google Cloud Storage (GCS)
3. Dataproc Serverless
4. BigQuery
5. Identity and Access Management (IAM)
6. Cloud Logging (for monitoring)
