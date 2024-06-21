# sonarQube

It is a code review tool. To check whether our application code is maintaining all the standards or not. Instead of going through the code manually we are using some tools rather going line by line manually,
Ex: code reviews tools are sonarQube, VeraCode

SonarQube is popular because it is free and no license needed for most of the tools. using we are doing the static code analysis

### code coverage: How many lines of code is tested by the unit test cases, developers write unit test cases

Java --> Junit test cases, pythin --> PyTest, C --> CUnit

***80% of the code has to be tested by the unit test cases, ths is the standard for the code checking unit test cases***

### static code analysis:

## use of databases in sonarqube server
It is used to generate report if we have anything in the statemnt format, so to store the report we are suing the databases.

## lets says there is not databases attached to the sonarqube server, then where the sonar saves the generated reports
Database attachment is not manditory for the sonarqube, basically it has an inbuilt database called the ***H2 database*** 

## prerequists of the sonarqube
java, 
4 gb ram

## architecture of the sonarQube 
1. scanner: Takes the code from repository and scans the applciation code and sends the report to the sonarQube server
2. sonarQube server: we have a ***compute engine*** inside the sonarQube server, it classifies the report to the 3 categories tehy are ***vulnarabilities, code smells, bugs***
3. After categorizing it stores into the internal or external database
4. To access the report we use ***one webserver*** we have search option in the dashboard of sonar to get the search results quickly.
![image](https://github.com/bhargavsp/sonarQube/assets/45779321/55e71c83-6ad2-4d59-a560-6438709d6625)


## Installing/configuring the sonar
Refer to https://mithuntechnologies-devops.blogspot.com/search/label/SonarQube%20Server <br/>
Refer to this link also https://devopscube.com/setup-and-configure-sonarqube-on-linux/
|command|usage|
|:---:|:---:|
Install java from amazon linux website | 
installing sonarQube | 
