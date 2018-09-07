# Database-Projects
## Dimensional Modeling

Dimensional modeling is a set of techniques and concepts that are developed in order to design a data warehouse. The first step to executing a dimensional model plan is to understand the business requirements for the project. This is where CEO’s and business executives and stakeholder’s opinions and concerns are consolidated in order to understand the business issue at hand. The data set provided is on public housing inspection data. Public housing is when the property is owned by the government thus inspections are performed in order to monitor its maintenance. We will consider the column “Inspection score” because it is a quantitative value and are additive figures. The inspection score adds onto each development name as the inspection occurs over and over, making this fact additive. There are other facts such as “Inspection date”, “Inspection ID”, “Inspection score”, “Inspection Date”, “Development ID”, “Address ID”, “State ID”, “CBSA CODE” and “PHA CODE”. 
These are the following dimensions and dimension tables that can be formed using the given data.
Development table: 
Development ID (PK), Development Name, Address ID(FK), Location Quality
Address Table:
Address ID(PK), Address, City, State ID(FK)	
State Table: 
State ID(PK), State Name, ZIP, Latitude, Longitude, CBSA CODE(FK)
CBSA Table: 
CBSA CODE(PK), County_name, County_code
PHA Table: 
PHA_CODE, Pha_Name

The granularity of the data can be determined from the above dimensions or vice versa. The related fields would be: 
•	Development ID, Inspection score, Development Name
•	Development ID, Inspection ID, Address
•	PHA_Code, PHA_name
•	CBSA_Code , County_name , County_code
Star Scheme is as follows:


![image](https://user-images.githubusercontent.com/31625655/45193092-61880c80-b21a-11e8-8195-b29ded7c099c.png)
 <img src="(https://user-images.githubusercontent.com/31625655/45193092-61880c80-b21a-11e8-8195-b29ded7c099c.png)" width="200" height="200" align="center" />

Relevant questions on this data set:
Which state has the highest number of inspections?
Which public housing has the lowest inspections score?
Which state received more than one inspection per year?
