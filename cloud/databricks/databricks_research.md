## Question 1
What can be considered "Big Data"?

### Answer
Big Data is data that is too large, complex, or fast-moving to be efficiently processed using traditional data processing tools.

It is often described by the 3 Vs:

• Volume: very large amounts of data  
• Velocity: data generated and processed quickly  
• Variety: different types of data such as text, images, video, and sensor data

Examples include social media data, online shopping transactions, IoT sensor data, streaming services data, financial market data, and healthcare records.

## Question 2  
What is OLTP?

### Answer  
OLTP (Online Transaction Processing) is a system designed to handle a large number of short, fast, and real-time database transactions.

It is used for day-to-day operations where data is constantly inserted, updated, or deleted.

**Key characteristics:**
- Fast processing of transactions
- High number of small operations
- Focus on current data (not historical analysis)
- Supports many users at the same time

**Examples:**
- Bank transactions (withdrawals, deposits)
- Online shopping orders
- Booking systems (flights, hotels)
- Payment processing systems

## Question 3  
What is ACID?

### Answer  
ACID is a set of properties that ensure reliable processing of database transactions.

It stands for:

- Atomicity: A transaction is fully completed or not done at all  
- Consistency: A transaction takes the database from one valid state to another  
- Isolation: Transactions do not interfere with each other  
- Durability: Once a transaction is committed, it is permanently saved

## Question 4  
What is OLAP?

## Answer  
OLAP (Online Analytical Processing) is a system designed for analysing large amounts of historical data.

It is used for complex queries, reporting, and data analysis rather than day-to-day transactions.

**Key characteristics:**
- Focus on data analysis and insights  
- Works with large historical datasets  
- Fast reading and querying of data  
- Used for decision making rather than operations  

**Examples:**
- Sales trend analysis  
- Financial reporting  
- Business intelligence dashboards  
- Market analysis
  
## Question 5  
What are Data Warehouses? How do they work?

### Answer  
A data warehouse is a central system used to store large amounts of structured data from multiple sources for analysis and reporting.

It is designed for querying and analysis rather than day-to-day operations (A data warehouse is not used for running live business actions, but for analysing past data and creating reports.)

A giant organised storage system in the cloud where companies keep cleaned data so they can analyse it easily.

**Examples of data warehouse services:**
- Amazon Redshift (AWS)  
- Google BigQuery (Google Cloud)  
- Snowflake (runs on AWS / Azure / GCP)  
- Azure Synapse (Microsoft)

**How it works:**
Data is collected from different systems (such as databases, applications, and files), then:
- Extracted from source systems (copied from the original systems)
- Transformed into a consistent format (cleaned and standardised the data)
- Loaded into the data warehouse (ETL process)

**Once stored, the data is used for:**
- Reporting  
- Dashboards  
- Business analysis  
- Decision making  

**Key idea:**
A data warehouse brings data together in one place so it can be analysed efficiently.

**Simple explanation:**
Data warehouses store data as files across multiple servers, but the data inside those files is organised and presented to users as tables.

## Question 6
What are Data Lakes? How do they work?

### Answer  
A data lake is a storage system that holds large amounts of raw data in its original format.

It can store structured data (tables), semi-structured data (JSON, XML), and unstructured data (images, videos, logs).

**How it works:**
Data is collected from different sources and stored directly into the data lake without being heavily processed first.

Later, when needed, the data is processed and analysed for specific use cases.

**Key idea:**
Unlike a data warehouse, a data lake stores raw data first and structures it later when needed.

## Question 7
What are Data Lakehouses?

### Answer  
A data lakehouse is a modern data architecture that combines the features of a data lake and a data warehouse.

It allows organisations to store all types of data (like a data lake) while also supporting structured data and fast analytics (like a data warehouse).

**How it works:**
- Data is stored in low-cost storage like a data lake  
- On top of this storage, a structured layer is added  
- This allows SQL queries, analytics, and machine learning on the same data  

**Key idea:**
A lakehouse brings together the flexibility of a data lake and the structure and performance of a data warehouse in one system.

## Question 8
What are Delta Lakes?

### Answer  
Delta Lake is an open-source storage layer that adds reliability and structure to a data lake.

It works on top of data lake storage (such as cloud storage) and improves how data is stored and managed.

**Key features:**
- Ensures data reliability using ACID transactions  
- Supports fast queries on large datasets  
- Allows both batch and streaming data processing  
- Keeps data consistent even when multiple users access it  

**Key idea:**
Delta Lake turns a basic data lake into a more reliable and structured system, often used in lakehouse architectures.

## Question 9
What is Apache Spark?

### Answer  
Apache Spark is a fast, open-source data processing framework used for big data analytics.

It allows distributed processing, meaning it can handle large datasets by splitting work across multiple computers.

**Key features:**
- Very fast processing (in-memory computing)  
- Works with large-scale data  
- Supports multiple languages (Python, Scala, Java, SQL)  
- Can process batch data and streaming data  

**Key idea:**
Apache Spark is used to process and analyse big data efficiently by distributing tasks across many machines.




### Additional Notes

✅ Data Warehouse  
- mainly structured data (tables: rows + columns)  
- data is cleaned and organised before storage  
- used for analysis and reporting  

✅ Data Lake  
- stores all types of data  
  - structured (tables)  
  - semi-structured (JSON, logs)  
  - unstructured (images, videos, text)  
- data is kept in raw form first  
- structured later when needed  

✅ Simple summary  
Warehouse = clean, structured data  
Lake = all raw data types stored as they are  
