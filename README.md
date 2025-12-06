# DevOps Deployment Pipeline for Angular Application

This project demonstrates a complete **DevOps pipeline** for building and deploying a static Angular application using:

- **GitHub Actions (CI/CD)**
- **AWS S3 (Static Hosting)**
- **AWS CloudFront (CDN)**
- **AWS IAM (Secure Deployment)**

It showcases real-world DevOps workflows including automated builds, cloud deployment, CDN caching, and secure secrets management.

---

## 🚀 Project Overview

This repository contains:

- A production-ready Angular application.
- A fully automated CI/CD pipeline.
- Deployment to AWS S3 with CloudFront global CDN.
- Automatic cache invalidation on every push to `main`.

This project demonstrates industry-standard cloud deployment practices.

---

## 🏗 Architecture

Developer Push → GitHub → GitHub Actions
│
├── Install & Build Angular App
├── Upload dist/ to S3 bucket
└── Invalidate CloudFront CDN cache
│
▼
Users access via CloudFront URL


---

## 🛠 Technologies Used

### DevOps & Cloud
- **AWS S3**
- **AWS CloudFront**
- **AWS IAM**
- **GitHub Actions**

### Frontend
- **Angular 17+**
- **CSS (Custom styling)**

### Tooling
- **Node.js 20**
- **Angular CLI**
- **NPM**

---

## 🔧 Run Locally

```bash
npm install
ng serve --open

Build for Production
ng build --configuration production


Output location:

dist/portfolio-final/browser/

🚀 CI/CD Pipeline

Pipeline file:

.github/workflows/deploy.yml

The workflow automatically:

Installs Node.js

Installs dependencies

Builds Angular

Deploys build files to AWS S3

Invalidates CloudFront cache

This ensures the website updates instantly worldwide.

🔐 GitHub Secrets Required
Secret Name	Purpose
AWS_ACCESS_KEY_ID	IAM access key
AWS_SECRET_ACCESS_KEY	IAM secret key
AWS_REGION	ex: eu-central-1
📦 Deployment Output

Your application becomes available globally through CloudFront, giving:

Ultra-fast load times

Global CDN caching

Automatic invalidation on deploy

CloudFront distributes your Angular app at a stable public URL.

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
 ├── main.ts
 └── index.html
