



## EMERGENCY ROOM DASHBOARD


## Problem Statement

This dashboard provides hospitals with insights into emergency room operations, helping them understand patient trends and optimize care delivery. It highlights areas such as patient satisfaction, wait times, demographics, and referral patterns. These insights assist in resource allocation, improving patient flow, and addressing operational inefficiencies.

### Key Observations:

- Patient Satisfaction: 
        
        Moderate satisfaction levels with an average score of 4.99/10, indicating room for improvement in service delivery.

- Average Wait Time:  

        35.2 minutes, necessitating measures to reduce delays in patient processing.

- Admission Patterns: 

       A nearly equal split between admitted and non-admitted patients (49.97% and 50.03%, respectively).


###  Dashboard Views
### 1. Monthly View
The Monthly View provides a detailed snapshot of emergency room performance on a month-by-month basis, allowing users to identify trends and anomalies over time.

- Metrics Included:

        Number of patients treated, Average wait time per month,Monthly patient satisfaction scores, Admission rates split by admitted and not admitted.

- Visualizations:
      
      Line charts for time-based trends, Bar charts to compare admission rates and patient demographics.

![Image](https://github.com/user-attachments/assets/ff2ca406-ea8c-4571-854d-6965dd702f1b)



### 2. Consolidated View
This view offers a high-level summary of all data for the 24-month period, enabling quick insights into overall performance.

- Metrics Included:
      
      Total number of patients,
      Overall averages for wait time and satisfaction scores,
      Percentages of patients seen within the target time.

- Visualizations:
      
      Summary cards for key metrics,
      Pie charts for gender and race distributions,
      Bar charts for department referrals and age group segmentation.

![Image](https://github.com/user-attachments/assets/84f4d9be-0205-4966-9d67-5bab7ad49f22)


### 3. Patient Details View
The Patient Details View drills down into individual patient records, making it easy to identify patterns or investigate specific cases.

- Fields Displayed:
       
       Patient demographics (age, gender, and race),
       Admission status and referral department,
       Wait times for each patient.

- Use Cases:
      
      Investigating outliers or specific complaints,
      Analyzing referral trends and demographic details.

![Image](https://github.com/user-attachments/assets/5b2a7b0c-303c-41cc-8542-feb20c2f13c9)

### Key Takeaways View:

This view provides actionable insights and recommendations derived from the data.

- Insights Provided:
     
      High-demand periods (busiest days and hours),
      Areas needing improvement (satisfaction and wait times),
      Departmental trends (most referred departments).

- Purpose:
      
      Serve as a summary for stakeholders to quickly understand key challenges and areas for improvement.

- Visualization:
      Text-based analysis supported by summary visuals.

![Image](https://github.com/user-attachments/assets/20599321-9c69-450e-9ba1-b4597ec74086)



### Steps followed 

### Data Preparation
1. Data Loading : Imported a 24-month emergency room dataset into Power BI.
2. Data Profiling : Conducted data quality checks in Power Query Editor:

       Activated Column Quality, Column Distribution, and Column Profile options.

       Ensured profiling for the entire dataset.
    
       Identified and excluded null values in critical columns like Wait Time.
### Report Design

#### 1. Visualizations:

 - Added slicers for filtering by Age Group, Gender, Race, Referral Department, and Admission Status.
- Used card visuals to display :

        Average wait time ,Patient satisfaction score , Percentage of patients seen within 30 minutes.
- Created bar charts to represent:

         Patient count by age group

         Gender distribution across admitted and non-admitted patients.

         Designed a line chart to track patient volume trends over months.

#### 2. Calculated Columns and Measures:

- Created a calculated column for age group distribution using DAX
        
        Age Group = 
        IF(Patients[Age]<=25, "0-25",
        IF(Patients[Age]<=50, "25-50",
        IF(Patients[Age]<=75, "50-75", "75+")))

- Used measures for:
- Count of Patients:

        Total Patients = COUNT(Patients[ID])

- Percentage of Patients Admitted:

       Admitted Percentage = DIVIDE(COUNTROWS(FILTER(Patients, Patients[Admission Status]="Admitted")), COUNTROWS(Patients)) * 100

#### 3. Styling and Layout:

- Added the hospital logo, name, and tagline using text boxes and image elements.
- Applied a consistent theme for professional aesthetics.

### Insights
#### 1. Patient Demographics
- Age Groups:

      Largest group: 20–29 years (1158 patients).
      Second-largest group: 10–19 years (1151 patients).
- Gender:
      
      Male: 50.94%, Female: 48.81%
- Race Distribution:

      Largest racial group: White (2571 patients).
#### 2. Operational Metrics
- Satisfaction Scores:

      Overall average: 4.99/10.

      Highest-rated services: In-flight Service (3.64/5) and Baggage Handling (3.63/5).

      Lowest-rated service: In-flight Wifi (2.81/5).
- Wait Times:

      Average arrival delay: 35.2 minutes.

      Percentage of patients seen within 30 minutes: 59.19%.
- Peak Times:

      Busiest days: Saturdays and Sundays.

      Busiest hours: 11 AM, 1 PM, and 7 PM.
#### 3. Admission Patterns

       Admitted: 49.97%.

       Not Admitted: 50.03%.
- Most common referral departments:

       General Practice (1840 cases).
       Orthopedics (995 cases).

        
















        


        

 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
