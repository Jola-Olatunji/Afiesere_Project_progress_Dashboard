# Afiesere project Progress Dashboard
![Dashboard](https://github.com/Jola-Olatunji/Afiesere_Project_progress_Dashboard/tree/master/blobs/Capture.png)
## A Brief Introduction
This project was designed to monitor and manage progress in the execution of the Afiesere 
facility Information Management (FIM) project for **Heritage Energy Operations Services Limited**. 
The project incorporates a reporting template and a Dashboard. In the reporting templating, 
all team members involved particularly in the 3d modelling phase of the FIM project can log in their daily progress and activities and also comment on particular issues. While, the dashboard gives a summary of important development as they happen from time to time. Therefore, ensuring that progress can be monitored as they occur and can be attended to.

## Data Gathering/ Reporting
The reporting template is designed such that it will be easy to use and will require minimal effort on the part of the user. This was achieved by employing data validation where necessary, to govern user input and ensure uniformity. Also excel formula and VBA Scripting was heavily leveraged to timestamp and log activities. This ensures that several data are infered when the user start a task, finish a task, or record the level of progress achieved per time.

However, team leads have the responsibility to assign task to owners before the project begin and also assign the number of hours required for each assigned task.

## Some excel formula used 

#### Start time
> Timestamp of when a user select "InProgress" from the Status column
![starttime](https://github.com/Jola-Olatunji/Afiesere_Project_progress_Dashboard/tree/master/blobs/start_date_snip.png)


#### End Time
> Timestamp of when a user select "Complete" from the Status column
![endtime](https://github.com/Jola-Olatunji/Afiesere_Project_progress_Dashboard/tree/master/blobs/enddate_snip.png)


#### Time Taken
> Calculated from the difference between start time and end time putting into consideration, 8 hours workday from 8:00am to 4:00am, weekends and holidays
![time_taken_snip](https://github.com/Jola-Olatunji/Afiesere_Project_progress_Dashboard/tree/master/blobs/time_taken_snip.png)


#### Estimated End date
> Calculated from the start date and estimated time to finish information. This will also inform due task and escalate them on the dashboard
![Estimated_Enddate](https://github.com/Jola-Olatunji/Afiesere_Project_progress_Dashboard/tree/master/blobs/Estimated_Enddate.png)



#### Due tasks
> Calculated using an array formula that logically test for due tasks on the main reporting template sheet and logs them in a different table on a "Due_tasks" sheet. This will help to easily see due tasks and reach alignment on mitigating further risk to project timeline. 
![Due_tasks](https://github.com/Jola-Olatunji/Afiesere_Project_progress_Dashboard/tree/master/blobs/Due_tasks.png)


#### project log and VBA_Code
> A VBA code taking advantage of the worksheet change event object in the workshet was used to timestamp changes per time on an activity and also to log important information about the tasks InProgress and Completed. and also to show the cummulative addition of man hours to the project per time.
![VBA_Snip](https://github.com/Jola-Olatunji/Afiesere_Project_progress_Dashboard/tree/master/blobs/VBA_Snip.png)

![Project_Log](https://github.com/Jola-Olatunji/Afiesere_Project_progress_Dashboard/tree/master/blobs/Project_Log.png)


## Limitation
The project can be used to track  and manage intra departmental tasks and activities, but further data engineering activities will be required in collecting this data and storing it in a proper database in order to provide more long term insights into team performance from project to project.
