# Afiesere project Progress Dashboard

[Dashboard](blobs/Capture.PNG)
## A Brief Introduction
This project was designed to monitor and manage progress in the execution of the Afiesere 
Facility Information Management (FIM) project for **Heritage Energy Operations Services Limited (HEOSL)**. 
The project incorporates a reporting template and a Dashboard. In the reporting template, 
all team members involved mainly in the 3d modeling phase of the FIM project can log in their daily progress and activities and also comment on particular issues. While, the dashboard gives a summary of important development as they happen from time to time. Therefore, ensuring that progress can be monitored as they occur and can be attended to.

## Data Gathering/ Reporting
The reporting template is designed such that it will be easy to use and will require minimal effort on the part of the user. This was achieved by employing data validation where necessary, to govern user input and ensure uniformity. Also, excel formula and VBA Scripting was heavily leveraged to timestamp and log activities. This ensures that several data are inferred when the user starts a task, finishes a task, or records the level of progress achieved per time.

However, team leads have the responsibility to assign tasks to owners before the project begins and also assign the number of hours required for each assigned task.

## Some Excel formulas used 

#### Start time

> Timestamp of when a user select "InProgress" from the Status column
[starttime](blobs/start_date_snip.PNG)


#### End Time

> Timestamp of when a user select "Complete" from the Status column
[endtime](blobs/enddate_snip.PNG)

#### Time Taken
> Calculated from the difference between start time and end time putting into consideration, 8 hours workday from 8:00am to 4:00am, weekends and holidays
[time_taken](blobs/time_taken_snip.PNG)


#### Estimated End date

> Calculated from the start date and estimated time to finish information. This will also inform due task and escalate them on the dashboard
[Estimated_Enddate](blobs/Estimated_Enddate.PNG)




#### Due tasks

> Calculated using an array formula that logically test for due tasks on the main reporting template sheet and logs them in a different table on a "Due_tasks" sheet. This will help to easily see due tasks and reach alignment on mitigating further risk to project timeline. 
[Due_tasks](blobs/Due_tasks.PNG)


#### project log and VBA_Code

> A VBA code taking advantage of the worksheet change event object in the workshet was used to timestamp changes per time on an activity and also to log important information about the tasks InProgress and Completed. and also to show the cummulative addition of man hours to the project per time.
[VBA_Snip](blobs/VBA_Snip.PNG)

[Project_Log](blobs/Project_Log.PNG)


## Limitation
The project can be used to track  and manage intra-departmental tasks and activities, but further data engineering activities will be required in collecting this data and storing it in a proper database in order to provide more long-term insights into team performance from project to project.
