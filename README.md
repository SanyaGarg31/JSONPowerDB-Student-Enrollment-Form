![image](https://github.com/user-attachments/assets/67a7ef29-d4ec-440e-bfdc-cde282e4eaa9)
![image](https://github.com/user-attachments/assets/64d69572-83f2-4e11-afa2-86b614f5779e)
![image](https://github.com/user-attachments/assets/cfe09d7d-47d4-4a9e-9260-f5932c9ce770)




## 📂 Categories




### 📚 Standards and Frameworks
{expand:title=View Standards and Frameworks}
- [ISO Standards Overview](#)
- [Framework Guidelines](#)
- [Compliance Checklist](#)
{expand}

---

### 📝 Procedures
{expand:title=View Procedures}
- [Step-by-Step Onboarding](#)
- [Incident Handling Procedure](#)
- [Approval Workflow](#)
{expand}

---

### 🛠️ Design Diagrams
{expand:title=View Design Diagrams}
- [System Architecture](#)
- [Database Schema](#)
- [Component Diagrams](#)
{expand}

---

### 🔄 Logical Flows
{expand:title=View Logical Flows}
- [Authentication Flow](#)
- [Data Processing Flow](#)
- [Error Handling Flow](#)
{expand}

---

### 🎨 UI/UX Flows
{expand:title=View UI/UX Flows}
- [User Login Flow](#)
- [Checkout Process](#)
- [Interactive Prototypes](#)
{expand}



# JSONPowerDB-Student-Enrollment-Form
This repository is in lieu with the micro course 'JSONPowerDB' of Login2EXplore

Name: Sanya Garg

Education: BTech, Computer Science and Engineering

Email: sanya.garg318@gmail.com

Objective: Micro Project Work

Title of the Project : Student Enrollment Form

Description : Student Enrollment Form that will store data in STUDENT-TABLE relation of SCHOOL-DB database. Input Fields: {Roll-No, Full-Name, Class, Birth-Date, Address, Enrollment-Date} and Primary key: Roll No.

Benefits of using JsonPowerDB : It is a real-time, lightweight REST API based multi-mode DBMS. It defines set of constraints/architectural style between client applications and API servers while integration of a database supporting mutiple data models. It is a ready-to-use API for Json Documents DB, RDBMS, time series DB functionality. It supports serverless and pluggable API development. It is schema free with multiple security layers, build around the world's fastest indexing engine PowerIndex.

Release History (release of your JsonPowerDB related code on Github)

Table of contents: Columns: Roll-No, Full Name, Class, Birth-Date, Address, Enrollment-Date, and Buttons: Save, Change and Reset

Illustrations:
![image](https://github.com/SanyaGarg31/JSONPowerDB-Student-Enrollment-Form/assets/95563058/c5a472ce-6edb-48f3-bc6d-61af32d4b8a9)

Generating Connection Token:
![image](https://github.com/SanyaGarg31/JSONPowerDB-Student-Enrollment-Form/assets/95563058/09a3bc7c-0c55-43fd-943a-0ddc31cba36d)

![image](https://github.com/SanyaGarg31/JSONPowerDB-Student-Enrollment-Form/assets/95563058/89c4b669-e6d1-4c01-8879-e2af83694177)

![image](https://github.com/SanyaGarg31/JSONPowerDB-Student-Enrollment-Form/assets/95563058/89434929-f538-4452-a6b7-4c7c0def4f67)

![image](https://github.com/SanyaGarg31/JSONPowerDB-Student-Enrollment-Form/assets/95563058/6e1fc058-ba4f-4a4a-8209-aa9d7c15d87f)

When the field is empty:
![image](https://github.com/SanyaGarg31/JSONPowerDB-Student-Enrollment-Form/assets/95563058/c398c963-454e-42be-8b24-2abdb0c77959)

Data feeded in the database:
![image](https://github.com/SanyaGarg31/JSONPowerDB-Student-Enrollment-Form/assets/95563058/f9ec2191-9522-4670-9464-5da91328256c)

Scope of functionalities : We can insert records into the the database with the 'Save' button, Update records in the database with the 'Change' button, Clear entered values in the form using the 'Reset' button and Remove records from the Database.

Examples of use : Use cases involve getting data of applicants to any firm or employee data in a company.

Project status : Done

Sources :Introduction to JsonPowerDB - V2.0
![image](https://github.com/user-attachments/assets/52a54115-b5ae-4f57-a81f-d541d4277dc1)
![image](https://github.com/user-attachments/assets/9aebb185-5ce6-49b1-a5cf-e98941a28e4d)
![image](https://github.com/user-attachments/assets/4f70df29-15eb-40a4-ba48-8c4e5316fd3b)
![image](https://github.com/user-attachments/assets/94ccec0c-424c-4842-a2f2-a77a1f56bd98)
![image](https://github.com/user-attachments/assets/f609c1a8-5618-4931-ae0f-e1fbfdefad73)



Step 1:
Fetch rolling average data from the table considering a window of +5 and -5 days around the target date.

Step 2:
Retrieve the current day's record count from the database.

Step 3:
Set buffer limits based on the rolling average to define acceptable thresholds for record counts. These limits help in determining whether the data upload was successful or if there is a potential anomaly.

Step 4:
Perform an Anomaly Check by comparing the current day's count against the buffer limits.

Step 5:
Insert the calculated rolling average and buffer data into the Hive table for historical tracking and reference.

Step 6:
Generate an Anomaly Report summarizing deviations, highlighting affected tables, and calculating deviation percentages.

Step 7:
Trigger an Email Alert to the concerned team, notifying them immediately about the detected anomalies and attaching the report.

Module 1: Buffer Calculation
📏

Objective:
Establish a smart, adaptive range that defines "acceptable" data fluctuations for each table.

Functionality:

Fetch historical record counts for the previous 5 days and the next 5 days (if available).

Calculate a rolling average of record counts.

Define upper and lower buffer limits (example: ±10%) around this average.

These buffer limits will act as the baseline for detecting any anomalies in current day's data ingestion.

Outcome:
A dynamic tolerance window that evolves with time, making the anomaly detection context-aware and reliable.

Module 2: Internet Protocol (IP) Module
🌐

Objective:
Connect securely to the target databases and pull real-time data counts.

Functionality:

Establish network connection with the Big Data system (Hive, HDFS, etc.).

Retrieve the current day's record count based on the ingestion date (usually n-1).

Handle exceptions like network failures, table unavailability, and data access issues.

Outcome:
Accurate retrieval of the live operational data for anomaly checking, ensuring connectivity is reliable and consistent.

Module 3: Detect and Confirm Anomaly
🚨

Objective:
Identify significant deviations from expected record counts and confirm anomalies with precision.

Functionality:

Compare today's actual record count with the calculated buffer range.

Classify outcomes:

Within range → No anomaly detected.

Outside range → Potential anomaly detected.

Categorize severity (Normal, Minor, Major, Critical) based on the percentage deviation.

Outcome:
Fast, automated detection of suspicious drops or spikes in data volume to proactively safeguard fraud detection systems.

Module 4: Create an Anomaly Report
📝

Objective:
Compile findings into a structured, visual format that can be easily reviewed and analyzed.

Functionality:

Create a tabular report listing:

Date

Table Name

Actual Record Count

Rolling Average

Deviation Percentage

Severity Level

Include color-coding for quick visual analysis (green for normal, yellow for warning, red for breach).

Outcome:
A crisp, easy-to-understand report that summarizes the health of data ingestion processes at a glance.

Module 5: Trigger Email with Anomaly Report
📧

Objective:
Ensure that relevant stakeholders are alerted promptly to take corrective action.

Functionality:

Auto-generate an email notification if any anomaly is detected.

Attach the generated anomaly report.

Highlight critical anomalies directly in the email body for faster visibility.

Outcome:
Quick dissemination of important information, enabling timely investigation and resolution of data issues.

