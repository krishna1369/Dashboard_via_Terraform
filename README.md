# Observability as Code — Part 1 (Dashboards)

This repository contains Terraform examples and workflow steps for implementing **Observability as Code** with New Relic, based on the official New Relic guide:  
**“Automate your configuration with observability as code — Part One.”**

The goal is to automate the creation of **New Relic Dashboards** using Terraform so they can be consistently deployed, version-controlled, and reproduced across environments.

---

## 📌 Table of Contents

1. [Introduction](#introduction)  
2. [Prerequisites](#prerequisites)  
3. [Stage 1: Terraform Setup](#stage-1-terraform-setup)  
4. [Stage 2: Provision Sample Application](#stage-2-provision-sample-application)  
5. [Stage 3: Create Dashboard as Code](#stage-3-create-dashboard-as-code)  
6. [Stage 4: Apply Terraform](#stage-4-apply-terraform)  
7. [Stage 5: Cleanup](#stage-5-cleanup)  
8. [Next Steps](#next-steps)

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
- **Terraform 1.x**  
- **Git**  
- **Text/code editor**

### 🔹 Sample App (FoodMe)
New Relic uses a Glitch-hosted demo app to generate telemetry.

---

## 🚀 Stage 1: Terraform Setup

Create a directory structure:

