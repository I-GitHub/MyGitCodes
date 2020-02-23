# Service Monitor




# Background:

Window services plays a critical to get the processes completed successfully in real environment. Sometimes, we comes across a situation where we need to ensure that these services on a given server needs to be monitored either manually or through some mechanism which ensure that if there is an issue reported with the service should be timely notified and actioned immediately. Doing this manually would be a difficult excercise which even involves risk due to manual intervention and efforts in term of costs etc.

Automation will prove beneficial in mitigating the risk due to manual monitoring and this can be done through Powershell. Powershell is a built in utility that comes with Windows and lets the users to create the script.


# Introduction:

This powershell script is used to track status of window service on a given server whether it is running or not. And if the service is not up, this will let the recipients/audience know about it to take a corrective action.

Special feature of this script is that it also tries to bring the server up implcitly if the service is found to be stopped state. Also, this follows with mail notifications depending on outcome to intended audience/recipients whether retry attempt has succeeded or failed.

# Benefits:

Key advantage of this script are:
1. Implcit attempt to start a service is an important feature here.
2. Keeps track of a window service on a given server.
3. Can be easily customized as per need.
4. Email notification to intended audience/teams to take corrective action.


# Prerequistes:

Following parameters in the script needs to be passed as required to make the script running:

A.	MAILSERVER		:	This needs to be replace with the smtp mail server details (like NAME/IP etc.) to deliver mail.
  
B. 	SERVICENAME   :	This needs to be replace with the actual service name which needs to be monitored.
  
C. 	From, To, Cc	:	Here correct email needs to be provided in the SEND-MAILMESSAGE function.



# Deployment process:

ServiceMonitor.ps1 script can be scheduled in task scheduler  by creating a new job in it.  Reference path of this script needs to be passed so that it can be triggered by the job.




