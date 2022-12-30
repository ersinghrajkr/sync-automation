# Otalio sync-automation

JMeter scripts for Synchronization, Resync and Resend Automation.

#Generation from an existing sample CSV log file and Make sure you are running/opening cmd, whereever your JMX scripts exist
jmeter -g D:\Automation\JMeter\JMeter-5.4.1\bin\jmeter.log -o D:\Apps\#SDET\AppDevelopment\sync-automation\report-output

#Generation after load test
jmeter -n -t TestPlan-LearnJMeter04ListenerExample.jmx -l D:\Apps\#SDET\AppDevelopment\sync-automation\logs-output\jmeter.log -e -o D:\Apps\#SDET\AppDevelopment\sync-automation\report-output

#Generation using GUI Tools menu
You can generate the HTML report using menu item Tools → Generate HTML report:
For each parameters see the following table :

Parameters
Attribute 				Description 													Required
Results file (csv or jtl) 	The CSV output of a tes run 										Yes
user.properties file 		The user.properties file used to run the load test 						Yes
Output directory 		The directory where you want the report to be created(must be empty) 	No

If no output directory is defined, the controller will use ${JMETER_HOME}/bin/report-output.
You then only have to click on the Generate report button and wait for an information dialog to appear
If report generation takes more than two minutes, adjust the property generate_report_ui.generation_timeout
