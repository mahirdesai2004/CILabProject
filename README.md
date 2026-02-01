# Jenkins CI/CD Lab Project

**Name:** Mahir Desai
**Registration Number:** 23FE10CSE00345
**Course:** DevOps Lab Assignment 1

---

## 📖 1. User Manual
This project demonstrates a Continuous Integration (CI) pipeline using Jenkins. It includes a Java Calculator application and Python scripts for automation.

### **How to Run the Pipeline**
1.  **Open Jenkins:** Navigate to 'http://localhost:8080' and log in.
2.  **Freestyle Job:**
    * Go to **Job1_Freestyle_Calculator**.
    * Click **Build Now**.
    * Check the **Console Output** to see the Python script execution.
3.  **Multibranch Pipeline:**
    * Go to **Job2_Multibranch_Pipeline**.
    * Click **Scan Multibranch Pipeline Now**.
    * Jenkins will automatically detect the 'Jenkinsfile' and run the stages (Build, Test, Deploy).

---

## ⚙️ 2. Installation Guide
Follow these steps to set up the environment on a local machine (macOS/Linux).

### **Prerequisites**
* **Java:** JDK 17 or newer ('java -version').
* **Git:** Installed and configured ('git --version').
* **Jenkins:** Latest LTS version.

### **Setup Steps**
1.  **Install Jenkins:**
    * On macOS (Homebrew): 'brew install jenkins-lts'
    * Start Service: 'brew services start jenkins-lts'
2.  **Unlock Jenkins:**
    * Copy the initial admin password from the path shown in the terminal.
    * Paste it into the setup wizard at 'http://localhost:8080'.
3.  **Install Plugins:**
    * Select "Install Suggested Plugins".
    * Additionally, ensure **Git**, **Pipeline**, and **JUnit** plugins are installed.
4.  **Global Tool Configuration:**
    * Go to 'Manage Jenkins' -> 'Tools'.
    * Set **JDK Path** to your local Java installation.
    * Set **Git Path** to '/usr/bin/git'.

---

## 🔧 3. Troubleshooting Guide
Common issues encountered during setup and their solutions.

### **Issue 1: "Jenkins command not found"**
* **Cause:** Jenkins is not in the system PATH.
* **Fix:** Use Homebrew to start it: 'brew services start jenkins-lts' or run the WAR file directly: 'java -jar jenkins.war'.

### **Issue 2: "Port 8080 already in use"**
* **Cause:** Another service is using the default Jenkins port.
* **Fix:** Change the port by running: 'java -jar jenkins.war --httpPort=9090'.

### **Issue 3: "Java version mismatch"**
* **Cause:** Jenkins requires Java 11, 17, or 21.
* **Fix:** Verify your Java version with 'java -version'. If using Java 8, upgrade to Java 17 or 21.
