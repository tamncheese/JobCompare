V2 - updated to include additional functionality

# User Manual for JobCompare6300

## 1. Application Summary
The JobCompare6300 app is a mobile android application created to compare job applications according to a single user's needs. This app is intended to compare across several factors, including salary, bonus, location, cost of living, and other benefits. 

## 2. Getting Started
To get started, simply run the android application JobCompare6300, which will take you to the main menu screen.


## 3. Using the application
After launching the application, there are 4 buttons to reflect theactivities to perform. First includes uploading for editing the information of the user's current job. The third is to add additional job offers to be compared. The third, is to adjust the settings of the comparison. The fourth will be to perform the job comparisons and select the jobs to compare. 

When initially using the app, there will need to be jobs. In order to create a job, the user should select the "create job details" button. Here, the user will be taken to a new screen with the option to enter new job details. These job details contain:
* Title
* Company
* Location
* Cost of living in the location (as an index)
* Yearly salary
* Yearly bonus
* Leave (number of  days from 0 to 30 inclusive)
* Maternity/Paternity Leave (number of days from 0 to 20 inclusive)
* Life Insurance (Percentage of Salary, in whole numbers)

Its important to hit "save" to successfully save the information. Otherwise the data will be lost. 
If the user selects a job that is already present, the above information is presented.

When the user selects to create a new Job Offer, or option 2, the user will be able to add the same informaiton as the current job. There will also be the functionality to directly compare this job with the current offer. Selecting this button will trigger a comparison and take you to that screen. 


When selected the button for option 3, to adjust the comparison settings, the user will be taken to a new screen where the user can enter integer weights to the below criteria, expressing the importance placed on the factor. The possible intries are:

* Title
* Company
* Location 
* Yearly salary adjusted for cost of living
* Yearly bonus adjusted for cost of living
* Leave
* Maternity/Paternity Leave 
* Life Insurance 

Once several jobs have been entered, the jobs will be sorted according to their "job score", highest to lowest, which is calulated based on their weights in the below formula:


AYS + AYB + (LT * AYS / 260) + (MPL * AYS / 260) + (LI/100 * AYS)

where:
AYS = yearly salary adjusted for cost of living
AYB = yearly bonus adjusted for cost of living
LT = Leave
MPL = Maternity/Paternity Leave
LI = Life Insurance

The final button allows the user to select only two job offers to compare against each other. the user will know whether a job been selected by the checkbox to the right of the job offer. Once the user selects to Job Offers (or one with their current job) they can click the Compare button to be taken the results screen. 

On the results screen, the user will be able to review the relevant information of the jobs to make a wise decision. When the user is done, they have the option of performing a new comparison or returning to the home screen. 

## 4. Error Handling
If there are any errors, closing and re-opening the app will clear the memory and start fresh. 

## 5.  Notes
The data is saved to a csv file on the machine. Closing and reopening the app will not have any affect on the data. 