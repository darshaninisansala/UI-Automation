Automation Assignment – Selenium Java UI Automation

 Objective
The purpose of this project is to design and implement automated UI tests for the [Automation Test Store](https://automationteststore.com/) web application.  
This project demonstrates the ability to build a structured Selenium automation framework using Java, TestNG, and Maven, while following best practices in UI test automation.


Frameworks and Tools Used

This project is developed using the following tools and technologies:

1. Java (JDK 17 or higher)– The main programming language used for writing the test scripts.  
2. Selenium WebDriver – Used to automate interactions with the web browser.  
3. TestNG – Used as the testing framework for managing test cases, assertions, and reports.  
4. Maven– Used as the build and dependency management tool.  
5. WebDriverManager – Used to automatically download and manage browser drivers.  
6. Extent Reports (optional) – Used to generate beautiful HTML reports.  
7. GitHub Actions – Used to run tests automatically in a Continuous Integration (CI) environment.


Project Structure

The project follows a clean Page Object Model (POM) structure for better readability and maintenance.  
Below is the structure of the project:

AutomationTesting/
 pom.xml # Maven dependency file
 README.md # Project documentation
 src/
 main/java/com/automationteststore/
base/ # Base setup classes for WebDriver
common/ # Common reusable commands
pages/ # Page Object classes for different pages
 utilities/ # Utility or helper classes
 test/java/com/automationteststore/testcases/
 AutomationTestStoreTestCase.java
 OtherTestCases.java
 reports/ # Folder containing generated test reports



Setup Instructions

To set up and run the tests locally, follow these steps carefully.

Step 1: Clone the Repository
Open a terminal and run the following command to clone the project:
~bash
git clone https://github.com/<your-username>/automation-assignment.git
cd automation-assignment


Step 2: Install Java
Install Java JDK 17 or later and verify the installation by running:
java -version


Step 3: Install Maven
Download and install Maven from the official website: https://maven.apache.org/download.cgi
Verify the installation by running:
mvn -version


Step 4: Install Dependencies
Once Maven is installed, navigate to your project directory and run:
mvn clean install


How to Run Tests Locally


You can run the tests using either TestNG or Maven.
Option 1 – Run from TestNG
Open the project in IntelliJ IDEA or Eclipse.

Open the AutomationTestStoreTestCase file.
Right-click on it and select Run 'AutomationTestStoreTestCase'.
This will execute all the tests defined in the TestNG suite file.

Option 2 – Run from Maven Command
You can also run tests directly from the terminal using Maven:
mvn clean test


GitHub Actions – Continuous Integration (CI)

This project includes GitHub Actions to automate the process of building and running tests whenever changes are pushed to the repository or when a pull request is created.
GitHub Actions allows you to set up a workflow that runs your Selenium TestNG test cases automatically in a cloud-based environment. This helps ensure that your tests are executed consistently, and any new code changes do not break existing functionality.
In this project, a workflow file named .github/workflows/ci.yml is created to define the CI process. The workflow performs the following steps:
Checks out the repository – This step downloads your code from GitHub so that it can be built and tested.
Sets up the Java environment – The workflow installs Java 17 using the actions/setup-java tool.
Caches Maven dependencies – This step stores previously downloaded Maven dependencies to speed up future builds.
Installs all required dependencies – It runs the Maven command mvn clean install to download and install all necessary libraries.
Runs the automated tests – The command mvn test is executed to run all Selenium TestNG test cases.
Uploads the test reports – Once the tests are finished, the generated reports are automatically uploaded as an artifact. This allows you to download and view them directly from the GitHub Actions interface.



