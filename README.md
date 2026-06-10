# 🛡️ Insurance Policy Management System

<div align="center">

![Insurance Banner](https://img.shields.io/badge/Project-Insurance%20Policy%20Management-blue?style=for-the-badge&logo=shield&logoColor=white)

[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)](https://www.php.net/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)](https://www.selenium.dev/)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)

> A full-stack web application for managing insurance policies — built with PHP & MySQL on the backend, HTML/CSS on the frontend, and automated with Selenium for end-to-end testing.

</div>

---

## 📋 Table of Contents

- [About the Project](#-about-the-project)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Testing with Selenium](#-testing-with-selenium)
- [Screenshots](#-screenshots)
- [Test Cases](#-test-cases)
- [Contributors](#-contributors)

---

## 📖 About the Project

The **Insurance Policy Management System** is a web-based application that allows insurance companies to manage various types of policies and offer them to customers. Administrators can create, update, and categorize policies, while customers can browse, purchase, and manage their insurance coverage.

This project was developed as part of a **Software Testing** course — featuring a complete Selenium automation test suite covering all critical user flows.

---

## ✨ Features

### 👨‍💼 Admin Panel
- ➕ Add / Edit / Delete insurance policies
- 📂 Manage policy categories (Life, Health, Vehicle, Home, etc.)
- 👥 View registered customers and their active policies
- 📊 Dashboard with policy and customer statistics

### 👤 Customer Portal
- 🔐 Customer registration & login
- 🔍 Browse available insurance policies by category
- 📝 Apply for a policy online
- 📄 View and manage personal policy portfolio
- 🔄 Renew or cancel existing policies

### 🧪 Automated Testing
- Full end-to-end test coverage using **Selenium WebDriver**
- Tests written in **Python**
- Covers login, registration, policy CRUD, and customer workflows

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML5, CSS3 |
| Backend | PHP |
| Database | MySQL |
| Automation / Testing | Selenium WebDriver, Python |
| Server | Apache (XAMPP / WAMP) |

---

## 📁 Project Structure

```
insurance-policy-management/
│
├── customer/                  # Customer-facing portal
│   ├── index.php              # Customer home/login page
│   ├── register.php           # Customer registration
│   ├── dashboard.php          # Customer dashboard
│   ├── view_policies.php      # Browse available policies
│   └── my_policies.php        # Customer's active policies
│
├── insurance/                 # Admin panel
│   ├── index.php              # Admin login
│   ├── dashboard.php          # Admin dashboard
│   ├── add_policy.php         # Add new policy
│   ├── manage_policies.php    # View/Edit/Delete policies
│   └── manage_customers.php   # View all customers
│
├── insurancemanagement/       # Core backend logic & DB config
│   ├── db_connect.php         # Database connection
│   ├── config.php             # App configuration
│   └── ...                    # Shared utilities
│
├── selenium_tests/            # Selenium test scripts (Python)
│   ├── test_login.py
│   ├── test_registration.py
│   ├── test_add_policy.py
│   └── test_customer_flow.py
│
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- [XAMPP](https://www.apachefriends.org/) or [WAMP](https://www.wampserver.com/) (Apache + PHP + MySQL)
- [Python 3.x](https://www.python.org/)
- [Google Chrome](https://www.google.com/chrome/) + [ChromeDriver](https://chromedriver.chromium.org/)
- Selenium Python library

### 🔧 Installation

**1. Clone the repository**
```bash
git clone https://github.com/Hariom584/insurance-policy-management.git
cd insurance-policy-management
```

**2. Start XAMPP and place the project**
```bash
# Copy project to your XAMPP htdocs folder
cp -r insurance-policy-management /xampp/htdocs/
```

**3. Import the database**

- Open **phpMyAdmin** → `http://localhost/phpmyadmin`
- Create a new database: `insurance_db`
- Import the SQL file from the `insurancemanagement/` folder

**4. Configure the database connection**

Edit `insurancemanagement/db_connect.php`:
```php
$host     = "localhost";
$username = "root";
$password = "";          // your MySQL password
$database = "insurance_db";
```

**5. Run the application**

Open in your browser:
```
http://localhost/insurance-policy-management/insurance/index.php    ← Admin
http://localhost/insurance-policy-management/customer/index.php     ← Customer
```

---

## 🧪 Testing with Selenium

### Setup

**Install Python dependencies:**
```bash
pip install selenium
```

**Download ChromeDriver** matching your Chrome version from:
> https://chromedriver.chromium.org/downloads

Place `chromedriver.exe` in your system PATH or in the project root.

### Running Tests

```bash
# Run all tests
python -m pytest selenium_tests/

# Run a specific test
python selenium_tests/test_login.py
```

### Test Coverage

| Test Module | Description | Status |
|-------------|-------------|--------|
| `test_login.py` | Admin & customer login/logout | ✅ |
| `test_registration.py` | New customer registration form | ✅ |
| `test_add_policy.py` | Admin adds a new policy | ✅ |
| `test_edit_policy.py` | Admin edits existing policy | ✅ |
| `test_delete_policy.py` | Admin deletes a policy | ✅ |
| `test_customer_flow.py` | Customer browses & applies for policy | ✅ |
| `test_invalid_login.py` | Negative test: wrong credentials | ✅ |

---

## 📸 Screenshots

> *(Add screenshots of your project here by uploading images to the repo)*

| Admin Dashboard | Customer Portal | Policy List |
|:-:|:-:|:-:|
| ![Admin](https://via.placeholder.com/250x150?text=Admin+Dashboard) | ![Customer](https://via.placeholder.com/250x150?text=Customer+Portal) | ![Policies](https://via.placeholder.com/250x150?text=Policy+List) |

---

## 📝 Test Cases

### TC-01: Admin Login
| Field | Detail |
|-------|--------|
| **Test ID** | TC-01 |
| **Description** | Verify admin can log in with valid credentials |
| **Precondition** | Server is running, admin account exists |
| **Steps** | 1. Open admin login page<br>2. Enter valid username/password<br>3. Click Login |
| **Expected Result** | Redirected to admin dashboard |
| **Status** | ✅ Pass |

### TC-02: Add New Policy
| Field | Detail |
|-------|--------|
| **Test ID** | TC-02 |
| **Description** | Admin adds a new insurance policy |
| **Steps** | 1. Login as admin<br>2. Navigate to Add Policy<br>3. Fill in policy details<br>4. Submit form |
| **Expected Result** | Policy appears in policy list |
| **Status** | ✅ Pass |

### TC-03: Customer Registration
| Field | Detail |
|-------|--------|
| **Test ID** | TC-03 |
| **Description** | New customer registers successfully |
| **Steps** | 1. Open registration page<br>2. Fill all fields<br>3. Submit |
| **Expected Result** | Account created, redirected to login |
| **Status** | ✅ Pass |

### TC-04: Invalid Login (Negative Test)
| Field | Detail |
|-------|--------|
| **Test ID** | TC-04 |
| **Description** | Login fails with incorrect credentials |
| **Steps** | 1. Enter wrong password<br>2. Click Login |
| **Expected Result** | Error message displayed, no access granted |
| **Status** | ✅ Pass |

---

## 👨‍💻 Contributors

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/Hariom584">
        <img src="https://github.com/Hariom584.png" width="80px;" alt="Hariom"/><br/>
        <b>Hariom</b>
      </a>
      <br/>Developer & QA
    </td>
  </tr>
</table>

---

## 📄 License

This project is for educational purposes as part of a Software Testing curriculum.

---

<div align="center">

⭐ **If you found this project helpful, please give it a star!** ⭐

Made with ❤️ for Software Testing

</div>
