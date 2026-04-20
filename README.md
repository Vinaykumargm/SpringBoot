# SpringBoot
Spring Boot : A tool used to create a Standalone and production Grade Spring Application.

Need of spring boot when we have Spring : Reduces Boilerplate Code and many pre configurations, and includes embeded tomcat server.
<img width="1885" height="684" alt="Screenshot 2026-04-19 122337" src="https://github.com/user-attachments/assets/066caf30-a6df-4c36-90de-099a94e225ae" />

<img width="1696" height="779" alt="Screenshot 2026-04-17 163445" src="https://github.com/user-attachments/assets/cef9e00c-c737-435a-b7de-6f2247a8685d" />

<img width="1905" height="756" alt="Screenshot 2026-04-17 163642" src="https://github.com/user-attachments/assets/b8cbdb36-2b31-46e9-8a1c-e5f926d55fca" />

<img width="1858" height="557" alt="Screenshot 2026-04-19 122810" src="https://github.com/user-attachments/assets/26f0afed-d55a-4a4d-98b1-efc8973a762d" />

<img width="1775" height="770" alt="Screenshot 2026-04-19 122904" src="https://github.com/user-attachments/assets/0d1bc0a8-8a7b-47bf-8811-e40a997f8610" />

Maven : A build Automation Tool and helps to manage the Dependencies

"mvn package : used to generate jar file , which we can share with others" 

Life cycle of maven : 
validate - validate the project is correct and all necessary information is available
compile - compile the source code of the project
test - test the compiled source code using a suitable unit testing framework. These tests should not require the code be packaged or deployed
package - take the compiled code and package it in its distributable format, such as a JAR.
verify - run any checks on results of integration tests to ensure quality criteria are met
install - install the package into the local repository, for use as a dependency in other projects locally
deploy - done in the build environment, copies the final package to the remote repository for sharing with other developers and projects.

For Details : https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html#Lifecycle_Reference

Structure of Spring Boot Project :

.mvn & .gitignore: The .mvn folder facilitates the use of the Maven Wrapper, while .gitignore ensures unnecessary files (like IDE-specific configurations or build artifacts) are not tracked in version control)

src Directory: Divided into main (core application code) and test (unit tests). The main folder further separates java code from resources (e.g., application properties and static assets)

pom.xml: Known as the Project Object Model, this file is the heart of a Maven project. It defines project dependencies, plugins, and configuration.

Target & FAT JAR: When the project is packaged, a target folder is generated ,Executable JAR which bundles not just the compiled source code but also all necessary dependencies, allowing the application to run independently without an external server 

>Main jar file contains all necessary dependencies and embeded tomcat server required to run the application.
>The .jar.original file contains only your compiled source code (your classes and resources).

Repackaging: The Spring Boot plugin automatically handles the creation of both an original JAR and the executable FAT JAR, a process known as repackaging. (As first it will create the .jar.original file and with that it will repackage the .jar file)
