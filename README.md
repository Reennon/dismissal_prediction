[[_TOC_]]

# Description

## Introduction
People turnover numbers were always important for any organization, especially in the case of their continued growth – the more the organization is growing the more these numbers become critical. Therefore, it is more significant now than ever to make sure that the number of volontary dismissals is very low. As this would lead to huge savings
related to the cost per hire, including advertising, recruiting, training, internship expenses, and variance in salary between hired
and dismissed employees. Obviously, the most cost-efficient and effective approach overall is to manage unwanted dismissals by preventing them in a timely manner before a person makes the final decision to leave the company.

We propose to participate in the competition on best solution in the area of HR Analytics and try to develop the predictive model, which provides the assessment of the Employees Dismissal Risk, based on the historical data analysis.  


## Problem Description
The major goal of the competition - develop a model, which provides an answer to the question - <b>"Will the particular Employee leave the Company within the next three month?" </b>

Solution should be made with respect of the following business goals:

1.  Managers should have a notification about Employees even in case of insignificant risk of Dismissal
2.  Managers should get an information regarding Dismissal drivers - the interpretability of the prediction result is desirable
3.  Managers should get the recommendations regarding potential actions for Employees retention.


Point 1 is mandatory for this competition, points 2-3 are optional and will be assessed independently.


## Expected results

With respect of business needs, the following outcomes are expected:

1. Assignment of binary label to each employee (0 - Not At Risk, 1 - At Risk), for the next three month after observed period
2. Analysis of the historical data and modelling results in order to define the factors that have the most significant impact to the Employees Turnover. Reasoning and conclusions should be represented in view of report. 
3. Sensitivity (what-if) analysis approach description with respect of data insights and modelling results 

### Results Assessment 

* Task 1 will be assessed formally via callucaling success score, which reflect the accuracy of the solution with taking into account business criteria.
* Tasks 3-4 will be assessed for 15 teams who will show high results for the main task and are considered as separate nomination

### Tricky Moment

Please, pay attantion that we do not provide target variable, but have already generated it for your results validation. So, it's critically important to provide correct binary flag to each employee in dataset with respect of his historical data for submission. 
For instance if some Employee left the Company in Oct 2017, the target flag for him should be represented as:

| Employee ID | Date | target |  
|-----------|:-----------:|-----------:|  
| 1 | 2017/04 | 0 |  
| 1 | 2017/05 | 0 |
| 1 | 2017/06 | 0 |
| 1 | 2017/07 | 1 |
| 1 | 2017/08 | 1 |
| 1 | 2017/09 | 1 |

The record for the last month (2017/10) is absend due to the reason that employee left company in this month doesn't have a target for the next period.

-----------

# Evaluation

## Main Nomination

###  Employees "At Risk" assessment - binary classification problem (the first task)

Results assessment via Kaggle Platform.
Submissions are evaluated on <b>f-beta score</b> (beta is equal to 1.7) between the predicted value and the observed target for the next three month out of the provided DataSet, which takes two values:

*  0 - Employee is not At Risk
*  1 - Employee is At the Risk

![f-beta score](./f-beta.png =300x)


## Additional Nomination
###  1. Dismissal Drivers Analysis (second task)

Submissions will be scored using the following:

* Approach Explanation
  * Did the participant explain their approach to the Dismissal Drivers detection?
  * Did the participant highlight the pros and cons of their approach?
* Approach Demonstration
  * Did the participant provide code (Python / R / Jupyter Notebook) with the demonstration (implementation) of the described Dismissal Drivers detection for particular employee or in general
* Documentation
  * Is the proposed approach well documented?
  * Is the code easy to read and reuse?

###  2. WHAT-IF Analysis (third task)

Submissions will be scored using the following:

* Approach Explanation
  * Did the participant explain their approach to the Actions Recommendations (what Managers should do in order to prevent Employee dismissal)?
  * Did the participant highlight the pros and cons of their approach?
* Approach Demonstration
  * Did the participant provide code (Python / R / Jupyter Notebook) with WHAT-IF analysis approach demonstration (implementation) with respect of particular employee 
* Documentation
  * Is the proposed approach well documented?
  * Is the code easy to read and reuse?

-----------

# Submission File

## 1. Employees "At Risk" assessment - binary classification problem (first task)

Submission files (csv format) should contain two columns: *EmployeeId* and *target*. For each EmployeeId in the test set, you must predict 1 if the employee will leave the company in the next 3 months, and 0 otherwise.

The file should contain a header and have the following format:

```
EmployeeId,target
1,1
3,1
5,0
7,1
```

Winner of main nomination should send the the final model’s software code as used to generate the winning Submission and associated documentation. 
All assessments should meet the competitions rules.

All artefacts should be sent via email (with will be provided later).

##  2. Dismissal Drivers Analysis (second task)

