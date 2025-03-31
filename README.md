## 📂 Categories

public static JSONObject getGroovyRuleJson(String appName) {
    return new JSONObject()
        .put("className", "com.pingidentity.pa.policy.GroovyPolicyInterceptor")
        .put("name", "A1234" + appName + "Reqit: groovy") // Dynamic app name
        .put("supportedDestinations", new JSONArray()
            .put("Site")
            .put("Agent")
        )
        .put("configuration", new JSONObject()
            .put("rejectionHandlingEnabled", false)
            .put("rejectionHandler", JSONObject.NULL) // Correct JSON null representation
            .put("errorResponseCode", 403)
            .put("errorResponseStatusMsg", "Forbidden")
            .put("errorResponseTemplateFile", "policy.error.page.template.html")
            .put("errorResponseContentType", "text/html;charset=UTF-8")
            .put("groovyScript", 
                "def useragent=exc?.request?.header?.getFirstValue(\"User-Agent\");\\ndef ua=useragent;"
            )
        );
}






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





