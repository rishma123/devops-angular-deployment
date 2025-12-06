# 🚀 DevOps Deployment Pipeline for Angular Application

This project demonstrates a complete **DevOps pipeline** for building and deploying a static Angular application using:

- **GitHub Actions (CI/CD)**
- **AWS S3 (Static Hosting)**
- **AWS CloudFront (CDN)**
- **AWS IAM (Secure Deployment)**

It showcases real-world DevOps workflows including automated builds, cloud deployment, CDN caching, and secure secrets management.

---

## 📌 Project Overview

This repository contains:

- A production-ready Angular application  
- A fully automated CI/CD pipeline  
- Deployment to AWS S3 with CloudFront global CDN  
- Automatic cache invalidation on every push to `main`  

This project demonstrates industry-standard DevOps and cloud deployment practices.

---

## 🏗 Architecture

Developer Push
      ↓
GitHub → GitHub Actions
      │
      ├── Install & Build Angular App
      ├── Upload dist/ to S3 bucket
      └── Invalidate CloudFront CDN cache
      ↓
Users access the application via CloudFront URL


---

## 🛠 Technologies Used

### DevOps & Cloud
- AWS S3  
- AWS CloudFront  
- AWS IAM  
- GitHub Actions  

### Frontend
- Angular 17  
- CSS  

### Tooling
- Node.js 20  
- Angular CLI  
- NPM  

---

## 🔧 Run Locally

### Install dependencies
```bash
npm install
Start development server
ng serve --open

Build for production
ng build --configuration production

Build output location
dist/devops-angular-deployment/browser/

🤖 CI/CD Pipeline

Pipeline file:

.github/workflows/deploy.yml

The CI/CD workflow automatically:

Installs Node.js

Installs dependencies

Builds Angular production files

Deploys the build output to AWS S3

Invalidates CloudFront CDN cache

This ensures the website updates instantly worldwide.

🔐 GitHub Secrets Required
Secret Name	Purpose
AWS_ACCESS_KEY_ID	IAM access key
AWS_SECRET_ACCESS_KEY	IAM secret key
AWS_REGION	Region (ex: eu-central-1)
🌍 Deployment Output

Your application is deployed globally via AWS CloudFront, providing:

Fast CDN delivery

Automatic caching + invalidation

A stable public CloudFront URL

🧩 Project Structure
src/
 ├── app/
 │    ├── app.html
 │    ├── app.css
 │    ├── app.ts
 │    ├── app.routes.ts
 │
 ├── assets/
 │    └── icons/
 │
 ├── styles.css
 ├── index.html
 └── main.ts

