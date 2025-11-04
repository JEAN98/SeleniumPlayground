# TrainingAutomation2 — Selenium Test Automation Learning Project
[![Java](https://img.shields.io/badge/Java-8%2B-blue)](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html)
[![Selenium](https://img.shields.io/badge/Selenium-3.x-green)](https://www.selenium.dev/)
[![TestNG](https://img.shields.io/badge/TestNG-%F0%9F%9A%80-lightgrey)](https://testng.org/doc/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> 🧠 *This project was created some time ago as a learning exercise to explore Selenium WebDriver and TestNG for UI automation.*

---

## 📖 Overview

**TrainingAutomation2** is a Java-based UI automation framework built to practice and demonstrate automated web testing concepts using **Selenium WebDriver** and **TestNG**.  
It follows the **Page Object Model (POM)** design pattern and includes examples of **local** and **remote (Selenium Grid)** test execution, **data-driven testing**, and modular page structures.

The project automates a sample web application covering flows like registration, login, posting ads, and browsing categories.

---

## 🚀 Features

- End‑to‑end UI automation with Selenium WebDriver  
- Organized Page Object Model (POM) with reusable page classes  
- Configurable for **local** and **remote (Grid)** test runs  
- **Data‑driven** tests using JSON and TestNG `@DataProvider`  
- Suite configuration through TestNG XML files  
- NetBeans/Ant compatible project layout  

---

## 📦 Project Structure

```
TrainingAutomation2/
  ├── src/trainingautomation2/
  │   └── TrainingAutomation2.java
  ├── test/
  │   ├── base/ (BaseTest, BasePage)
  │   ├── page/ (HomePage, LoginPage, RegisterPage, etc.)
  │   ├── test/ (TestNG test classes for each feature)
  │   ├── utilities/ (DriverHelper, LocalDriver, RemoteDriver, etc.)
  │   ├── entities/ (Data models like PersonRegister)
  │   ├── jsonFiles/ (Test data such as PersonRegister.json)
  │   └── xmfiles/ (TestNG suite files: Config1.xml, Grid.xml)
  ├── build.xml
  └── nbproject/
```

---

## 🧰 Technologies Used

- **Language:** Java (JDK 8+)
- **Framework:** TestNG
- **Automation:** Selenium WebDriver (3.x)
- **Utilities:** Gson, Guava, Apache HttpClient, OkHttp
- **IDE:** NetBeans (Ant build system)
- **Browsers:** Chrome, Firefox
- **Optional:** Selenium Grid

---

## ⚙️ Installation

### Prerequisites

- Install **Java JDK 8+**
- Add **ChromeDriver** or **GeckoDriver** to your PATH
- (Optional) Start a Selenium Grid hub at `http://localhost:4445/wd/hub`

### Setup

1. **Clone or unzip** the project:
   ```bash
   git clone <repo-url>
   ```

2. **Open in NetBeans**
   - File → Open Project → select `TrainingAutomation2`
   - Verify TestNG and Selenium JARs are configured under Project Properties → Libraries

3. **Or run via command line:**
   ```bash
   java -cp "<build-classes>:<test-classes>:<path-to-libs/*>" org.testng.TestNG test/xmfiles/Config1.xml
   ```

---

## 🧪 Usage

### Run Tests Locally
```bash
java -cp "<libs/*>:build/classes" org.testng.TestNG test/xmfiles/Config1.xml
```

### Run Tests on Selenium Grid
```bash
java -cp "<libs/*>:build/classes" org.testng.TestNG test/xmfiles/Grid.xml
```

---

## 🧾 Configuration

TestNG suite files (`test/xmfiles/Config1.xml` and `Grid.xml`) define runtime parameters:

```xml
<suite name="AutomationTraining">
  <parameter name="browser" value="chrome"/>
  <parameter name="startURL" value="http://192.168.0.103:86/"/>
  <parameter name="driverType" value="localdriver"/>
</suite>
```

You can modify:
- `browser`: `chrome` or `firefox`
- `startURL`: Base URL for the AUT (application under test)
- `driverType`: `localdriver` or `remotedriver`

---

## 📚 Learning Topics Demonstrated

- Building maintainable POM frameworks in Java  
- Using TestNG annotations (`@BeforeClass`, `@Test`, `@DataProvider`)  
- Integrating JSON-based test data  
- Switching between local and remote execution  
- Structuring test suites and organizing code modularly  

---

## 🤝 Contributing

This was originally a personal learning project, but contributions are welcome to modernize it (e.g., migrate to Maven/Gradle or Selenium 4).

1. Fork and clone the repo  
2. Create a branch (`feature/your-change`)  
3. Make your updates and commit  
4. Submit a pull request

---

## 🧾 License

This project is licensed under the **MIT License**.

---

## 🏁 Notes

> 🗓️ This framework was built several years ago as a **learning exercise** to understand Selenium and TestNG fundamentals.  
> It serves as a good starting point for anyone exploring test automation in Java.
