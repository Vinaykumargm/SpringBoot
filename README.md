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

Working of Spring Boot :

In traditional Java, we manually create objects using the new keyword. In Spring Boot, the IoC container manages object creation and lifecycle. We register classes as beans using annotations like @Component, and Spring injects them wherever needed using dependency injection (@Autowired).

The @SpringBootApplication annotation is a combination of @Configuration, @EnableAutoConfiguration, and @ComponentScan, which together enable automatic configuration, bean creation, and component scanning in the application


Spring Security :

<img width="549" height="173" alt="image" src="https://github.com/user-attachments/assets/d64b85e1-8d65-412a-89e7-0cd5f6a5bdc1" />

Authetication : process of verifying a user identification (username & password)
Authorization : 
<img width="559" height="195" alt="image" src="https://github.com/user-attachments/assets/5f40005a-30d1-4687-867c-7d352ca7774a" />

<img width="1866" height="591" alt="Screenshot 2026-04-23 172020" src="https://github.com/user-attachments/assets/4e593a50-c4db-4c28-b5e8-7567141fbe6d" />

By default spring security uses Basic Http Authentication.

<img width="585" height="210" alt="image" src="https://github.com/user-attachments/assets/0522a5d9-48c6-4812-9f62-5b9a4f029d97" />

<img width="495" height="170" alt="image" src="https://github.com/user-attachments/assets/23dd1680-c430-4fb0-8b48-1d7b1195d7b5" />

<img width="482" height="163" alt="image" src="https://github.com/user-attachments/assets/213b8631-7e6a-4d7a-bdfa-7f95b76ff529" />

we can also explicitly define user name and password in the application.properties.

spring.security.user.name=username
spring.security.user.password=password

<img width="437" height="221" alt="image" src="https://github.com/user-attachments/assets/1ec0f8fc-4932-446c-af61-ccc007abc027" />

<img width="571" height="197" alt="image" src="https://github.com/user-attachments/assets/3a74f23d-129c-4d08-b565-700e668143c7" />


<img width="484" height="220" alt="image" src="https://github.com/user-attachments/assets/f37dc47e-4e0d-42c0-b5c7-191ce6b4cb18" />

<img width="556" height="214" alt="image" src="https://github.com/user-attachments/assets/4f4914c1-e9cb-457a-8f2e-4315a1f43ada" />

<img width="1170" height="563" alt="image" src="https://github.com/user-attachments/assets/3f6a2061-a639-4f79-94ef-7475f1299579" />

<img width="484" height="205" alt="image" src="https://github.com/user-attachments/assets/3986555a-6b98-4696-8124-699115faa2c1" />
<img width="585" height="220" alt="image" src="https://github.com/user-attachments/assets/6bbbb048-e3af-45f2-a663-4b377467b30b" />
<img width="1859" height="896" alt="Screenshot 2026-04-24 174543" src="https://github.com/user-attachments/assets/0e0b40bc-1d95-4812-b85a-e01b64c175d3" />

To authenticate users based on their credentials stored in the database.

<img width="1886" height="537" alt="Screenshot 2026-04-24 175458" src="https://github.com/user-attachments/assets/3742c672-3137-45ac-bc0c-d6806ee44901" />
