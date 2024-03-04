Project Title:
Workforce forecasting and planning analysis. 
Contact Information:
Md Taqi Tahmid Hussain
Mdtaqitahmid.Hussain18@bcmail.cuny.edu


Abstract:
The HR Operations and Analytics - Workforce Planning and Position Management team at the MTA is tasked with preparing forecasting and analysis for various MTA agencies. This involves implementing an enterprise-wide recruitment strategy to address the expansive demands to fill vacant positions across the MTA agencies. The team collaborates with MTA agencies and other members of the People Department to design and implement a standardized workforce planning process that aligns hiring plans with the MTA’s strategic goals and Talent Acquisition’s recruitment efforts.

As an intern I  will support the Workforce Planning and Position Management team by assisting in creating and developing forecast reporting mainly. I will help with the data gathering process and work as an analyst  to establish metrics and overall workforce analytics. Additionally, I will assist in generating various reports and performing data analysis. Sometimes, I will  also participate in discussions with areas of the People organization, such as Talent Acquisition, in the development of hiring and recruitment plans.


Diagrams:

Data Gathering:  
The data for a specific agency needs to be created as per their company name. The managers and supervisors are requested by other agencies to create reports by a certain deadline.  Then the process starts. 
![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/15a448db-22d6-4ec0-8cac-a82e4765f385)

Data Preparation:

Generally, 3 main data files are prepared to make the reporting. The file names are: Headcount, hire promotion file, and Transfer file. These 3 files need to be created according to the agency name. 

![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/b3688fb0-a3c4-481a-b984-9cb4dca67a1a)










so, these 3 data files are created:
![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/f0e2778a-f2fd-4e50-ad21-29f6ac59f815)


Fig: The 3 prepared data files for reporting. 
Head count: 
The headcount basically creates the prediction of retirement eligibles in upcoming years and has the total headcount of an agency from the last 5 years.

Based on age, length of service, last start date of an employee the retirement eligibles are determined. The age of current year is the actual one for the upcoming years 1 is added. For length of service (LOS) it’s the same. In retirement eligible (RET ELIG)  an if else condition is used to determine the retirement eligibles. The MTA has specific retirement categories and based on that the retirement eligible is defined. There are specific unions in which employees join which are also an important factor for retirement eligibility. So, the user needs to filter the last start date and union first. Then based on that they will insert the formula in the retirement eligibles column. Then by dragging the data needs to be filled up. 


![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/fd4a1f32-8ea0-4ce3-bfb5-e171c5b676f5)


This process will be followed for every set of unions. Once these steps are followed. There might be blanks , and union titles named interns might be there. The interns are not any part of the retirement eligible. So, these will be deleted and the blanks need to be checked for correct data. There are columns where data needs to be retrieved from other files. Like for departments, union titles. These data don’t come with the original data. So, we use Vlookup to get those from another file. The action, reason columns are the actions taken for the employee like promotion, transfer, hire and reason for that.  Finally, a pivot table needs to be created to see if the numbers make sense.
![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/3c34fa5b-807f-4306-8924-a49e2ab83a24)


Hire Promotion: 
This one is used to find out the hire, promotion, retirements of the current year and past 4 years. The retirement eligible here is also available but only for the current year. There are some columns where extra data is needed. These are the department, union titles. 
The vlookup formula used for the union titles or other column like department act/ reason desc is generally this: 
=VLOOKUP(“Union column name/ column name I’m going to compare to”,’File name from which the data needs to be extracted for union names and the selection of data”,The columns until which the union column name will be compared to”,FALSE). 
   This is basically the same for headcount and other upcoming files.

![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/f799b660-d5df-4e1b-810e-8a3b5f24085e)



Transfer File:
This file is used for transfer related data. To know how many transfers a agency had based on unions, based on positions, if the transfer happened within the agency or out of the agency. These data are extracted from this file. Some new columns are created for this . Apart from the previous data some extra columns related to the transfer is added: 

All these data are gathered by using VLookup. New act/ reason is the action taken for the employee due to promotion/ hire/ transfer. The report name is generally  promotion, resignation, retirement.

![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/3b9da40d-d7ac-4a87-a345-6557e13c57f5)

Reporting: 
The reporting is done from headcount , hire promotion and transfer file. 
Each report consists of the following reports:
1. Summary
2. Hire, promotion , transfer 
3. Retirement summary
4. Eligible retirements
5. Transfers
6. Attrition by union. 
![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/5ea8890a-97c9-4ca2-a852-ba0dbd7043cd)


Fig: Extraction of the data from the data files that are prepared. 




1. Summary: This report has the overview of the whole report. The headcount is available along with attrition of the employees under unions or without unions.
                                                               
![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/910a817c-3e84-485f-a1b1-5adc07ee229c)


2. Hire Promotion & Transfer Summary: 

   This one has the hire promotion and transfer from 2017-2023
![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/22e174de-7918-4c35-b1fa-d500ac19ea40)

Here, 3 years are shown but the years needed to report are up to 2023.

3. Retirement summary: 
The retirement summary generally has 3 tables like this. Other two are union employees and their retirement eligibles and non unions. Charts are added to each of the tables. The charts are bar chart. 

![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/bebd2500-6909-4e75-8fc9-bbeecd2a1fac)

	
 


4.Eligible Retirements:
![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/b93ac630-13cd-47d8-9f3f-397712b436a2)

So, here we predict the retirement eligibles from the headcount file for the upcoming 5 years. 

5. Transfers: 
The transfer data is collected from the transfer file. The transfers in and out are found out until running year to past 5 years. VAR is the difference in transferring in and out. The first table is the number of people who got in based on departments. The Agency Transfer in is the amount of people who transferred in the agency and the transfer out is vice versa 
![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/7090642b-fc89-4afd-b498-3f33202d5652)


6. Attrition by union: 
This is basically , the resignation, retirement, termination and death of the employees. The data is retrieved from the hire promotion file. The Headcount in the 2nd table is taken from the headcount file. It’s basically the headcounts by unions. The percentage in the first table is the cell’s value / previous year’s headcount’s value. 

![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/4e9988d0-83e1-42ab-9f1f-6a10478a54d8)


User Interface: 
The user is going to see the completed report. So, they’ll start seeing it from the beginning and here’s a glimpse:
![image](https://github.com/Taqit2000/CISC4900-/assets/120526002/dbc54bab-f92f-4061-af00-cfaa2dee1377)


Next Steps: After we’re done with reporting the reports are sent to the supervisors and it gets another revision. After that the reports are sent to managers. If the reports have mistakes we change them accordingly. 


