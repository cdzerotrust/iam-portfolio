# 🔐 Privileged Identity Management (PIM) Implementation – Microsoft Entra ID

## 📌 Overview

This lab demonstrates the implementation of **Privileged Identity Management (PIM)** in Microsoft Entra ID to enforce:

* Least privilege access
* Just-In-Time (JIT) role activation
* Privileged access governance

---

## 🎯 Objectives

* Configure eligible role assignments
* Enable Just-In-Time (JIT) access
* Reduce standing privileges
* Implement approval-based role activation
* Track and audit privileged access

---

## 🏗️ Environment

* Microsoft Entra ID (P2 License)
* Test User: Chris Davis
* Role: User Administrator

---

## ⚙️ Implementation Steps

### 1. Navigate to PIM

Accessed via:
**Microsoft Entra Admin Center → Identity Governance → Privileged Identity Management**

![Navigate to PIM](./pim-01-navigation-to-pim.png)

---

### 2. Select Role – User Administrator

Chose the **User Administrator** role for controlled identity management operations.

![Select Role](./pim-02-role-selection-user-admin.png)

---

### 3. Assign Eligible Role

Configured role as **Eligible** instead of permanently active:

* Assignment Type: Eligible
* Scope: Directory

This removes standing administrative access.

![Add Assignment](./pim-03-add-assignment.png)

---

### 4. Configure Role Settings (Security Controls)

Implemented governance controls:

* Require **Azure MFA**
* Require **justification on activation**
* Require **approval to activate**
* Configure **activation duration limits**

![Role Settings](./pim-05-edit-role-settings.png)

---

### 5. Activate Role (Just-In-Time Access)

Performed JIT activation:

* Navigated to **My Roles**
* Selected **User Administrator**
* Submitted activation request

![Activation](./pim-07-role-activation-success.png)

---

### 6. Validate Active Role

Confirmed role transitioned from **Eligible → Active** with time-bound access.

![Active Assignment](./pim-08-active-assignments.png)

---

## 🔍 Key Security Benefits

* Eliminates **permanent administrative access**
* Reduces **attack surface**
* Enforces **Zero Trust principles**
* Enables **audit and compliance tracking**
* Prevents **privilege creep**

---

## ⚠️ Lessons Learned

* Approval workflows can block activation if misconfigured
* Activation duration must align with policy limits
* Global Administrator roles must be tightly controlled
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

Chris Davis
Cloud Security Engineer | IAM | Zero Trust
