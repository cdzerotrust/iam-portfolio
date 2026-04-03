# iam-portfolio
Identity and Access Management (IAM) hands-on labs and security implementations
# 🔐 Privileged Identity Management (PIM) Implementation – Microsoft Entra ID

## 📌 Overview

This lab demonstrates the implementation of **Privileged Identity Management (PIM)** in Microsoft Entra ID to enforce **least privilege access**, **Just-in-Time (JIT) role activation**, and **privileged access governance**.

---

## 🎯 Objectives

* Configure eligible role assignments
* Enable Just-in-Time (JIT) access
* Reduce standing privileges
* Implement approval-based role activation
* Track and audit privileged access

---

## 🏗️ Environment

* **Platform:** Microsoft Entra ID (P2 License)
* **Test User:** Chris Davis
* **Role:** User Administrator

---

## ⚙️ Implementation Steps

### 1. Navigate to PIM

Accessed Privileged Identity Management through the Entra admin center.

![PIM Navigation](./images/pim-01-navigation-to-pim.png)

---

### 2. Select Role for Management

Navigated to roles and selected **User Administrator** for configuration.

![Role Selection](./images/pim-02-role-selection-user-admin.png)

---

### 3. Assign Eligible Role

Configured the role assignment as **Eligible** to enforce Just-in-Time access.

* Assignment Type: Eligible
* Scope: Directory
* Assigned to test user

![Add Assignment](./images/pim-03-add-assignment-screen.png)

---

### 4. Configure Role Settings (Governance Controls)

Applied governance controls to enforce secure access:

* Activation duration set to **1 hour**
* **Azure MFA required**
* **Justification required**
* **Approval required**
* Assigned approver

![Role Settings Configuration](./images/pim-05-edit-role-settings-governance-controls.png)

---

### 5. Activate Role (Just-in-Time Access)

Initiated activation of the eligible role.

* Navigated to **My Roles**
* Selected **User Administrator**
* Clicked **Activate**

![Activation Request](./images/pim-07-role-activation-request.png)

---

### 6. Activation Successful

Validated that the role activation completed successfully.

* Request processed
* Activation validated
* Role transitioned to **Active**

![Activation Success](./images/pim-08-role-activation-success.png)

---

### 7. Validate Active Role Assignment

Confirmed the role is now active and time-bound.

![Active Role Validation](./images/pim-09-active-role-validation.png)

---

## 🔍 Key Security Benefits

* Eliminates permanent administrative access
* Reduces attack surface
* Enforces Zero Trust principles
* Enables auditing and monitoring
* Prevents privilege creep

---

## ⚠️ Lessons Learned

* Approval workflows must be configured correctly to avoid blocking access
* Time-bound assignments must align with policy limits
* Overuse of Global Administrator roles increases risk
* Always maintain a **break-glass account**

---

## 🧠 Real-World Application

In enterprise environments, PIM is used to:

* Enforce least privilege access
* Provide temporary elevated access
* Meet compliance requirements (SOC 2, ISO 27001, NIST)
* Monitor privileged account activity

--- 

## 📎 Author

**Chris Davis**
Cloud Security Engineer | IAM | Zero Trust
