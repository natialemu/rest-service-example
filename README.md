## Overview

This project includes two web services. The first service, under com.client.company.hr, consumes a second web service,
under com.comany.hr

Both web services are spring-boot based REST services, and both use
maven for managing dependencies(see pom.xml for details)


## Tools/Frameworks
 - swagger-ui: for visualizing your APIs
 - Feign: for sending client requests
 - Tomcat as an embedded web server


## Running the services

Before you can run the services, make sure you have the following pre-requisites:
   - Java 11 is installed and correctly configured into your IDE
   - mvn is installed
   - IntelliJ(preferred not required)

To build the project via the command line, execute `mvn clean install` under
the root project directories.

To run the server, right click on `com.company.hr.Application` and click on 'Run'. you can also run it via the command line
using this command `mvn spring-boot:run`

Before running the client application, make sure the server application is running. 
Once the server is succesfully running, you can run the client application 
`com.client.company.hr.ClientApplication` by using the following mvn command
`mvn spring-boot:run -Dspring.profiles.active=client`
Alternatively, in InteliJ, you can run the client application via the following
steps:

    1. Run" -> "Edit Configurations", then add '-Dspring.profiles.active=client'
        as a VM Option for the ClientApplication.
    2. Right click on ClientApplication, then click on 'Run'.
