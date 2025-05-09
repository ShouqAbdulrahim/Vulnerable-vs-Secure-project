# 🔒 Vulnerable vs Secure Flask App

Hi there 👋 This project showcases a **simple Flask web application** designed to demonstrate **common security vulnerabilities** and how to fix them 🔧.

---

## 💡 Project Idea

The app is a basic user registration & login system that includes:

- User Registration (Sign Up)
- User Login
- User Dashboard (to post comments)
- Admin Dashboard (for admin users)

⚠️ **Version 1 (`app.zip`) contains vulnerabilities** such as:

- SQL Injection 💉
- XSS (Cross-Site Scripting) 💥
- Access Control
- Weak password storage using MD5
- Encryption of Sensitive Data

✅ **Version 2 (`app-fixed.zip`) includes security improvements:**

---

## 🔐 Security Enhancements Implemented

- **SQL Injection Mitigation:**  
  Converted raw SQL queries into **parameterized queries** to prevent injection attacks.

- **Weak Password Storage Fix:**  
  Migrated from insecure MD5 hashing to **Werkzeug’s secure password hashing** with salt.

- **XSS Prevention:**  
  Sanitized user input using **Jinja2’s escaping** and ensured no unsafe rendering.

- **Access Control Implementation:**  
  Added session-based **role validation** to restrict access to sensitive routes (e.g., admin page).

- **Encryption of Sensitive Data:**  
  The secure version enforces **HTTPS (SSL/TLS)** with self-signed certificates (`cert.pem` & `key.pem`).

---

## 🗂️ Files Included

| File                   | Description                                      |
|------------------------|--------------------------------------------------|
| `app.zip`              | Vulnerable version of the Flask app             |
| `app-fixed.zip`        | Secure version with vulnerabilities patched     |

---

## 🚀 How to Run

1️⃣ **Download and extract the files:**

```bash
unzip app.zip
unzip app-fixed.zip
2️⃣ Navigate to the project folder:
cd app
# or for the secure version:
cd app-fixed/app
3️⃣ Create & activate the virtual environment:
python3 -m venv venv
source venv/bin/activate
4️⃣ Install dependencies:
pip install flask werkzeug
```

## 🛠️ Running the App
	•	For the vulnerable version (HTTP):
       python3 vulnerable.py
	•	For the secure version (HTTPS):
       python3 app.py
    # It will run at https://localhost:5001

---
✅ Notes

     	
    •	Test the vulnerabilities in the vulnerable version to see the risks in action, then switch to the secure version to verify that they are patched 🔒.
      
  	•	The secure app uses self-signed SSL certificates, so expect your browser to show a warning when you visit it locally.
 ---
