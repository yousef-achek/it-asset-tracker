# IT asset and incident tracker

A console application in Java that tracks IT equipment (servers, switches, firewalls...) and the incidents reported on it. Built as an intermediate project to practice object-oriented design, collections, streams, file storage and unit testing.

## Features

- Add and list assets with type and location (for example "Data center 1, rack A3")
- Report incidents with a severity (LOW, MEDIUM, HIGH, CRITICAL)
- Move incidents through OPEN, IN_PROGRESS and RESOLVED
- Summary report: open incidents by severity, incidents per asset, average resolution time
- Data is saved in the `data/` folder and reloaded at the next start

## Project structure

```
src/main/java/com/yousef/tracker
  Main.java                  console menu
  model/                     Asset, Incident (records) and the enums
  service/TrackerService     business rules and the summary report
  storage/CsvStorage         reads and writes the data files
src/test/java/...            JUnit 5 tests
```

## Run it in IntelliJ IDEA

1. Open the project folder in IntelliJ IDEA. It detects `pom.xml` and imports the project as a Maven project.
2. Set the project SDK to JDK 21 or newer (File > Project Structure > Project).
3. Open `Main.java` and click the green run arrow next to `main`.
4. To run the tests, right-click `src/test/java` and choose Run Tests.

## Ideas to extend it

- Replace the text files with a database using JDBC and SQLite or PostgreSQL
- Add a REST API with Spring Boot, then a web page on top of it
- Add users with roles (technician, manager) and assign incidents to technicians
- Export the summary report to PDF or Excel
- Send an email when a CRITICAL incident is created

Author: Yousef Achek, engineering student at Esprit
