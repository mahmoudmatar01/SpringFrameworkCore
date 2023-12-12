# Spring Framework Tutorials

Welcome to the Spring Framework tutorials repository! This series is designed to provide you with a solid foundation in the Spring framework, a versatile and widely used framework for building Java-based enterprise applications. Let's dive into the first two tutorials:

## 1. Introduction to Spring Framework (Spring Tutorial 00)

### Overview

Welcome to the Spring Framework Tutorial 00: Introduction to Spring Framework. This tutorial provides a foundational understanding of the Spring framework, a robust and comprehensive framework for building Java-based enterprise applications. Let's delve into the key aspects of Spring.

### What is Spring?

**Spring** is an open-source framework for building enterprise applications in Java. It addresses the complexity of enterprise application development by providing a cohesive and modular infrastructure.

#### Key Features

1. **Inversion of Control (IoC):** In Spring, IoC is a core principle that shifts the control of program flow from the developer to the Spring container.
2. **Aspect-Oriented Programming (AOP):** Spring supports Aspect-Oriented Programming, allowing developers to modularize cross-cutting concerns like logging and security.
3. **Data Access:** Spring provides a consistent and simplified approach to data access through JDBC and Object-Relational Mapping (ORM) frameworks.
4. **Transaction Management:** Spring facilitates declarative transaction management, ensuring data integrity in database operations.
5. **Model-View-Controller (MVC):** Spring MVC is a powerful framework for building web applications following the Model-View-Controller architectural pattern.

### Core Concepts

1. **Inversion of Control (IoC):** In Spring, IoC is achieved by the Spring container, which manages the lifecycle of application objects.
2. **Dependency Injection (DI):** Dependency Injection is a key concept where the Spring container injects dependencies into a class, promoting loose coupling.

### Spring Ecosystem

1. **Spring Boot:** Spring Boot simplifies the process of building production-ready applications, providing defaults for application setup and enhanced features like embedded servers.
2. **Spring Data:** Spring Data simplifies data access, providing a consistent approach to data repositories.
3. **Spring Security:** Spring Security offers comprehensive security services for Java EE-based enterprise software applications.

### Example: Hello, Spring!

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Spring!");
    }
}
```


## Dependency Injection in Spring (Spring Tutorial 01)

### What is Dependency Injection?

**Dependency Injection (DI)** is a design pattern used in software development, including Spring. It addresses the coupling between classes by allowing the inversion of control over their dependencies. In simpler terms, instead of a class creating its dependencies, they are injected from the outside.

### Advantages of Dependency Injection

1. **Loose Coupling:** Dependency Injection promotes loose coupling, making it easier to modify, extend, and test code. Changes in one part of the application don't necessarily impact other parts.

2. **Testability:** DI facilitates easier testing by allowing the substitution of real dependencies with mock or test dependencies during unit testing.

3. **Reusability:** Classes become more reusable as they are not tightly coupled to specific implementations of their dependencies.

### Dependency Injection in Spring

In Spring, DI is achieved through:

### Constructor Injection

```java
public class Car {
    private Engine engine;

    // Constructor Injection
    public Car(Engine engine) {
        this.engine = engine;
    }

    // ...
}
```

### Setter Injection
```java
public class Car {
    private Engine engine;

    // Setter Injection
    public void setEngine(Engine engine) {
        this.engine = engine;
    }

    // ...
}
```

### Example: Spring Dependency Injection
```java
public interface Engine {
    void start();
}

public class GasolineEngine implements Engine {
    @Override
    public void start() {
        System.out.println("Gasoline engine started");
    }
}

public class ElectricEngine implements Engine {
    @Override
    public void start() {
        System.out.println("Electric engine started");
    }
}

public class Car {
    private Engine engine;

    // Constructor Injection
    public Car(Engine engine) {
        this.engine = engine;
    }

    public void start() {
        engine.start();
        System.out.println("Car started!");
    }
}
```
In this example, the Car class is injected with an Engine implementation, either GasolineEngine or ElectricEngine. This enables the flexibility to switch between different engine implementations without modifying the Car class.



## Spring Tutorial 02 - Setting Up

### Overview

Welcome to Spring Tutorial 02: Setting Up. In this tutorial, we'll guide you through the process of setting up your development environment for Spring framework development. Proper setup ensures a smooth development experience and allows you to leverage the full power of Spring for building robust Java applications.

### Prerequisites

Before setting up your Spring development environment, make sure you have the following prerequisites installed:

1. **Java Development Kit (JDK):** Spring is a Java-based framework, so you need to have JDK installed on your machine. You can download the latest version from [Oracle JDK](https://www.oracle.com/java/technologies/javase-downloads.html) or use [OpenJDK](https://adoptopenjdk.net/).

2. **Integrated Development Environment (IDE):** Choose an IDE that suits your preferences. Popular choices include [Eclipse](https://www.eclipse.org/downloads/), [IntelliJ IDEA](https://www.jetbrains.com/idea/download/), or [Visual Studio Code](https://code.visualstudio.com/). Make sure your IDE supports Java development.

### Setting Up a Spring Project

Now, let's create a simple Spring project to verify your setup. Follow these steps:

### Step 1: Install Build Tool (Optional)

You can use a build tool like [Apache Maven](https://maven.apache.org/) or [Gradle](https://gradle.org/) to manage dependencies and build your project. If you don't have Maven or Gradle installed, consider installing one of them.

### Step 2: Create a Spring Project

#### Using Spring Initializr (Online)

1. Visit [Spring Initializr](https://start.spring.io/).
2. Choose your project settings, including project type, language (Java), Spring Boot version, and dependencies.
3. Click "Generate" to download the project ZIP file.

#### Using IDE (Eclipse as an example)

1. Open your IDE and create a new Maven or Gradle project.
2. Add the necessary Spring dependencies to your project configuration.

### Step 3: Verify Your Setup

Create a simple "Hello, Spring!" application. Here's an example using Spring Boot:

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class HelloSpringApplication {

    public static void main(String[] args) {
        SpringApplication.run(HelloSpringApplication.class, args);
    }
}
```

### Step 4: Run the Application
Run your Spring application and navigate to http://localhost:8080 in your web browser. If everything is set up correctly, you should see a "Whitelabel Error Page" indicating that your Spring application is running.






