Ask - Answer Portal
====================

[![License](http://img.shields.io/:license-apache-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)

[Spring Boot](http://projects.spring.io/spring-boot/) FullStack App.


## Requirements

For building and running the application you need

- [JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- [Maven 3](https://maven.apache.org)


## Running the application locally

There are several ways to run a Spring Boot application on your local machine. One way is to execute the `main` method in the `dev.muhammad.aapo.AapoApplication.java` class from your IDE.

Alternatively you can use the [Spring Boot Maven plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins-maven-plugin.html) like so:

```shell
mvn spring-boot:run
```

## Deploying the application to OpenShift or AWS


To deploy the sample application to OpenShift you can use the [OpenShift CLI](https://docs.openshift.org/latest/cli_reference/index.html):

```shell
oc new-app codecentric/springboot-maven3-centos~https://github.com/Urodacus/ask-answer-portal
```

This will create:

* An ImageStream called "springboot-maven3-centos"
* An ImageStream called "aapo"
* A BuildConfig called "aapo"
* DeploymentConfig called "aapo"
* Service called "aapo"

If you want to access the app from outside your OpenShift installation, you have to expose the aapo service:

```shell
oc expose aapo --hostname=www.example.com
```

#### To deploy the sample application to AWS or Container

you can check these links :
* [Deploying on AWS Using AWS Elastic Beanstalk](https://aws.amazon.com/blogs/devops/deploying-a-spring-boot-application-on-aws-using-aws-elastic-beanstalk/)
* [Deploying a Spring Boot Application - docs](https://docs.spring.io/spring-boot/docs/current/reference/html/deployment.html)