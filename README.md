🌐 Business Website Deployment with CI/CD Automation (DevOps Project)
📌 Overview

This project demonstrates the design, automation, and deployment of a business website using a DevOps-inspired workflow. It integrates version control, Python-based automation, and CI/CD pipelines to streamline deployment and improve reliability.

The goal of this project is to simulate a real-world DevOps workflow by automating parts of the deployment process and maintaining a structured release pipeline using GitHub.

🚀 Live Demo

🔗 [View Website](https://vspourdecisions.com/)

🛠️ Tech Stack
Frontend: HTML, CSS, JavaScript
Scripting & Automation: Python
Version Control: Git & GitHub
CI/CD Pipeline: GitHub Actions
Hosting & Domain: Namecheap
Deployment: Automated + manual hybrid workflow
⚙️ Features
Responsive business website for desktop and mobile
Automated file preparation using Python scripting
CI/CD pipeline for automated build and deployment
Version-controlled development workflow
Custom domain configured through Namecheap
Streamlined deployment process with reduced manual steps
🧠 DevOps Concepts Applied
Version Control: Managed code changes using Git and GitHub
Automation: Python scripts used to automate build and deployment preparation
CI/CD: GitHub Actions pipeline triggers automated deployment on push
Continuous Integration: Code changes are validated through structured workflow
Continuous Deployment: Successful builds are automatically deployed to production
Environment Consistency: Standardized deployment process across updates
🐍 Python Automation Script Example

This script prepares the website files before deployment by organizing output files and ensuring a clean build directory.

import os
import shutil

SOURCE_DIR = "src"
BUILD_DIR = "dist"

def clean_build_directory():
    if os.path.exists(BUILD_DIR):
        shutil.rmtree(BUILD_DIR)
    os.makedirs(BUILD_DIR)

def copy_files():
    for root, dirs, files in os.walk(SOURCE_DIR):
        for file in files:
            if file.endswith((".html", ".css", ".js", ".png", ".jpg")):
                source_path = os.path.join(root, file)
                shutil.copy(source_path, BUILD_DIR)

def main():
    print("Starting build process...")
    clean_build_directory()
    copy_files()
    print("Build completed successfully.")

if __name__ == "__main__":
    main()
⚙️ CI/CD Pipeline (GitHub Actions)

This workflow automatically builds and deploys the website when changes are pushed to the main branch.

Create this file:

.github/workflows/deploy.yml
GitHub Actions Workflow:
name: Deploy Website

on:
  push:
    branches:
      - main

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Repository
        uses: actions/checkout@v3

      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: "3.10"

      - name: Run Build Script
        run: python build.py

      - name: Deploy to Server (Namecheap Hosting via FTP/SFTP)
        uses: SamKirkland/FTP-Deploy-Action@v4
        with:
          server: ${{ secrets.FTP_SERVER }}
          username: ${{ secrets.FTP_USERNAME }}
          password: ${{ secrets.FTP_PASSWORD }}
          local-dir: ./dist/
🔐 Secrets Configuration (GitHub)

To enable deployment securely, the following GitHub Secrets are required:

FTP_SERVER
FTP_USERNAME
FTP_PASSWORD

These are configured in:
GitHub Repository → Settings → Secrets → Actions

🔄 Deployment Workflow
Code is written and committed locally
Pushed to GitHub repository (main branch)
GitHub Actions pipeline automatically triggers
Python script builds and prepares deployment files
Files are deployed to Namecheap hosting via FTP
Live website is updated automatically
📂 Project Structure
/project-root
│── src/
│   ├── index.html
│   ├── css/
│   ├── js/
│   └── images/
│
│── build.py
│── dist/                # Generated build output
│── .github/
│   └── workflows/
│       └── deploy.yml
│
│── README.md
📈 Future Improvements
Add automated testing stage in CI pipeline
Migrate deployment to AWS S3 + CloudFront
Implement Terraform for infrastructure as code
Add monitoring and logging for uptime tracking
Containerize project using Docker
👩🏽‍💻 About Me

I am currently transitioning into DevOps Engineering through structured training and hands-on projects. My background in customer service and sales strengthens my communication, problem-solving, and user-focused mindset, which I now apply to technical systems and automation workflows.

📬 Contact
LinkedIn: (YOUR LINKEDIN URL)
Email: (YOUR EMAIL)
⭐ Key Takeaway

This project demonstrates a real-world DevOps workflow using Python automation, GitHub version control, and CI/CD pipelines, simulating how modern applications are built and deployed in production environments.
