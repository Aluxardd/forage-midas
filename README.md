# Midas - JPMC Advanced Software Engineering Forage Program

## Project Overview
I completed the Midas project as part of the JPMC Advanced Software Engineering Forage program. Midas is a Spring Boot application that simulates a financial transaction processing system. Throughout this project, I built a system that processes financial transactions between users, updates their balances, and provides an API to query user balances.

## Tools I Used
- Java 17 for development
- Maven for building and running tests
- Git for version control

## Project Structure I Worked With
I worked with the following project structure:

- `src/main/java/com/jpmc/midascore/`
  - `MidasCoreApplication.java` - The main Spring Boot application class that I configured
  - `component/` - Where I implemented application components
    - `DatabaseConduit.java` - I used this wrapper for database operations
  - `entity/` - Where I defined JPA entities
    - `UserRecord.java` - I used this entity to represent users with balances
  - `foundation/` - Where I worked with domain models
    - `Balance.java` - I used this to represent user balances
    - `Transaction.java` - I used this to represent financial transactions between users
  - `repository/` - Where I implemented data access
    - `UserRepository.java` - I used this repository for UserRecord entities
- `src/test/java/com/jpmc/midascore/`
  - `TaskOneTests.java` through `TaskFiveTests.java` - Test classes I ran for each task
  - Helper classes I used for testing:
    - `BalanceQuerier.java` - I used this to query the balance API
    - `FileLoader.java` - I used this to load test data from files
    - `KafkaProducer.java` - I used this to send transactions to Kafka
    - `UserPopulator.java` - I used this to populate the database with users

## Tasks I Completed

### Task One: Application Setup
For the first task, I ensured the application booted successfully. I ran the test which verified the setup and produced a mathematical sequence as output.

### Task Two: Kafka Integration
I implemented Kafka message consumption in the application. I created a consumer that processed transaction data sent to a Kafka topic by the test.

### Task Three: Transaction Processing
I developed transaction processing logic that updates user balances. The test populated the database with users and sent transactions. I implemented the logic to process these transactions and was able to find Waldorf's balance after all transactions were processed.

### Task Four: Advanced Transaction Processing
Building on Task Three, I enhanced the transaction processing to handle different scenarios and edge cases. I used a different set of transaction data and successfully determined Wilbur's balance after all transactions were processed.

### Task Five: REST API Implementation
For the final task, I implemented a REST API to query user balances. I created an endpoint that allowed the test to query the balances of users with IDs 0 through 12 after processing transactions.

## How I Ran the Tests
Each task had a corresponding test class that I ran to verify my implementation. The tests guided me through the tasks and provided feedback on my progress.

I ran each test using the following command:
```
mvn test -Dtest=TaskOneTests
```

I replaced `TaskOneTests` with the name of the test class for the task I was working on (e.g., `TaskTwoTests`, `TaskThreeTests`, etc.).

## Resources I Used
- I utilized the `services/transaction-incentive-api.jar` file as a service for some of the tasks.
- I configured the initially empty `application.yml` file as needed for the different tasks.
- I worked with test data stored in files in the `src/test/resources/test_data/` directory.

