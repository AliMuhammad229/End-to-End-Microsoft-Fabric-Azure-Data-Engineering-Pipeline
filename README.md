# End-to-End-Microsoft-Fabric-Azure-Data-Engineering-Pipeline

![diagram-export-10-3-2024-12_30_54-PM](https://github.com/user-attachments/assets/4a2f6bcc-8106-4060-aeb5-78a49586d704)

## Overview
This project demonstrates a **complete data engineering pipeline** using **Microsoft Fabric** and various **Azure services**. From fetching data via **Bing API** to processing it with **Synapse Data Engineering** and **Synapse Data Science**, and finally visualizing insights with **Power BI**, the pipeline covers all the steps in a modern data solution.

---

## Architecture

The architecture follows a modular approach:

```mermaid
graph TD;
    A[Bing API] --> B[Azure Data Factory];
    B --> C[JSON Storage];
    C --> D[Synapse Data Science];
    C --> E[Synapse Data Engineering];
    D --> F[Power BI];
    E --> F;
```

## Data Flow
1. Data Ingestion: Fetch data via the Bing API using relevant search query parameters.
2. Data Processing & Machine Learning:
   - Synapse Data Science ML: the AnalyzedText model processes the textual data.
   - Snapse Data Engineering: transforms and enriches data.
3. Data Storage: Data is stored in JSON format and Lakehouse DB for efficient access.
4. Visualization: Power BI connects to the data sources to create rich, interactive dashboards.

## Prerequisites
1. Azure Subscription with access to:
   - Bing API credentials.
   - Azure services like Data Factory, Synapse Data Science, Synapse Data Engineering, Lakehouse DB, and Power BI.
Bing API Key for fetching news data (https://learn.microsoft.com/en-us/bing/search-apis/bing-news-search/reference/query-parameters)
