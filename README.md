# Disabled WebElement Handling using JavaScriptExecutor

This project demonstrates how to handle a **disabled web element** in Selenium using the `JavascriptExecutor` interface in Java.

## Project Overview

Normally, Selenium cannot directly interact with disabled input fields using `sendKeys()`.
In this example, JavaScriptExecutor is used to enter text into a disabled textbox.

The script:

* Launches Chrome browser
* Opens the QSpiders demo application
* Navigates to the Disabled element section
* Checks whether the element is enabled
* Uses JavaScriptExecutor to enter text into the disabled field

---

##Technologies Used

* Java
* Selenium WebDriver
* ChromeDriver
* JavaScriptExecutor
* Eclipse / IntelliJ IDEA

---

## Project Structure

```bash
learning_JavascriptExecutor_Interface/
│── Disabled_WebElement.java
```

---

##Features

* Browser automation using Selenium
* Handling disabled elements
* Using JavaScriptExecutor in Selenium
* Checking element state with `isEnabled()`

---

## Code Explanation

### 1. Launch Chrome Browser

```java
WebDriver driver = new ChromeDriver();
```

### 2. Maximize Window & Apply Wait

```java
driver.manage().window().maximize();
driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(20));
```

### 3. Open Demo Website

```java
driver.get("https://demoapps.qspiders.com/ui");
```

### 4. Click Disabled Section

```java
driver.findElement(By.xpath("//li[text()='Disabled']")).click();
```

### 5. Locate Disabled Textbox

```java
WebElement ele = driver.findElement(By.id("email"));
```

### 6. Verify Element Status

```java
System.out.println(ele.isEnabled());
```

### 7. Use JavaScriptExecutor

```java
JavascriptExecutor js = (JavascriptExecutor) driver;

js.executeScript("arguments[0].value='Mani'", ele);
```

---

## How to Run

1. Install Java JDK
2. Install Selenium dependencies
3. Configure ChromeDriver
4. Run the Java file

---

## Expected Output

```bash
false
```

The textbox is disabled, but the value is still entered using JavaScriptExecutor.

---

## Learning Outcome

Through this project, you will learn:

* What disabled elements are
* Why Selenium cannot interact with them directly
* How JavaScriptExecutor bypasses UI restrictions
* Real-time automation handling techniques

---

## Author

Maniyarasi
Aspiring Software Test Engineer | Automation Testing Enthusiast
