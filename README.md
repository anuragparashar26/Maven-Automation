# Maven Automation

## Overview

This is a Java project built using **Maven**, designed for automation testing with **Selenium WebDriver**. It includes test cases and utility classes written in Java, structured under `src/test/java`. Selenium JARs are included in the `lib` folder for local usage, though it's recommended to manage dependencies via Maven for maintainability.

---

## Prerequisites

- **Java Development Kit (JDK):** OpenJDK 21 (or Java 17 for compatibility)
- **Maven:** Version 3.9+ recommended
- **Google Chrome:** Stable release (e.g., `126.0.6478.126` or later)
- **ChromeDriver:** Should match your Chrome browser version (manually or via WebDriverManager)
- **Operating System:** Tested on Ubuntu 24.04, should work on Windows/macOS with minor tweaks

---

## Project Structure

```

.
├── .idea/                   # IntelliJ project configuration
├── lib/
│   └── selenium-java-4.29.0.jar    # Selenium JAR manually added (optional if using Maven dependency)
├── src/
│   └── test/
│       └── java/
│           └── com/
│               └── example/
│                   ├── Main.java
│                   └── LoginTest.java
├── pom.xml                 # Maven configuration file
└── .gitignore

````

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/anuragparashar26/Maven-Automation.git
cd Maven-Automation
````

### 2. Set Up Java

Check if Java is installed:

```bash
java -version
```

If not installed:

```bash
sudo apt update
sudo apt install openjdk-21-jdk
```

Set `JAVA_HOME` (Ubuntu):

```bash
export JAVA_HOME=/usr/lib/jvm/java-21-openjdk-amd64
echo "export JAVA_HOME=/usr/lib/jvm/java-21-openjdk-amd64" >> ~/.bashrc
source ~/.bashrc
```

---

## Maven Dependency (Recommended)

If you're not using the local JAR in `lib/`, add Selenium to `pom.xml`:

```xml
<dependencies>
    <dependency>
        <groupId>org.seleniumhq.selenium</groupId>
        <artifactId>selenium-java</artifactId>
        <version>4.29.0</version>
    </dependency>
</dependencies>
```

Run Maven to install dependencies:

```bash
mvn clean install
```

---

## Run Tests

To execute tests with Maven:

```bash
mvn test
```

You can also run individual test files from your IDE like IntelliJ.

Test reports will be generated under:

```
target/surefire-reports/
```

---

## Example Test: `LoginTest.java`

A sample Selenium test that automates browser interactions like visiting a login page, entering credentials, and submitting the form.

---
