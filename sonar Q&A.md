# sonar Q&A

## can we execute the sonar for standalone and the Enterprise web application

## ERRORS
|Error|solution|
|:---:|:---:|
if we are getting error starting sonar or taking time, timeout | delete the temp directory at the root level re-assign the chmod and chown for the sonarQube folder and stop and start the sonar again 
we shouldnt use the RUN_AS_SERVICE in the sonarQube as it is existed in previosu version before 9.6.0.59 later we should use that in production instead follow the below process | process is in link: https://community.sonarsource.com/t/update-to-sonarqube-9-6-0-59041-missing-files/70117/21
