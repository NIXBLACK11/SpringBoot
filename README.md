# SpringBoot

- First head to start.spring.io

![Alt text](./Readme/image.png)

## Annotations
In Spring Boot, annotations are a way to provide metadata to the Spring framework to configure various aspects of your application. Annotations are used to define the behavior of classes, methods, or fields in a concise and declarative manner. They help Spring Boot automatically configure and manage components and services within your application. Here are some common annotations used in Spring Boot:

    @SpringBootApplication:
        This annotation is typically placed on the main class of a Spring Boot application. It combines several other annotations, such as @Configuration, @EnableAutoConfiguration, and @ComponentScan, to enable Spring Boot's auto-configuration and component scanning.

    @Controller, @RestController:
        These annotations are used to define Spring MVC controllers. @Controller is used for traditional MVC controllers, while @RestController is used for RESTful web services and combines @Controller and @ResponseBody.

    @Service:
        This annotation is used to define a service class in Spring. Services are typically used to encapsulate business logic.

    @Repository:
        This annotation is used to define a data repository class. It is often used with Spring Data JPA or other data access technologies.

    @Autowired:
        This annotation is used for automatic dependency injection. It tells Spring to inject a bean of a specified type into the annotated field, constructor, or method.

    @Component:
        This is a generic stereotype annotation used to define a Spring-managed component. It is often used when no specific stereotype annotation (e.g., @Service, @Repository) is more appropriate.

    @Configuration:
        This annotation is used to define a Java-based configuration class. It can be used to define beans and their dependencies.

    @Value:
        This annotation is used to inject values from properties files or application.yml (YAML) files into fields in a Spring component.


In a Java application, "beans" typically refer to JavaBeans, which are a reusable software component model. JavaBeans are Java classes that adhere to a set of conventions for design and naming. They are used to encapsulate and manage the state and behavior of objects. JavaBeans are an essential part of Java's component-based programming paradigm and are often used in various contexts, such as graphical user interfaces (GUIs), enterprise applications, and more. Here are some key characteristics and uses of JavaBeans:

    Properties: JavaBeans typically have private fields (attributes) and public getter and setter methods to access and modify these attributes. For example, a JavaBean representing a person might have properties like name, age, and address, each with corresponding getter and setter methods.

    No-argument Constructor: JavaBeans should provide a no-argument constructor, allowing the instantiation of the bean using the default constructor.

    Serializable: JavaBeans should implement the java.io.Serializable interface to enable them to be easily saved to and restored from streams, making them suitable for various purposes, including data persistence.

    Event Handling: JavaBeans can be used in event-driven programming, where they generate events and can be registered to listen for events. This is common in GUI frameworks like Java Swing.

    Reusability: JavaBeans are designed for reusability. You can create a JavaBean representing a specific entity or functionality and reuse it across different parts of your application or even in different applications.

    Integration: JavaBeans can be easily integrated into development environments and tools, including visual development tools like IDEs and frameworks that rely on component-based architectures.

Here's a simple example of a JavaBean:

java

import java.io.Serializable;

public class PersonBean implements Serializable {
    private String name;
    private int age;

    // No-argument constructor
    public PersonBean() {
    }

    // Getter and setter methods for name
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    // Getter and setter methods for age
    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}

In this example, PersonBean is a simple JavaBean with properties for name and age, along with getter and setter methods.

JavaBeans are used extensively in various Java frameworks and technologies, such as JavaServer Faces (JSF), Spring Framework, and more, to simplify and enhance the development of Java applications.

## Tips:
- Whenever creating something new always create under the dev.sidharth.project folder
- To add a bean to the bin 

    @Component 

    needs to be added before the class so that the bin takes it under and handles it

- I@Bean
Indicates that a method produces a bean to be managed by the Spring container.