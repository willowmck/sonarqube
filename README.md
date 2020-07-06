# SonarQube Image 

This is a SonarQube image forked from the work done by Red Hat Open Innovation Labs for OpenShift:

https://github.com/rht-labs/labs-ci-cd

This repo installs SonarQube 7.7 Community edition.  There are two options for installing:
* ephemeral SonarQube
* SonarQube backed by persistence layer with PostgreSql.

## Steps to Deploy
First, create the OpenShift project to deploy SonarQube. 

`oc new-project sonar`

Second, deploy SonarQube.  

To deploy the ephemeral SonarQube, execute the following:

`oc new-app -f sonarqube-template.yml`

To deploy SonarQube backed by Postgres, execute:

`oc new-app -f sonarqube-persistent-template.yml`

In either case SonarQube will deploy with default credentials setup.  You should look at SonarQube's community documentation for further configuration and setup.  

https://docs.sonarqube.org/7.7

