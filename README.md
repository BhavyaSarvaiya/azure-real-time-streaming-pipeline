Real-Time Streaming Platform Pipeline with Analytics and NoSQL Database
Project Overview
This project implements an end-to-end real-time streaming data pipeline using Microsoft Azure. Clickstream data is simulated in Google Colab, streamed to Azure Event Hub, processed using Azure Stream Analytics, stored in Azure SQL Database and Azure Cosmos DB, and visualized through interactive Power BI dashboards.
The system demonstrates event-driven architecture, real-time stream processing, dual-database storage (SQL + NoSQL), and cloud-based analytics. It showcases how modern cloud platforms can handle scalable real-time data workloads efficiently.

Architecture

Google Colab (Data Producer)
        ↓
Azure Event Hub (Ingestion Layer)
        ↓
Azure Stream Analytics (Processing Layer)
        ↓
Azure SQL Database (Structured Storage)
Azure Cosmos DB (NoSQL Storage)
        ↓
Power BI (Visualization Layer)

Technologies Used
* Microsoft Azure
* Azure Event Hub
* Azure Stream Analytics
* Azure SQL Database
* Azure Cosmos DB
* Power BI
* Python (pandas, azure-eventhub SDK)
* Google Colab

Project Workflow

1. Clickstream dataset loaded and preprocessed using pandas.
2. Timestamps converted to datetime and sorted chronologically.
3. Time differences between events calculated.
4. Replay delay implemented with compression factor.
5. Maximum replay delay capped to ensure smooth streaming.
6. Events streamed to Azure Event Hub using Python SDK.
7. Stream Analytics processes incoming data using SQL-like queries.
8. Processed data routed to:
   * Azure SQL Database (relational storage)
   * Azure Cosmos DB (NoSQL storage)
9. Power BI connected to create live dashboards.

Dashboard Insights
* Live User Count
* User Activity by Source
* Navigation Trends per User
* Time-based Event Distribution
The dashboard updates dynamically based on incoming streaming data.

 Repository Structure
azure_realtime_streaming_pipeline/
│
├── notebooks/
│   └── azure_realtime_streaming_pipeline.ipynb
│
├── Documentation/
│   └── (Azure_Realtime_Streaming_pipeline_Documentation)
│
├── data/
│   └──All_clickstream.csv
│
└── README.md

How to Run
1. Open the notebook in Google Colab.
2. Install required dependency:
   "pip install azure-eventhub"
3. Replace the placeholder connection string with your Azure Event Hub connection string.
4. Run all cells to start real-time streaming simulation.

Key Learning Outcomes
* Designed a real-time cloud-based streaming architecture
* Implemented event replay simulation
* Configured Azure Stream Analytics inputs and outputs
* Integrated relational and NoSQL cloud databases
* Built interactive real-time dashboards in Power BI
* Understood scalability, partitioning, and stream processing concepts

Final Outcome
Successfully built a scalable, end-to-end real-time streaming analytics pipeline using Microsoft Azure services, demonstrating practical cloud data engineering and real-time analytics implementation.
