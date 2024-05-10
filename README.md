# ETL-Project--Spar-Nord-Bank---AM---SRB

This project serves as a comprehensive test of knowledge in batch processing tools, focusing on Apache Sqoop, Apache PySpark, Amazon S3, and Amazon RedShift—industry-standard tools. Centered on a real-world scenario from the banking sector, the task is to construct a batch ETL pipeline. This pipeline will entail reading transactional data from RDS, transforming it, and subsequently loading it into Redshift Tables. Additionally, executing analytical queries on the loaded data to fulfill the project requirements.

**Dataset:**
In this project, participants will analyze a Danish ATM Transactions Data Set, comprising approximately 2.5 million withdrawal records from 113 ATMs in 2017, alongside weather information at the transaction time. The dataset is divided into two files totaling around 503 MB. There are 33 columns present in the dataset. Transactional data includes transaction date and time, ATM status, and details such as ATM ID, manufacturer, and location. Additionally, weather data includes location details and parameters like temperature, pressure, and wind speed.

The dataset has been released by Spar Nord Bank on Kaggle under the Database Contents License (DbCL) v1.0 — Open Data Commons.

Source of the Data Set in Kaggle: https://www.kaggle.com/sparnord/danish-atm-transactions

**Target Dimension Model:**
For this project, four dimension tables and one fact table are required, as outlined below:

1. ATM Dimension: This dimension includes data related to ATMs, such as ATM number (ATM ID in the original dataset), ATM manufacturer, and a reference to the ATM location. It is crucial for analytical queries involving ATM data.

2. Location Dimension: This dimension contains comprehensive location data, including location name, street name, street number, zip code, and latitude and longitude coordinates. This information is vital for pinpointing transaction locations and analyzing demand variations among different locations, especially when combined with weather data.

3. Date Dimension: This dimension includes fields such as full date and time timestamp, year, month, day, hour, and weekday for transactions. It facilitates analysis of transaction behavior over time, including variations by hour, day, and weekday.

4. Card Type Dimension: This dimension provides information about the card types used for transactions. It enables analysis of transaction patterns based on different card types.

5. Transaction Fact: This fact table contains numerical data such as transaction currency, service type, transaction amount, message code and text, as well as weather information such as description and weather ID. It serves as the core data repository for the dataset, enabling comprehensive analysis of transactional and weather-related metrics.