Submission for the third task should contain a report with the description of the proposed approach in pdf format and Reproducible code with comments if provided.
All artefacts should be sent via email (with will be provided later).

##  3. WHAT-IF Analysis (third task)

Submission for fourth task should contain a report with the description of the proposed approach in pdf format and Reproducible code with comments if provided.
All artefacts should be sent via email (with will be provided later).

-----------

# Data Description

We are providing anonymized dataset, which was generated based on real distributions, extracted from historical Employees data.

<b><span style="font-size:1.2em"> Employee History</b></span>

Employee History data for 1.5 years, which is gathered on regular basis (ones per month)
* EmployeeID - Employee identifier
* Date - Month of Employee Statistics gathering
* DevCenterID - Employee Location in terms of Company Geography
* SBUID - Employee Location in terms of Company Structure
* PositionID - Identifier of Employee Position (like QC Engineer, Development Consultant, etc)
* IsTrainee - Trainee flag of Employee
* LanguageLevelID - English Level Identifier (like Intermediate low, Upper-intermediate, etc)
* CustomerID - Client Identifier (one client may be related to the several projects)
* ProjectID - Employee Main Project Identifier
* IsInternalProject - Internal / External project flag
* Utilization - percent of Employee load on Non-Internal Projects during last month
* HourVacation - vacation hours are spent as on the last month
* HourMobileReserve - total hours in Mobile reserve as on the last month 
* HourLockedReserve - total hours in Locked reserve as on the last month 
* OnSide - was Employee involved to OnSite visit last month
* MonthOnPosition - month without position changing as on the last month 
* MonthOnSalary - month without salary increasing as on the last month 
* CompetenceGroupID - Employee Competency Group (like QC, Big Data,  Data Science, etc)
* FunctionalOfficeID - Functional Office Identifier (like SDO, QMO, etc)
* PaymentTypeId - Payment with respect to the country-specifics employment
* WageGross - Compensation GROSS
* BonusOneTime - One Time Bonus
* APM - Employee APM
* PositionLevel - Employee Seniority Level (Junior, Middle, Senior, etc)

<b><span style="font-size:1.2em"> Employee</b></span>

Information about Employee employment

* EmployeeID - Employee identifier
* HiringDate - Date of Hiring
* DismissalDate - Date of Dismissal

-----------

# Timelines

Competition for the Fist Nominion (Dismissal Risk Score Assessemnt) starts 12/05/2020 and ends 17/05/2020. 
Any assignments after 17/05/2020 will not be accepted.

Submition for the second nomination (Dismissal Risk Drivers / WHAT-IF analysis) are accepted via email till 20/05/2020.

-----------

# Competition Rules

COMPETITION TITLE: SoftServe DS Hackathon 2020 
COMPETITION SPONSOR: SoftServe, inc 
COMPETITION WEBSITE: https://www.kaggle.com/c/softserve-ds-hackathon-2020/

## PRIZES
Main Nomination Prize: 
Additional Nomination Prize:  

ENTRY IN THIS COMPETITION CONSTITUTES YOUR ACCEPTANCE OF THESE OFFICIAL COMPETITION RULES.

The Competition named above is a skills-based competition to promote and further the field of data science. You must register via the Competition Website to enter. Your competition submissions (“Submissions”) must conform to the requirements set forth on the Competition Website. The Competition Sponsor will score your Submissions based on the evaluation metric described on the Competition Website. 

## SPECIFIC COMPETITION RULES
In addition to the provisions of the General Competition Rules below, you understand and agree to these Specific Competition Rules required by the Competition Sponsor:
* Team Limits: Up to three members.
* Submission Limits: You may submit a maximum of 5 entries per day.
* Final Judging: You may select up to 2 final kernels for judging against the final test set.
* Winner's License: Non-Exclusive: You will grant to Competition Sponsor and its designees a worldwide, non-exclusive, sub-licensable, transferable, fully paid-up, royalty-free, perpetual, irrevocable right to use, reproduce, distribute, create derivative works of, publicly perform, publicly display, digitally perform, make, have made, sell, offer for sale and import your winning Submission and the source code used to generate the Submission, in any media now known or hereafter developed, for any purpose whatsoever, commercial or otherwise, without further approval by or payment to Participant. 
* Allowed Programming languages: Python / R

## GENERAL COMPETITION RULES
### BINDING AGREEMENT:

In order to enter the Competition, you must agree to these Official Competition Rules, which incorporate by reference the provisions and content of the Competition Website and any Specific Competition Rules above (collectively, the “Rules”). Please read these Rules carefully prior to entry to ensure you understand and agree. You agree that submission of an entry in the Competition constitutes agreement to these Rules. You may not submit an entry to the Competition and are not eligible to receive the prizes described in these Rules unless you agree to these Rules. These Rules form a binding legal agreement between you and the Competition Sponsor with respect to the Competition.
### COMPETITION PERIOD:

