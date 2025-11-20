# Observability as Code — Dashboards/Alerts

This repository contains Terraform and workflow stage for implementing **Observability as Code** with New Relic:  
**“Automate your configuration with observability as code.”**

The goal is to automate the creation of **New Relic Dashboards** using Terraform so they can be consistently deployed, version-controlled, and reproduced across environments.

---

## 📌 Table of Contents

1. [Introduction](#introduction)  
2. [Prerequisites](#prerequisites)  
3. [Stage 1 Terraform Setup](#stage-1-terraform-setup)  
4. [Stage 2 Provision Sample Entity](#stage-2-provision-sample-entity)  
5. [Stage 3 Apply Terraform](#stage-3-apply-terraform)  
6. [Stage 4 Validate Dashboard](#stage-4-validate-dashboard)  
7. [Stage 5 Version Control](#stage-5-version-control)



---

## 📘 Introduction

**Observability as Code** allows you to automate the configuration of dashboards, alerts, monitors, and more using code.  
This brings the same advantages as Infrastructure as Code:

- Repeatability  
- Version control  
- Consistency across teams  
- Git-based collaboration  
- Zero manual UI configuration

This guide focuses on creating **New Relic dashboards via Terraform**.

---

## 🧩 Prerequisites

Before beginning, you must have:

### 🔹 New Relic Account
You need the following values:

- **ACCOUNT ID**  
- **USER API KEY** (starts with `NRAK-...`)  
- **REGION** (US or EU)

### 🔹 Installed Tools
- **Terraform**  
- **Git**  
- **Text/code editor**
  
---

## 💼 Stage 1: Terraform Setup

This directory contains Terraform configuration to deploy a New Relic dashboard using JSON definitions.

## Files

| File | Purpose |
|------|---------|
| **main.tf** | Terraform config + loads dashboard.json |
| **provider.tf** | Provider configuration (account ID, API key, region) |
| **variables.tf** | Terraform input variables |
| **dash_basic.tf** | Dashboard resource definition |
| **dashboard.json** | JSON dashboard definition |

---

## 📝 Stage 2: Provision Sample Entity

Here we are using Synthetic script as an entity for creating Synthetic dashbaord.

---

## 🚀 Stage 3: Apply Terraform


### Terraform Commands

#### **1️⃣ Initialize Terraform**

Initializes the working directory.

```bash
terraform init
```
---
#### **2️⃣ Preview the Execution Plan**

Generates an execution plan so you can preview Terraform’s changes.

```bash
terraform plan
```
---
#### **3️⃣ Apply Changes**

Creates or updates resources based on your Terraform files.

```bash
terraform apply
```
---
Terraform will show the execution plan and prompt you to continue.

To proceed, type:

```bash
yes
```
---
#### **4️⃣ Destroy Resources**

Destroys the resources managed by this Terraform configuration.

```bash
terraform destroy
```

To confirm destruction, type:

```bash
yes
```

---

## 📊 Stage 4: Validate Dashboard

Log in to New Relic and confirm that the dashboard appears in your dashboard list.

---

## 🔄 Stage 5: Version Control

Below is a clean, ready-to-use **Version Control section** for your *Observability as Code using New Relic* project.
It includes the essential **Git commands**.

---

### **1️⃣ Initialize a Git Repository**

Create a new Git repository in your project directory.

```bash
git init
```
---
### **2️⃣ Add All Project Files**

Stage your Terraform files, dashboard file, and docs.

```bash
git add .
```
---
### **3️⃣ Commit Your Changes**

Create your first commit with a helpful message.

```bash
git commit -m "Observability as Code"
```
---
### **4️⃣ Add Remote Repository**

Connect local project to a Git hosting service like GitHub, GitLab, or Azure repo.

```bash
git remote add origin https://github.com/your-username/your-repo-name.git
```
---
### **5️⃣ Push to the Remote Repository**

Push local commits to the remote `main` branch.

```bash
git push -u origin main
```

---
