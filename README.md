# MIST-4610-Project1

# Team Name 
29704 Group 6

# Team Members
1. Luis Garcia @LuisCVG
2. Emily Coffield @emilycoffieldd
3. Efe Guvenc @eguvenc03
4. Eris Jang @erissjang
5. Jessica Nguyen @jessngph09

# Problem Description
Grassroots Financial Empowerment Co. is at the forefront of fostering sustainable growth in economically challenged areas. By bridging the gap between the underprivileged and basic financial services, we grant microloans that help kick-start businesses, enhance living standards, and nurture dreams.
At the center of our business model is the Loan Details entity, which is fostered directly by other entities including Loan Seekers, Loan Guarantee, Transaction History, Audit Logs, Loan Renewal Requests, Repayment Monitor, Loan Training Details, and Loan Type.
These support entities are haloed by five additional entities on the periphery of the model listed in no particular order as Training Sessions, Loan Collateral, Loan Guarantor, Workforce, and Branch Information. 
We aim to populate this model with sample data and connect entities on a variety of attributes in order to position a data set that can be tabled by ten SQL queries. 
These queries are meant to simulate the value of the data set to a business minded user.

Conversations with ChatGPT: 

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/203fe8a5-676e-439e-8399-916e4c436b5f)

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/e0df9549-d44f-42f6-a5de-ec43a72e9a35)

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/96f5db29-de65-4936-acc8-a2d4f6e7b147)

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/998ccb90-1062-40da-a440-6343799b8282)

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/ee8f2147-3abe-4481-96e2-bf2d1e533583)





# Data Model
Grassroots Financial Empowerment Co. explained the relationships that exist between the fourteen entities we modeled, so our model was formed off the following specifications:

Each Loan Seeker can have one or multiple loans, but each Loan Detail is specifically associated with one Loan Seeker.

A Loan Seeker can provide multiple Loan Collaterals for different loans. Each Loan Collateral is associated with a single Loan Seeker.

Each Loan Seeker can have one or multiple Guarantors depending on loan types or company policies. Each Guarantor can stand for multiple Loan Seekers, but the relationship should specify which loans they are guaranteeing.

Each Loan Detail corresponds to a specific Loan Type which provides context on the nature of the loan. A Loan Type can be associated with multiple Loan Details. 

A Loan Seeker, through their Loan Details, might be recommended or required to attend multiple Training Sessions. A particular Loan Detail(or type of loan it represents) requires attendance at multiple Training Sessions, and each Training Session can correspond to multiple Loan Details. 

Every Loan Detail can have multiple transaction histories, but each transaction is linked to a specific loan. 

Each Loan Detail has one or multiple Repayment Monitors tracking each repayment cycle.

Every Loan Detail can have zero or one Loan Renewal Request, suggesting if a Loan Seeker has ever asked for a renewal. 

Audit logs are generated whenever there are changes or actions associated with loan details. Each specific action or change related to a loan will generate an audit log entry. Therefore, multiple audit log entries can correspond to a single loan detail to capture all its history of changes, but each audit log entry will correspond to only one specific change or action related to a loan.

A single member of the Workforce can be responsible for creating multiple Audit Logs. Each Audit Log entry is associated with one and only one member of the Workforce, indicating which employee was responsible for that action that the log records.

Each member of the Workforce is assigned to a specific branch, but naturally, a branch can house multiple Workforce members.

Each Loan Detail might require one or multiple Loan Collaterals depending on the loan amount and terms. 

![DataModelMIST4610GP1](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/8c5c7659-5ca1-4542-95d1-bca981c9f0ef)


# Data Dictionary

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/d5f6b4da-84fe-432e-a287-2a8ac2c2ff2a)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/0feb1f7d-1681-4898-8ea0-b92df75aa576)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/5d770f05-b3c0-4598-a9e9-8b35c76cbc07)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/15637f46-6ff7-4a9c-8370-a27dab9d33ac)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/cd5c6ae4-3fc7-418a-ac4a-fb8ce8145073)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/891b14be-5bb3-493b-9727-d1a18f69698d)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/a04ee563-5203-4d16-9a42-24535ee0ed3c)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/59acf6e3-c39a-4010-9359-fc82960d9b5f)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/c053f993-b4e9-4d65-8e4c-eaf5d8f09adf)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/bd689028-e239-424d-ae43-31331f7ee02e)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/02910368-407f-406f-a632-b69c7316dde5)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/36ddf943-f344-40fc-8b42-d3ca7105616d)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/82856745-13ee-4bd9-b99f-c87d341d1336)
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/3f55133d-21ad-419a-ac81-3bbac7d58c02)




