# ETL SCD1 using Snowflake Tasks, Streams & Stored Procedure

## 📌 Project Overview

This project demonstrates how to implement a Slowly Changing Dimension Type 1 (SCD1) data pipeline using **Snowflake**, **AWS S3**, and **Snowflake-native features** such as **Streams**, **Tasks**, and **Stored Procedures**. The project simulates real-world scenarios where customer records are updated over time, and we want to keep only the latest version of the data (Type 1).

The entire pipeline follows an end-to-end approach:
- Ingesting data from files stored in **AWS S3**
- Using **Snowpipe** for continuous data loading into Snowflake
- Tracking changes using **Streams**
- Automating updates via **Tasks** and **Stored Procedures**

---

## 🚀 Why This Project Is Important

- ✅ **Real-World Relevance**: SCD1 is one of the most common ETL scenarios in Data Warehousing.
- 🧠 **Hands-On Practice**: You learn practical skills in Snowflake, S3, SQL scripting, and automation.
- 🔁 **Automation & Scheduling**: Shows how to set up automated pipelines without 3rd-party tools.
- 📦 **Cloud-Based & Scalable**: Uses fully cloud-native architecture with Snowflake and AWS.
- 🧩 **Modular Setup**: Each part of the pipeline can be reused and adapted to other use cases.

---

## 🔧 Technologies Used

| Tool/Service      | Purpose                                 |
|-------------------|-----------------------------------------|
| Snowflake         | Cloud Data Warehouse                    |
| AWS S3            | Storage for raw and change data files   |
| Snowpipe          | Automated data loading into Snowflake   |
| Streams           | Tracks changes in staging tables        |
| Tasks             | Schedules and triggers procedures       |
| Stored Procedures | Executes the SCD1 logic using SQL       |
| Anaconda          | Local environment for file preparation  |

---

## 📂 Project Structure



---

## 🧪 Pipeline Flow & Components

| Step | Description                                 | Status |
|------|---------------------------------------------|--------|
| 1    | Snowflake Account Setup                     | ✅ Done |
| 2    | AWS Account Setup                           | ✅ Done |
| 3    | Anaconda Cloud Setup                        | ✅ Done |
| 4    | AWS IAM User Configuration                  | ✅ Done |
| 5    | AWS S3 Bucket Setup                         | ✅ Done |
| 6    | AWS S3 + Snowflake Integration              | ✅ Done |
| 7    | Snowflake Snowpipe Setup                    | ✅ Done |
| 8    | Snowflake Stream Setup                      | ✅ Done |
| 9    | Snowflake Task Setup                        | ✅ Done |
|    |                        |  |

---

## 🧠 SCD1 Logic (How It Works)

1. **Initial Load**: Full customer dataset (`customer_full_data`) is loaded into Snowflake using Snowpipe.
2. **Change File Upload**: Change file (`customer_change_dataFile`) is uploaded to S3 and auto-loaded via Snowpipe.
3. **Stream**: A stream object tracks new/changed rows from the staging table.
4. **Stored Procedure**:
   - If customer ID exists: **update** the record with new values.
   - If customer ID does not exist: **insert** as a new row.
5. **Task**: A Snowflake task runs the procedure at regular intervals or upon file arrival.

---

## 📸 Screenshots

| Step                         | Screenshot |
|------------------------------|------------|
| Snowflake Setup              | ![Snowflake Setup](./images/snowflake-setup.png) |
| AWS S3 Bucket Configuration  | ![S3 Setup](./images/s3-setup.png) |
| Snowpipe Integration         | ![Snowpipe](./images/snowpipe.png) |
| Stream Creation              | ![Stream](./images/) |
| Task Scheduling              | ![Task](./images) |

---

## ✅ Future Improvements

- 🔁 Add **SCD Type 2** logic with historical tracking
- 📊 Connect to dashboards for real-time customer insights
- 🔔 Add alerting and monitoring with Snowflake Alerts or AWS SNS
- 🔌 Integrate source systems like Postgres, MySQL, or DynamoDB

---

## 🧑‍💻 Author

**Your Name**  
Cloud & Data Engineering Enthusiast  
🔗 [LinkedIn](www.linkedin.com/in/enochnumotetteh)  
🐙 [GitHub](https://github.com/numoenochtetteh)

---




