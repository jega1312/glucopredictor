# GlucoPredictor 🩺📊

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5-7952B3?style=flat&logo=bootstrap&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-AA4A44?style=flat)

> A web-based diabetes risk assessment and data entry system designed to help users evaluate and monitor their potential risk for diabetes — providing personalized rule and AI-based health tips using a trained XGBoost model.

---

## 📷 Screenshots

![Login Page](assets/login.png)
![Dashboard Homepage](assets/home-en.png)
![Diabetes Risk Assessment Form Page](assets/form-en.png)
![Diabetes Risk Assessment Result Page](assets/result.png)
![Personalized Health Tips Page](assets/tips-en.png)
![History Page](assets/history.png)
![Admin Dashboard](assets/admin.png)

---

## 💡 About The Project

**GlucoPredictor** is a web-based diabetes risk assessment and data entry system designed to help users evaluate and monitor their potential risk for diabetes. The system allows users to perform diabetes risk assessments, obtain risk assessment results, and track their glucose levels, insulin usage, and weight, while providing personalized rule and AI-based health tips using a trained XGBoost model and educational insights about diabetes.

> **Note:** Some portions of this code were developed with assistance from AI tools (e.g., ChatGPT). All AI-generated content has been reviewed and adapted by the developer to ensure accuracy and suitability for the project.

---

## ⚠️ Disclaimer

**GlucoPredictor** is intended for educational and non-commercial use only. This project is not a certified medical device or diagnostic tool. The results and health tips provided are based on general rules and AI predictions, and should not be considered as medical advice or diagnosis.

**Always consult with a qualified healthcare professional for medical concerns or before making decisions about your health.**

---

## ✨ Key Features

| # | Feature | Description |
|---|---|---|
| 1 | **User Authentication** | Registration, login, and email verification using PHPMailer. Admin panel to manage users and system access. |
| 2 | **Risk Assessment** | Calculates diabetes risk using both rule-based logic and AI-based predictions (XGBoost). Past results tracked on history page. |
| 3 | **Health Tracking** | Track glucose levels, insulin usage, and weight — visualized with charts and tables. |
| 4 | **Personalized Health Tips** | Health tips based on risk levels. AI-generated bonus tips fostering healthier living. |
| 5 | **Bilingual Support** | Supports English and Malay languages. |
| 6 | **Responsive Design** | Mobile-friendly with a dark mode toggle. |
| 7 | **Reset Password** | Users can reset their passwords if forgotten. |
| 8 | **Edit Profile** | Users can edit their username and password whenever desired. |
| 9 | **Account Deletion** | Users can delete their accounts along with their risk assessment details. |
| 10 | **Admin Dashboard** | Admins can manage and remove users, view user count, and edit their own profile. |

---

## ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, Bootstrap, JavaScript |
| Backend | PHP |
| Machine Learning | XGBoost (Python) |
| Database | MySQL (phpMyAdmin) |
| Server | Apache (XAMPP for local hosting) |

---

## 🧪 How It Works

1. **User Registration & Login** — Users sign up, activate their accounts via email, and log in. Admin users can manage other users.

2. **Data Input** — Users input details such as age, gender, pregnancies, weight, height, family history, blood pressure, activity level, sugar consumption, and symptoms on `form.php`. Glucose levels, insulin intake, and weight can also be tracked on dedicated tracking pages.

3. **Risk Calculation** — Risk is calculated using predefined rules via JavaScript and the AI model (`predict.py`) based on form inputs, and displayed on `result.php`.

4. **Health Tips** — Based on the risk assessment result, users receive personalized rule & AI-based health tips on `tips.php`.

5. **Risk Score History Tracking** — Users can view their stored risk score history on `history.php`.

---

## 🛠️ Installation

### Prerequisites

- [**XAMPP**](https://www.apachefriends.org/index.html) — to run Apache & MySQL locally
- [**Python 3**](https://www.python.org/downloads/) — for running the AI model
- [**Composer**](https://getcomposer.org/download/) — to install PHP dependencies (PHPMailer)
- [**Git**](https://git-scm.com/downloads) — to clone the repository (optional)

### Steps

**1. Clone the repository**
```bash
git clone https://github.com/yourusername/glucopredictor.git
```

**2. Set Up the Database**
- Open XAMPP Control Panel and start Apache & MySQL
- Go to `http://localhost/phpmyadmin`
- Create a new database named: `glucopredictor`
- Click on the new database → Go to the **Import** tab → Upload and execute `glucopredictor.sql`

**3. Configure Database Connection**

In any PHP files that connect to the database (e.g., `form.php`, `login.php`), ensure your credentials are correct:
```php
$conn = new mysqli("localhost", "root", "", "glucopredictor");
```
> If your MySQL password is not empty, update it accordingly.

**4. Install Composer Dependencies (PHPMailer)**
```bash
cd C:\xampp\htdocs\glucopredictor
composer require phpmailer/phpmailer
```
Make sure to include the Composer autoload in any file that uses PHPMailer:
```php
require 'vendor/autoload.php';
```

**5. Set Up the Python Environment (AI Model)**
```bash
cd C:\xampp\htdocs\glucopredictor\ml
pip install xgboost numpy
```
Make sure the following files are present in the `ml/` folder:
- `predict.py`
- `xgboost_diabetes_model.json`

---

## 📘 How to Use

- Register an account and activate it via email
- Login using your registered email and password
- Fill in the risk assessment form with the necessary details
- Get your risk calculated upon valid form submission
- View your personalized health tips based on your results
- Check your risk assessment history for past risk scores and levels
- Monitor your glucose, weight, and insulin intake using the tracking pages

---

## 👨‍💻 Author

**Jegathiswaran Thiaghu**

[![GitHub](https://img.shields.io/badge/GitHub-jega1312-181717?style=flat&logo=github)](https://github.com/jega1312)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-jegathiswaran--thiaghu-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/jegathiswaran-thiaghu/)
[![Portfolio](https://img.shields.io/badge/Portfolio-jega1312.github.io-0A66C2?style=flat)](https://jega1312.github.io/portfolio/)

---

## 📄 License

This project is open source and available under the MIT License ⚖️.
