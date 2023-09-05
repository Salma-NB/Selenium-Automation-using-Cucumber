# Selenium Automation using Cucumber

![GitHub last commit](https://img.shields.io/github/last-commit/Salma-NB/Selenium-Automation-using-Cucumber)
![GitHub](https://img.shields.io/github/license/Salma-NB/Selenium-Automation-using-Cucumber)

This repository contains a sample Selenium WebDriver project using Cucumber and Java for automated web testing. It demonstrates best practices for writing BDD-style (Behavior-Driven Development) test scripts and organizing your automation project.

The Selenium Automation using Cucumber is based on https://www.demoblaze.com/index.html

## Table of Contents

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Project Structure](#project-structure)
- [Writing Test Scenarios](#writing-test-scenarios)
- [Running Tests](#running-tests)
- [Reporting](#reporting)
- [Contributing](#contributing)
- [License](#license)

## Getting Started

These instructions will help you set up and run the Selenium automation project on your local machine.

### Prerequisites

Before you begin, ensure you have met the following requirements:

- Java Development Kit (JDK) 8 or higher installed.
- Maven installed.
- Your favorite integrated development environment (IDE) set up for Java development (e.g., Eclipse, IntelliJ, or Visual Studio Code).
- Chrome or Firefox web browser installed (you can configure other browsers if needed).

### Installation

1. Clone this repository:
   git clone https://github.com/Salma-NB/Selenium-Automation-using-Cucumber.git

2. Navigate to the project directory:
cd Web-Testing-using-Selenium-WebDriver-and-TestNg

3. Install project dependencies using Maven:
mvn clean install

### Project Structure
The project follows a standard Maven project structure with the following important directories:

src/main/java: Java source code for your automation framework.
src/main/resources: Configuration files, property files, and any other resources.
src/test/resources/features: Cucumber feature files containing test scenarios written in Gherkin syntax.
src/test/java: Step definitions and hooks for your Cucumber tests.
drivers: Store your WebDriver executable files (e.g., chromedriver, geckodriver) here.

### Writing Test Scenarios
You can start writing your test scenarios in the src/test/resources/features directory using Gherkin syntax. Organize your feature files logically. Here's a sample feature file:

Feature: User Login

  Scenario: Valid user login
  
    Given the user is on the login page
    When the user enters valid credentials
    Then the user should be logged in successfully

  Scenario: Invalid user login
  
    Given the user is on the login page
    When the user enters invalid credentials
    Then the user should see an error message

Implement step definitions in Java in the src/test/java directory to map these scenarios to automation code.

### Running Tests
To run your Cucumber tests, use TestNG XML files located in the src/test/resources directory. Sample TestNG XML file:
<!DOCTYPE suite SYSTEM "http://testng.org/testng-1.0.dtd">
<suite name="TestSuite">
    <test name="Test">
        <classes>
            <class name="com.example.tests.RunCucumberTests"/>
            <!-- Add more test classes here -->
        </classes>
    </test>
</suite>

Execute the tests using Maven:
mvn clean test -DsuiteXmlFile=testng.xml

### Reporting
Cucumber generates test reports in various formats (e.g., HTML, JSON, XML). You can configure the reporting options in the cucumber.properties file and view the reports in your browser.

### Contributing
Feel free to contribute to this project by creating pull requests or opening issues. Please follow the project's coding standards and guidelines when submitting changes.

### License
This project is licensed under the MIT License.
