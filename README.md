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
Install java from amazon linux website | https://docs.aws.amazon.com/corretto/latest/corretto-11-ug/amazon-linux-install.html
installing sonarQube | install zip from website, wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.6.1.59531.zip
install wget and unzip | 
mv sonarqube-9.6.1 sonarqube | change the name of sonarqube for further use and simplicity
useradd sonar | add the user as even the sonar uses the Elasticsearch which cant be performed at the linux root level
visudo | give sonar sudoers priviliges enter **`sonar ALL=(ALL) NOPASSWD: ALL`**(case sensitive) below root  ALL=(ALL)
chown -R sonar:sonar /opt/sonarqube/ ***and*** chmod -R 775 /opt/sonarqube/ | change the user, group permissions and the user, group, other level permissions  
cd su - sonar | `-` is manditory as we are logging into the sonar user completely
cd /opt/sonarqube/bin/linux | navigate to the folder
sh sonar.sh start | start the sonar server on linux environment
open port 9000 in AWS SG group |
default system administrator credentials | admin/admin

## when we create an sonar user after installing the sonarqube in the linux server
1. SonarQube starts an Elasticsearch process and the same account that is running SonarQube itself will be used for the Elasticsearch process.
2. Since Elasticsearch cannot be run as root, You must choose some other, non-root account with which to run SonarQube, preferably an account dedicated to the purpose.
3. Elasticsearch is a NoSQL database. That means it stores data in an unstructured way and that you cannot use SQL to query it
4. Elasticsearch provides extensive APIs for performing searches and aggregations on your data set out of the box
5. You want Elasticsearch when you're doing a lot of text search, where traditional RDBMS databases are not performing really well (poor configuration, acts as a black-box, poor performance). Elasticsearch is highly customizable, extendable through plugins. You can build a robust search without much knowledge quite fast.
