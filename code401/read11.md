# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 11 -->
## Spring
[comment]: <> (https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html)

[comment]: <> (https://spring.io/guides/gs/serving-web-content/)

In Spring’s approach to building web sites, HTTP requests are handled by a controller. You can easily identify the controller by the @Controller annotation

To speed up a refresh cycle, Spring Boot offers with a handy module known as spring-boot-devtools. Spring Boot Devtools:

- Enables hot swapping.

- Switches template engines to disable caching.

- Enables LiveReload to automatically refresh the browser.

- Other reasonable defaults based on development instead of production.

@SpringBootApplication is a convenience annotation that adds all of the following:

@Configuration: Tags the class as a source of bean definitions for the application context.

@EnableAutoConfiguration: Tells Spring Boot to start adding beans based on classpath settings, other beans, and various property settings. For example, if spring-webmvc is on the classpath, this annotation flags the application as a web application and activates key behaviors, such as setting up a DispatcherServlet.

@ComponentScan: Tells Spring to look for other components, configurations, and services in the com/example package, letting it find the controllers.

The main() method uses Spring Boot’s SpringApplication.run() method to launch an application. Did you notice that there was not a single line of XML? There is no web.xml file, either. This web application is 100% pure Java and you did not have to deal with configuring any plumbing or infrastructure.

You can run the application from the command line with Gradle or Maven. You can also build a single executable JAR file that contains all the necessary dependencies, classes, and resources and run that. Building an executable jar makes it easy to ship, version, and deploy the service as an application throughout the development lifecycle, across different environments, and so forth.

If you use Gradle, you can run the application by using ./gradlew bootRun. Alternatively, you can build the JAR file by using ./gradlew build and then run the JAR file, as follows:

java -jar build/libs/gs-serving-web-content-0.1.0.jar

Now that the web site is running, visit http://localhost:8080/greeting, where you should see “Hello, World!”

Provide a name query string parameter by visiting http://localhost:8080/greeting?name=User. Notice how the message changes from “Hello, World!” to “Hello, User!”:



[BACK TO HOME](../README.md)