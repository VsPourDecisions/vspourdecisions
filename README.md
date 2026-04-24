👉 `https://ywill77.github.io/vspourdecisions/`

# 🌐 VS Pour Decisions – Website Deployment Project

## 📌 Overview

This project is a personal business website deployed using a DevOps-style workflow. It demonstrates my ability to build, manage, and deploy a static website using **version control, automation concepts, and production hosting via GitHub Pages**.

The project reflects my ongoing transition into **DevOps Engineering**, focusing on practical deployment workflows, automation thinking, and infrastructure fundamentals.

---

## 🚀 Live Website

🔗 [https://ywill77.github.io/vspourdecisions/](https://ywill77.github.io/vspourdecisions/)

---

## 🛠️ Tech Stack

* **Frontend:** HTML, CSS, JavaScript
* **Hosting & Deployment:** GitHub Pages
* **Version Control:** GitHub
* **Automation / Scripting:** Python (workflow automation support concepts)
* **CI/CD Concept:** Git-based deployment pipeline (Git push → automatic deployment)

---

## ⚙️ Features

* Fully responsive business website
* Live deployment through GitHub Pages
* Custom branding and business content integration
* Structured repository for maintainability
* Git-based version control workflow
* Fast global access via static hosting

---

## 🧠 DevOps Concepts Applied

Although this is a static site project, it demonstrates foundational **DevOps practices**:

* **Version Control:** Managed using Git and GitHub
* **Continuous Deployment (CD):** Automatic deployment via GitHub Pages on push to main branch
* **Automation Thinking:** Python scripting used for workflow optimization concepts (file handling / deployment preparation mindset)
* **Environment Consistency:** Same codebase deployed from repository to production
* **Infrastructure Awareness:** Understanding of static hosting vs dynamic infrastructure

---

## 🐍 Python Automation Concept (Workflow Support Example)

This script represents how I approach automation for deployment preparation (file validation + build readiness):

```python id="vsp-build-script"
import os

SITE_DIR = "site"

def validate_files():
    required_files = ["index.html", "style.css"]
    
    print("Validating project structure...")
    
    for file in required_files:
        file_path = os.path.join(SITE_DIR, file)
        if not os.path.exists(file_path):
            raise FileNotFoundError(f"Missing required file: {file}")
    
    print("All required files are present. Ready for deployment.")

def main():
    validate_files()
    print("Build check completed successfully.")

if __name__ == "__main__":
    main()
```

---

## 🔄 Deployment Workflow

1. Develop website locally
2. Commit changes using Git
3. Push updates to GitHub repository
4. GitHub Pages automatically deploys latest version
5. Live site updates within seconds

---

## 📂 Project Structure

```id="vsp-structure"
/vspourdecisions
│── index.html
│── style.css
│── script.js
│── /images
│── README.md
```

---

## 📈 Future Improvements

* Add full CI/CD pipeline using GitHub Actions
* Expand Python automation into real build/deploy scripting
* Migrate to AWS S3 + CloudFront for enterprise-level architecture
* Add backend functionality (contact form automation)
* Implement logging/analytics tracking

---

## 👩🏽‍💻 About Me

I am currently transitioning into **DevOps Engineering** through structured coursework and hands-on projects. My background in Mortgage Underwriting, Risk and sales strengthens my communication, problem-solving, and user-focused approach, which I now apply to technical systems and automation workflows.

---

## 📬 Contact

* LinkedIn: www.linkedin.com/in/yvonda-davis
* Email: Notaree26@yahoo.com

---
## ⭐ Key Takeaway

This project demonstrates my ability to deploy and manage a live production website using GitHub-based workflows while applying foundational DevOps principles such as version control, automation thinking, and continuous deployment.

---
