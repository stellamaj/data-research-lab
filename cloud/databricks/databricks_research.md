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

Key characteristics:
- Fast processing of transactions
- High number of small operations
- Focus on current data (not historical analysis)
- Supports many users at the same time

Examples:
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

Key characteristics:
- Focus on data analysis and insights  
- Works with large historical datasets  
- Fast reading and querying of data  
- Used for decision making rather than operations  

Examples:
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

How it works:
Data is collected from different systems (such as databases, applications, and files), then:
- Extracted from source systems (copied from the original systems)
- Transformed into a consistent format (cleaned and standardised the data)
- Loaded into the data warehouse (ETL process)

Once stored, the data is used for:
- Reporting  
- Dashboards  
- Business analysis  
- Decision making  

**Key idea:**
A data warehouse brings data together in one place so it can be analysed efficiently.

**Simple explanation:**
Data warehouses store data as files across multiple servers, but the data inside those files is organised and presented to users as tables.

- What are Data Lakes? How do they work?
- What are Data Lakehouses?
- What are Delta Lakes?

