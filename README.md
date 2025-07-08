# DSA-_Power-BI-Project
This project explores gender distribution, pay gap, and salary compliance within a fictional manufacturing company, Palmoria Group, using Power BI. The analysis was conducted as part of a training program by Digital Skillup Africa (DSA) and aims to uncover insights around workplace fairness, regulatory compliance, and bonus allocation.

# Project Topic:  Palmora Group HR Analysis 

#  Introduction
 The Palmoria Group, a manufacturing company based in Nigeria, is embroiled in issues 
bordering on gender inequality in its 3 regions. Unfortunately, the media recently 
published the news with the headline “Palmoria, the Manufacturing Patriarchy”. This 
doesn’t look good for the owners of the business, based on their ambition to scale the 
business to other regions and even overseas. Cases like this can only spiral downwards, 
revealing other issues like the gender pay gap, amongst other possible issues.
The CEO of Palmoria, Mr Ayodeji Chukwuma, is keen to address these issues before they 
get out of hand. The CHRO, Mr Yunus Shofoluwe, has been assigned the task to identify 
key areas within the business that could give rise to issues and address them immediately. 
Mr Shofoluwe decided to recruit you as an HR Analytics expert to analyse the company’s 
HR data and come up with recommendations for management’s attention. “Now, the 
future of gender equality in Palmoria lies in your hands” – the exact words of Mr 
Shofoluwe before he handed the data to you.

## Data Source
This documentation outlines the data cleaning process for the Palmoria Group Business. A 3 sets of data was given to work on and to know about the issues the company is currently facing. The datasets are given below;

- The bonus mapping : This contains the rule for making payments to the employees in the company and their work rating
- The bonus rules : This contains the rule for making payments to the employees in the company and their work rating
- Palmoria Group_emp_data : This contains the employees details

  ## Problem Statment
  ### CASE SCENARIO 
  Analyse the company data and generate insights that the Palmoria management 
team would need to address 
● Your analysis should be visualised using appropriate charts 
● Your focus should be on gender-related issues within the organization and its 
regions 
● The insights required are based on your discretion. However, Mr Gamma, as an 
insider, has offered to give you pointers on areas you need to pay attention to  
Required: 
● Generally, there are two genders in the organization. However, some employees 
refused to disclose their gender. You would need to assign a generic gender status 
to these employees 
● Some employees are without a salary because they are no longer with the company. 
You will need to take those employees out 
● Lastly, some departments are indicated as “NULL”. These departments would also 
need to be taken out. 
Pointers from Mr Gamma 
   1. What is the gender distribution in the organization? Distil to regions and 
departments 
   2. Show insights on ratings based on gender 
   3. Analyse the company’s salary structure. Identify if there is a gender pay gap. If 
there is, identify the department and regions that should be the focus of 
management 
   4. A recent regulation was adopted which requires manufacturing companies to pay 
employees a minimum of $90,000 
● Does Palmoria meet this requirement? 
● Show the pay distribution of employees grouped by a band of $10,000. For example: 
● How many employees fall into a band of $10,000 – $20,000, $20,000 – $30,000, 
etc.? 
● Also visualize this by regions 

Case Questions

 iv. Mr Gamma thought to himself that since you were already working on the employee 
data, you could help out with allocating the annual bonus pay to employees based on the

### DATA Description;
The Palmoria Group manufacturing company gave out a data set of 3 different tables which are the bonus mapping, bonus rules and the Palmoria Group_emp-data. The bonus mapping and bonus rules consists of 12 rows and 6 columns while the Palmoria Group_emp_data consists of 6 columns and 1015 rows.. The Palmoria Group_emp_data tables contains a range of the employees details related to the Palmoria company staffs, such as Employees name, Gender, department, salary, location and rating While the bonus rules and mappings which are the same consist of 12 rows and 6 columns .The columns consists of the department and the ratings ie very poor, poor, very good, good and average

#### Palmoria HR Dashboard ![image](https://github.com/user-attachments/assets/d2b4d58b-d3de-4a75-bf60-0ec79edcf37b)