The Competition will run from the Start Date and time to the End Date and time, as set forth on the Competition Website. The Competition Period and Submission deadlines are subject to change, and Competition Sponsor may introduce additional hurdle deadlines during the Competition. Any updated or additional deadlines will be publicized on the Competition Website. It is your responsibility to check the Competition Website regularly to stay informed of any deadline changes. YOU ARE RESPONSIBLE FOR DETERMINING THE CORRESPONDING TIME ZONE IN YOUR LOCATION.
### INDIVIDUALS AND TEAMS:

1. Individual Account. You may make Submissions only under one, unique Kaggle.com account. You will be disqualified if you make Submissions through more than one Kaggle account, or attempt to falsify an account to act as your proxy. You may submit up to the maximum number of Submissions per day as specified on the Competition Website.
2. Teams. If permitted under the Competition Website guidelines, multiple individuals may collaborate as a team (a “Team”); however, you may join or form only one Team. Each Team member must be a single individual with a separate Kaggle account. You must register individually for the Competition before joining a Team. You must confirm your Team membership to make it official by responding to the Team notification message sent to your Kaggle account. Team membership may not exceed the Maximum Team Size set forth on the Competition Website.

### COMPETITION DATA:

“Competition Data” means the data or datasets available from the Competition Website for the purpose of use in the Competition, including any prototype or executable code provided on the Competition Website. 
1. Data Access and Use. Unless otherwise restricted under the Competition Specific Rules above, after your acceptance of these Rules, you may access and use the Competition Data for the purposes of the Competition, participation on Kaggle Website forums, academic research and education, and other non-commercial purposes. 
2. Data Security. You agree to use reasonable and suitable measures to prevent persons who have not formally agreed to these Rules from gaining access to the Competition Data. You agree not to transmit, duplicate, publish, redistribute or otherwise provide or make available the Data to any party not participating in the Competition. You agree to notify Kaggle immediately upon learning of any possible unauthorized transmission or unauthorized access of the Data and agree to work with Kaggle to rectify any unauthorized transmission. You agree that participation in the Competition shall not be construed as having or being granted a license (expressly, by implication, estoppel, or otherwise) under, or any right of ownership in, any of the Data. 
3. External Data. Unless otherwise expressly stated on the Competition Website, you may not use data other than the Competition Data to develop and test your models and Submissions. Competition Sponsor reserves the right in its sole discretion to disqualify any Participant who Competition Sponsor discovers has undertaken or attempted to undertake the use of data other than the Competition Data, or who uses the Competition Data other than as permitted by the Competition Website and these Rules.
### SUBMISSION CODE REQUIREMENTS:
1. Private Code Sharing. Unless otherwise specifically permitted under the Competition Website or Competition Specific Rules above, during the Competition, you are not allowed to privately share source or executable code developed in connection with or based upon the Competition Data. This prohibition includes code sharing between separate Teams, unless a Team merger occurs. Any such code sharing is a breach of these Competition Rules and may result in disqualification.
2. Public Code Sharing. You are permitted to publicly share source or executable code developed in connection with or based upon the Competition Data, or otherwise relevant to the Competition, provided that such public sharing does not violate the intellectual property rights of any third party. By so sharing, you are deemed to have licensed the shared code.
3. Use of Open Source. Unless otherwise set forth in the Specific Competition Rules above, if Open Source code is used in the model to general the Submission, then you must only use Open Source code licensed under an Open Source Initiative-approved license (see www.opensource.org>) that in no event limits commercial use of such code or model containing or depending on such code and inform the use to The Competition Sponsor upon submission.

### DETERMINING WINNERS:

Each Submission will be scored and ranked by the evaluation metric set forth on the Competition Website. During the Competition, the current ranking will be visible on the Competition Website’s leaderboard. Final results are determined solely by the leaderboard ranking on the private leaderboard as set forth on the Competition Website, subject to compliance with these Rules. 
Team with the highest score will get the First Nomination Award. 
Moreover, top 15 teams, including the First Nomination winner, will be allowed to continue the competition for the Second Nomination. 
The winner of second nomination is determined by Competition Sponsor with respect of formulated acceptance criteria.
The winner’s list will be publicly displayed at Kaggle.com. Determinations of Competition Sponsor are final and binding.

### WINNERS OBLIGATIONS:

As a condition to being awarded a Prize, a Prize winner candidate must deliver to the Competition Sponsor the final model’s software code as used to generate the winning Submission and associated documentation. 
The delivered software code must be capable of generating the winning Submission and contain a description of resources required to build and/or run the executable code successfully.
Code should be well described, accompanied with requirements file and launch instruction. Code should be provided as zip archive.
 

