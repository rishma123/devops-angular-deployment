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

Developer Push → GitHub → GitHub Actions
│
├── Install & Build Angular App
├── Upload dist/ to S3 bucket
└── Invalidate CloudFront CDN cache
▼
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
dist/portfolio-final/browser/

🤖 CI/CD Pipeline

Pipeline file:

.github/workflows/deploy.yml
