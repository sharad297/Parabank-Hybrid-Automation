<div align="center">

# 🏦 ParaBank Automation Suite

### A Java + Selenium test automation framework for the ParaBank banking application

[![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.java.com/)
[![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)](https://www.selenium.dev/)
[![TestNG](https://img.shields.io/badge/TestNG-DB4D6D?style=for-the-badge)](https://testng.org/)
[![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)](https://maven.apache.org/)

**Page Object Model · Test-Driven Development · Data-Driven Testing · HTML Reports**

[🌐 Application Under Test](https://parabank.parasoft.com/parabank/index.htm)

</div>

---

## 📖 Overview

**ParaBank Automation Suite** is a UI test automation project for [ParaBank](https://parabank.parasoft.com/parabank/index.htm), Parasoft's sample online banking application. Built with **Java**, **Selenium WebDriver**, **TestNG**, and **Maven**, the framework uses the **Page Object Model (POM)** to separate page interactions from test logic.

It showcases a **Test-Driven Development (TDD)** approach, Excel-based test data handling, centralized logging, HTML reporting, and screenshot capture when tests fail.

## ✨ At a Glance

| 🧩 Maintainability | 🧪 Test Execution | 📈 Observability |
| :--- | :--- | :--- |
| Page Object Model for reusable page actions | TestNG suites with Maven integration | ExtentReports HTML results |
| Separate page, test, and utility packages | Positive and negative login scenarios | log4j2 execution logs |
| Apache POI for Excel-based data | Dedicated suite XML files | Failure screenshots |

## ✅ Automation Coverage

**Test classes visible in the project structure:**

| Area | Scenarios |
| :--- | :--- |
| 🏠 Home page | Verify application logo |
| 👤 Registration | Register a new user |
| 🔐 Authentication | Valid login, empty username, incorrect password, blank fields, case sensitivity |
| 💳 Account overview | Verify account balance display after login |
| 🚪 Session management | Successful logout |
| 🏦 Account management | Open a new account |

**Additional capabilities mentioned in the original project description:** Fund transfers, bill payments, and transaction-history tests. The supplied file tree does not list corresponding test classes, so check the repository before presenting these as completed automated coverage.

## 🛠️ Technology Stack

| Category | Tool / Technology | Purpose |
| :--- | :--- | :--- |
| Language | **Java** | Automation implementation |
| Browser automation | **Selenium WebDriver** | Web UI interactions |
| Testing | **TestNG** | Tests, assertions, and suites |
| Build and dependency management | **Maven** | Build and test execution |
| Design pattern | **Page Object Model (POM)** | Page-level separation and reuse |
| Reporting | **ExtentReports** | HTML execution reports |
| Logging | **log4j2** | Centralized execution logs |
| Data handling | **Apache POI** | Excel-based test data |
| Utilities | **Apache Commons IO / Lang** | Shared helper functionality |

## 🏗️ Framework Structure

```text
Parabank_V1.2/
├── src/
│   ├── main/
│   │   ├── java/                 # Reserved for application code
│   │   └── resources/            # Optional application configuration
│   └── test/
│       ├── java/
│       │   ├── com.parabank.pages/
│       │   │   ├── HomePage.java
│       │   │   ├── LoginAccountPage.java
│       │   │   ├── MyAccountPage.java
│       │   │   ├── OpenNewAccountPage.java
│       │   │   └── RegisterPage.java
│       │   ├── com.parabank.tests/
│       │   │   ├── BaseClass.java
│       │   │   ├── TC001_VerifyLogoTest.java
│       │   │   ├── TC002_RegistrationOfNewUserTest.java
│       │   │   ├── TC003_UserLoginWithValidCredentialsTest.java
│       │   │   ├── TC004_VerifyLoginFailureWithEmptyUsernameTest.java
│       │   │   ├── TC005_VerifyLoginFailureWithIncorrectPasswordTest.java
│       │   │   ├── TC006_VerifyAccountBalanceDisplayAfterLoginTest.java
│       │   │   ├── TC007_VerifySuccessfulLogoutTest.java
│       │   │   ├── TC008_VerifyLoginWithBlankFieldsTest.java
│       │   │   ├── TC009_VerifyCaseSensitivityInLoginTest.java
│       │   │   └── TC021_VerifyOpenNewAccountFunctionalityTest.java
│       │   └── com.parabank.utils/
│       │       └── ExtentReportManager.java
│       └── resources/
│           ├── config.properties
│           ├── log4j2.xml
│           └── logo.png
├── logs/
│   └── execution.log
├── reports/
│   └── ExtentReport.html
├── screenshots/                 # Failure screenshots
├── Parabank-official/           # Application reference files
├── target/                      # Maven build output
├── test-output/                 # TestNG output
├── Master.xml
├── ParallelTesting.xml
├── pom.xml
├── run.bat
└── README.md
```

<details>
<summary><strong>🖼️ View the original project structure screenshot</strong></summary>

<br>

<img src="https://github.com/user-attachments/assets/78e5623c-cf54-42a0-bd32-15366301bea5" alt="ParaBank automation project structure screenshot" width="606" />

</details>

## 🚀 Getting Started

### 1. Prerequisites

- **Java JDK**, compatible with the project's `pom.xml`
- **Apache Maven**
- A supported web browser and appropriate WebDriver configuration
- **IntelliJ IDEA** or **Eclipse** (optional)

### 2. Clone the project

```bash
git clone https://github.com/sagar-bankar/ParaBank_Automation_Hybrid-Automation-Framework.git
cd ParaBank_Automation_Hybrid-Automation-Framework
```

> Verify that the clone URL matches your actual repository before publishing. The original README linked to a browser-based repository viewer rather than a standard clone URL.

### 3. Review test configuration

Check `src/test/resources/config.properties` and your local browser setup before running the tests. Do not commit credentials or other secrets.

### 4. Execute the tests

```bash
mvn clean test
```

The repository also includes `Master.xml`, `ParallelTesting.xml`, and `run.bat`. Review their contents before using them; their exact execution commands are not documented in the original README.

## 📊 Reports, Logs & Screenshots

| Output | Location | What it contains |
| :--- | :--- | :--- |
| 📈 ExtentReports | `reports/ExtentReport.html` | HTML test execution report |
| 🧾 TestNG | `test-output/` | TestNG-generated results |
| 📝 log4j2 | `logs/execution.log` | Test execution logs |
| 📸 Failure screenshots | `screenshots/` | Captures of failed test scenarios |

> Report paths reflect the original project documentation and can depend on your actual framework configuration.

## 🎯 What This Project Demonstrates

- **Test design:** positive and negative scenarios covering login validation and banking workflows.
- **Framework design:** POM-based organization for cleaner, more maintainable tests.
- **Test data management:** Apache POI integration for Excel-driven inputs.
- **Debuggability:** HTML reports, structured logs, and screenshots to support failure analysis.
- **Execution workflow:** Maven-managed test execution and TestNG suite configuration.
