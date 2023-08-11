# Afiesere project Progress Dashboard
![Dashboard](https://drive.google.com/file/d/1e8jmZ2W3i9-I1Jzi2SCxRh7E9W3KgvI0/view?usp=sharing)
## A Brief Introduction
This project was designed to monitor and manage progress in the execution of the Afiesere 
Facility Information Management (FIM) project for **Heritage Energy Operations Services Limited (HEOSL)**. 
The project incorporates a reporting template and a Dashboard. In the reporting templating, 
all team members involved mainly in the 3d modeling phase of the FIM project can log in their daily progress and activities and also comment on particular issues. While, the dashboard gives a summary of important development as they happen from time to time. Therefore, ensuring that progress can be monitored as they occur and can be attended to.

## Data Gathering/ Reporting
The reporting template is designed such that it will be easy to use and will require minimal effort on the part of the user. This was achieved by employing data validation where necessary, to govern user input and ensure uniformity. Also, excel formula and VBA Scripting was heavily leveraged to timestamp and log activities. This ensures that several data are inferred when the user starts a task, finishes a task, or records the level of progress achieved per time.

However, team leads have the responsibility to assign tasks to owners before the project begins and also assign the number of hours required for each assigned task.

## Some Excel formulas used 

#### Start time
> Timestamp of when a user selects "InProgress" from the Status column
![starttime](https://drive.google.com/file/d/18WKNYMkYykGuEz-Qj89AbqjghqVOyYGq/view?usp=sharing)


#### End Time
> Timestamp of when a user selects "Complete" from the Status column
![endtime](https://drive.google.com/file/d/1CRclTEBuNKOPxNy-LAICad0Cg4uvPcNy/view?usp=sharing)


#### Time Taken
> Calculated from the difference between start time and end time putting into consideration, 8 hours workday from 8:00am to 4:00am, weekends and holidays
![time_taken_snip](https://drive.google.com/file/d/1-dNjJM2YlMNHKmrVbZ7aH5h0OXxdFXNY/view?usp=drive_link)


#### Estimated End date
> Calculated from the start date and estimated time to finish information. This will also inform due tasks and escalate them on the dashboard
![Estimated_Enddate](https://drive.google.com/file/d/1IwcDdU4KmizBMLb0DZusjuMnskeUV4Bt/view?usp=sharing)



#### Due tasks
> Calculated using an array formula that logically tests for due tasks on the main reporting template sheet and logs them in a different table on a "Due_tasks" sheet. This will help to easily see due tasks and reach alignment on mitigating further risk to the project timeline. 
![Due_tasks](https://drive.google.com/file/d/1WRFeyWR6QI8i4YXnR6alis-hDvql4CnP/view?usp=sharing)


#### project log and VBA_Code
> A VBA code taking advantage of the worksheet change event object in the worksheet was used to timestamp changes per time on an activity and also to log important information about the tasks InProgress and Completed. and also to show the cumulative addition of man hours to the project per time.
![VBA_Snip](https://drive.google.com/file/d/1-siV7LIYzG12HqsuiyHogCr--qozF9oT/view?usp=drive_link)

![Project_Log](https://drive.google.com/file/d/1o0L8Y3TnwwZ9f24Gkmf1043eb7gz-J4B/view?usp=sharing)


## Limitation
The project can be used to track  and manage intra-departmental tasks and activities, but further data engineering activities will be required in collecting this data and storing it in a proper database in order to provide more long-term insights into team performance from project to project.
