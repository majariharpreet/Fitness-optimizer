# AI Fitness & Health Optimizer

A full-stack Java Web Application developed as a mini-project for **Advanced Internet Programming**. This tool calculates a user's BMI, determines their health status, and generates a personalized diet and workout plan based on their dietary preferences (Veg/Non-Veg) and fitness goals (Weight Gain/Loss).

## 🚀 Features
- **BMI Calculator:** Real-time BMI calculation based on Height (cm) and Weight (kg).
- **Dynamic Diet Generation:** Suggests specific protein-rich foods from a MySQL database based on user preference.
- **Workout Planner:** Tailors exercise routines (HIIT, Strength Training, etc.) according to user goals.
- **Modern GUI:** Responsive design featuring a CSS-based BMI reference slider and Glassmorphism effects.
- **PDF Export:** Integrated `html2pdf.js` module to download the health report as a professional PDF.

## 🛠️ Technology Stack
| Layer | Technology |
| :--- | :--- |
| **Frontend** | JSP, CSS3 (Advanced Styling), JavaScript (ES6) |
| **Backend** | Java Servlets (Jakarta EE 9+ / Tomcat 10) |
| **Logic** | Plain Old Java Objects (POJO) |
| **Database** | MySQL 8.0 |
| **Library** | html2pdf.js, MySQL Connector/J |

## 📁 Project Structure
- `com.fitness.controller`: Contains `HealthServlet.java` (Handles Request/Response).
- `com.fitness.logic`: Contains `HealthCalculator.java` (BMI and status logic).
- `src/main/webapp`: Contains `index.jsp` (Input form) and `result.jsp` (Output report).
- `WEB-INF/lib`: Contains the MySQL Database driver.

## ⚙️ Setup Instructions

### 1. Database Setup
1. Open MySQL Workbench.
2. Run the provided SQL scripts:
   - `health_db_food_items.sql`
   - `health_db_workouts.sql`
3. Ensure the database name is `health_db`.

### 2. Eclipse Configuration
1. Import the project folder into your Eclipse workspace.
2. Ensure you have **Apache Tomcat v10.x** configured as the server.
3. Check that the `mysql-connector-j-x.x.x.jar` is in the Build Path.
4. **Important:** Update the database password in `HealthServlet.java`:
   ```java
   Connection con = DriverManager.getConnection("jdbc:mysql://localhost:3306/health_db", "root", "YourPassword");
