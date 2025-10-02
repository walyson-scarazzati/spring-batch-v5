## 📚 Learning Resources

This project is based on the Udemy course:
- **Course**: "Curso Otimização de desempenho para jobs Spring Batch"
- **URL**: https://www.udemy.com/course/otimizacao-de-desempenho-para-jobs-spring-batch/

# Spring Batch v5 Demo Project

A demonstration project for Spring Batch v5 with Spring Boot 3.5.6, showcasing batch processing capabilities and performance optimization techniques.

## 📋 Table of Contents

- [Overview](#overview)
- [Technologies](#technologies)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Running the Application](#running-the-application)
- [Configuration](#configuration)
- [Learning Resources](#learning-resources)
- [Contributing](#contributing)

## 🎯 Overview

This project demonstrates the implementation of Spring Batch v5 features with a simple "Hello World" job. It serves as a foundation for learning Spring Batch concepts, job configuration, and performance optimization techniques.

### Key Features

- **Spring Batch v5**: Latest version of Spring Batch framework
- **Spring Boot 3.5.6**: Modern Spring Boot setup with auto-configuration
- **H2 Database**: In-memory database for job repository
- **Tasklet-based Job**: Simple job implementation using tasklets
- **Maven Build**: Standard Maven project structure

## 🛠 Technologies

- **Java 17**: Modern Java LTS version
- **Spring Boot 3.5.6**: Application framework
- **Spring Batch 5.x**: Batch processing framework
- **H2 Database**: In-memory database for development
- **Maven**: Build and dependency management

## 📋 Prerequisites

Before running this project, ensure you have:

- **JDK 17** or later installed
- **Maven 3.6+** for building the project
- **Git** for version control
- **IDE** (IntelliJ IDEA, Eclipse, or VS Code recommended)

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone <repository-url>
cd spring-batch-v5
```

### 2. Build the Project

```bash
mvn clean compile
```

### 3. Run Tests

```bash
mvn test
```

### 4. Run the Application

```bash
mvn spring-boot:run
```

Or using the Maven wrapper:

```bash
# On Windows
mvnw.cmd spring-boot:run

# On Unix/Linux/macOS
./mvnw spring-boot:run
```

## 📁 Project Structure

```
spring-batch-v5/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── br/com/walyson/spring_batch_v5/
│   │   │       ├── SpringBatchV5Application.java    # Main application class
│   │   │       └── BatchConfig.java                 # Batch job configuration
│   │   └── resources/
│   │       └── application.properties               # Application configuration
│   └── test/
│       └── java/
│           └── br/com/walyson/spring_batch_v5/
│               └── SpringBatchV5ApplicationTests.java
├── target/                                          # Build output directory
├── pom.xml                                         # Maven configuration
├── README.md                                       # Project documentation
└── mvnw, mvnw.cmd                                 # Maven wrapper scripts
```

## 🔧 Configuration

### Application Properties

The application uses H2 in-memory database by default. Configuration can be found in `src/main/resources/application.properties`:

```properties
spring.application.name=spring-batch-v5
```

### Job Configuration

The batch job is configured in `BatchConfig.java` and includes:

- **Job**: Main job bean named "job"
- **Step**: Single step that executes a simple tasklet
- **Tasklet**: Prints "Ola Mundo" to console

### H2 Database Console

When running the application, you can access the H2 console at:
- URL: `http://localhost:8080/h2-console`
- JDBC URL: `jdbc:h2:mem:testdb`
- Username: `sa`
- Password: (leave empty)

## 🏃 Running the Application

The application will automatically execute the configured batch job on startup. You should see output similar to:

```
Ola Mundo
Job: [SimpleJob: [name=job]] completed with the following parameters: [{}] and the following status: [COMPLETED]
```

### Running with Different Profiles

You can run the application with different Spring profiles:

```bash
mvn spring-boot:run -Dspring-boot.run.profiles=dev
```

### Additional Resources

- [Spring Batch Documentation](https://docs.spring.io/spring-batch/docs/current/reference/html/)
- [Spring Boot Documentation](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/)
- [Spring Batch Samples](https://github.com/spring-projects/spring-batch/tree/main/spring-batch-samples)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is for educational purposes. Please refer to the course materials for licensing information.

## 👨‍💻 Author

- **Walyson** - Initial work and course implementation

---

**Note**: This is a demo project for learning Spring Batch concepts. For production use, consider adding proper error handling, logging, monitoring, and security configurations.