### Skills/ Concepts Demonstrated
I looked into the data set and the data cleaning process was completed using Power Query, a powerful data transformation tool and I analyzed and generate an insights the management team need to address

- DAX

- Qucik Measures

- Page Navigation

- Modelling

- Filters

- Calculated columns

Data Cleaning Process
Using M language and a host of tools available in Power Query Editor, I was able to perform the following transformation to the data set

Text Cleaning
One of the issues identified during the data cleaning process was with the “Gender” column. The column contains male, female and blank so I replaced the blank with Unspecifed. The power query replaced values was used.
#### Before Column 
![image](https://github.com/user-attachments/assets/b1b090d6-5da8-4760-b40f-29c1481ed755)

#### After COlumn
![image](https://github.com/user-attachments/assets/b2ff42a0-5f4c-4c2a-b9d3-77bafc397897)



Department column
There are few rows that has a “NULL” text in the column so I removed it by unchecking it from the list of other department rows. Which gives our rows to reduce to 987 rows
#### Before column 
![image](https://github.com/user-attachments/assets/6ff5ac48-f4cc-473c-b8c4-7c13ad3cc83c)

#### After column 
![image](https://github.com/user-attachments/assets/48b3b8ea-59d8-46c4-b79a-948c3b73605b)

Salary Column
There are few rows that has a “null” text in the column so I removed it by unchecking it from the list of other salary rows. Which gives our rows to reduce to 946 rows 
#### Before Column 
![image](https://github.com/user-attachments/assets/c64ad470-def2-4c8e-8f39-c97b199e3e87)

#### After Column 
![image](https://github.com/user-attachments/assets/b71a2e12-647c-4a8c-933e-7c4f5c711110)


Merge table
I created a merge table to be able to get the employee who’s worthy of a bonus base on their performance rating so I was able to merge the Palmoria Group_emp_data and the bonus rules table together. I merged them by joining their unique identifier which is the “Department” column so that gives me the bonus discount column ![image](https://github.com/user-attachments/assets/3cde99df-f596-48a3-9c26-3e6a004a019c)
 

Modelling
Automatically derieved relaionships are adjusted to remove and replace unwanted relationships with the required.
Auto model Adjusted model. The model is a star schema There are 2-dimensional tables and 1 fact table. The dimension tables are all joined to the fact table (auto-detect) with a one-to-many relationships but after i merged the DSF_emp_data to the bonus rules table i adjusted the model which gives a many-to-many relationships.

### Conclusions
#### Gender Distribution 
• The gender disparity is most prominent in the Kaduna region (M-F ratio: 182–165), followed by Lagos (M-F ratio: 124–118) and then Abuja which has a negligible gender disparity (M-F ratio: 159–158). • Of the 12 departments, 7 have a higher Male headcount, with the Legal department leading the pack (M-F ratio: 49–34). • Overall, the gender disparity across the company is considered  ‘MARGINAL’.

#### Salary Structure
• A gender pay gap exists across all regions of the company; at an average M-F salary ratio of $74.8k — $72.1k, male employees were noted to earn slightly more in all regions. • Male employees earned more in total terms across 7 (out of 12) departments. On an average salary basis, Male employees earned more in 9 (out of 12) departments across the company. • Given the marginal pay gap, there isn’t sufficient evidence based on available data to conclude if the disparity is reflective of patriarchy. • Performance Ratings & Bonuses • Female employees overall performed better in the period under review (reflected in higher overall bonuses which accrued to females).

### Recommmendations
• Given the minimality of the gender disparity & pay gap, PALMORIA should consider reviewing its employment and remuneration policy to close the inherent gender gaps and neutralize current negative opinions. • PALMORIA should consider reviewing the salary structure across the company to meet the minimum wage requirement

#### Learning Outcome

•	Gained experience with real-world power BI data analysis

•	Improved storytelling with dashboards

•	Learned to uncover actionable insights using data















