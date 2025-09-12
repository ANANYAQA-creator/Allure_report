📊 Allure Report with TestNG + Maven

Generate beautiful Allure Reports for TestNG tests in a Maven project.

🏗 Setup Flow
graph TD;
A[TestNG Project] --> B[Add Dependencies in pom.xml]
B --> C[Run Tests with Maven]
C --> D[Allure Results Generated]
D --> E[Generate Allure Report]
E --> F[View in Browser 🎉]

🔧 Step 1: Add Dependencies

Add TestNG

Add Allure TestNG adapter

(Optional) Add Allure Maven plugin

📌 All dependencies can be found on Maven Central
.

💻 Step 2: Install Allure CLI

You need Allure CLI to generate and view reports.

🥇 Option A – Scoop (Recommended, Windows)

Install Scoop
.

Run in PowerShell:

scoop install allure


Verify:

allure --version

🥈 Option B – Manual Download

Download the latest zip from Allure Releases
.

Extract (e.g., C:\tools\allure-2.xx).

Add bin folder to PATH.

Verify with allure --version.

🥉 Option C – npm (Node.js)

Global: npm install -g allure-commandline

Project: npm install --save-dev allure-commandline

▶️ Step 3: Run Tests & Generate Report
⚡ Run Tests
mvn clean test

📂 Create Results Folder (if not auto-generated)

Linux/Mac: mkdir -p allure-results

Windows: mkdir allure-results

📊 Generate Report

Quick (temporary server):

allure serve allure-results


Persistent (sharable folder):

allure generate allure-results --clean -o allure-report
allure open allure-report

🎉 Final Output

allure-results/ → Raw data from test execution.

allure-report/ → Beautiful interactive HTML report.

Report opens automatically in your default browser.

📝 Notes

Ensure Java 8+ is installed (Allure CLI requires it).

allure serve is great for local quick checks.

Use allure generate when you want a permanent report folder to share.