# Ten Queries
![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/dd1b29a1-80c9-4052-b57c-d0f37cff5b80)

Query 1 lists the name of the loan seekers and a description of their business ventures. The query is useful for managers to see the trend of upcoming business ventures and study their user information.

Query:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/c538b62b-a099-4144-8d8b-4e1c3be68a83)

Response:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/dcb66bb0-db53-457c-8905-da0d7152a5c7)

Query 2 lists the audit log ID and changes made grouped by each employee that has written it. The query allows the managers to track which employee is responsible for which audit logs in case there is an instance when additional information is needed from the employee who wrote it. 

Query:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/61f9d9b6-8c53-4e7b-87ba-57c98c571907)

Response:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/4274486d-67e2-46b7-8cfb-f04348600aa8)


Query 3 lists all types of loans including their descriptions, typical loan range, and standard interest rates. Managers can view the basic, necessary information about the loans for both loan seekers and guarantors. 

Query:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/9f85a8ed-1bcf-47a5-bf30-45b525ac112d)

Response:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/4390365e-a457-427f-bfb0-0c72505c9078)

Query 4 lists the loan’s next due date and repaid amount for every loan seeker from the highest to lowest repaid amount order where the seeker has an overdue amount and a repayment amount higher than $1500. Managers can track the loan seekers who require more attention since these are the loan seekers who have a high repayment amount and an overdue amount. 

Query:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/72873c56-637a-4f79-b6eb-22a79a07d707)

Response:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/516a5eeb-502f-4b1b-b9ea-6bd4be7ae4f3)

Query 5 lists the names/positions/contacts of staff members that manage any loan within a specific intended use (to be declared by manager dependent on situation), making it useful for managers to track the directory of staff members that are associated with certain intended loans (who may want to assign these staff members to specific tasks).

Query: 

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/6fa9ba91-1b89-4a72-acae-1d1c93938d7e)

Response:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/6321a25d-fb8c-4cbf-ab17-1776eece9537)

Query 6 returns the name of all LoanSeekers along with their phone number and residential details, so it is a quick way for managers to access the directory for LoanSeekers (useful in the process of follow-up, mailing news, etc.)

Query:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/1a16028b-d3e7-4f93-b4b4-c1fb79a64fa0)

Response: 

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/71d28911-f694-4e15-90dc-0ead897aafb8)

Query 7 lists the names, intended uses of Loan Seekers who are giving up a collateral value above the total average which helps managers figure out the reasoning behind a higher value of collateral in correlation to the intended use of the loan.

Query:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/9a939d6d-a225-47c9-897c-638fe116d84a)

Response:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/d4dc5a4d-7c3c-4344-b850-4748a358aa65)

Query 8 lists the intended use of all loans with a requested amount higher than $5,000 (numerically in ascending order). It is important to figure out the purpose of loan requests. This query makes it possible to return the intended use of an amount above $5,000 (a respectable amount). This also allows managers to view trends and form relationships between the two variables.

Query/Procedure:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/665ef5fd-3128-4d4e-a0da-2ca6bbb98a8d)

Response:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/48841b26-1c4c-4a91-aa8f-da3eea2c2b9f)

Query 9 lists the recommended training type and the designated completion status for Loans that concern Medical Purposes. It is essential for managers to track the training programs associated with purposes amongst the Medical Field. It can be seen from the output that all purposes associated with the given field either require or recommend a form of training.

Query/Procedure:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/33b3def7-a55b-4c75-b74b-e0aab4139d44)

Response:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/c7128472-8c6e-4314-862f-07d0925a143f)

Query 10 lists loan seekers who are looking for a loan renewal along with their loan renewal reason and the requested renewal amount. The query is useful for managers because it allows them to view all the loan seekers who are looking for loan renewals and assess whether rewriting of the existing loan agreement is necessary.

Query:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/d4da8fad-d1d3-43d6-a8c9-972db43a64af)

Response:

![image](https://github.com/emilycoffieldd/MIST-4610-Project/assets/148081148/df1e06ce-791f-421d-84fd-74809c70d8af)


# Database Information

Name of Database: ns_F2329704Group6

All stored procedures can be called using the format TP_Qx (where x is to be replaced by the query number above it pertains to).
