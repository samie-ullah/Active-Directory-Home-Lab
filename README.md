
# 🖥️ Active Directory Home Lab (Windows Server)


## 📌 Overview
This project showcases a hands-on Active Directory lab built using Windows Server, simulating a real-world enterprise environment with user management, file sharing, and Group Policy deployment.


---

## 🧱 Lab Environment

## 🛠️ Technologies Used
- Windows Server
- Active Directory (AD DS)
- Group Policy (GPO)
- NTFS Permissions
- VirtualBox

---

## ⚙️ What I Built

### ✅ Active Directory Structure
- Organisational Units:
  - HR
  - IT
  - Finance

---

---

## 🔐 Part 2: Security, Monitoring & Alerting

This phase of the lab focused on securing user accounts, monitoring authentication activity, and responding to security events in a simulated enterprise environment.

### ✅ Security Policies Implemented
- Configured domain-level password policies (complexity, expiry, history)
- Implemented account lockout policy after multiple failed login attempts
- Enforced password change at next logon following administrative resets

### ✅ Monitoring & Investigation
- Used Windows Event Viewer to analyse authentication events:
  - Event ID 4625 – Failed logon attempts
  - Event ID 4740 – Account lockout events
- Identified source machines using the “Caller Computer Name” field
- Investigated user lockouts and authentication failures

### ✅ Event-Based Alerting
- Created an event-triggered task using Task Scheduler
- Automatically executed an action when an account lockout (Event ID 4740) occurred
- Verified alert execution during simulated security incidents

### ✅ User Account Lifecycle (Tested)
- User account lockout after failed logins
- Administrator investigation via security logs
- Manual account unlock
- Password reset with “change at next logon” enforced
- Successful user re-authentication


### ✅ User & Group Management
- Created users for each department
- Implemented Role-Based Access Control (RBAC) using:
  - HR_Users
  - IT_Users
  - Finance_Users

---

### ✅ File Server Setup

- Created shared folders:
  - `\\DC01\HR`
  - `\\DC01\IT`
  - `\\DC01\Finance`

- Configured:
  - NTFS permissions
  - Share permissions

---

### ✅ Group Policy (GPO)
- Automated drive mapping:
  - H: → HR
  - I: → IT
  - F: → Finance
- Implemented user restrictions:
  - Disabled Control Panel
  - Blocked Command Prompt

---

## 🧠 Key Challenges & Troubleshooting

- GPO not applying due to:
  - Incorrect UNC path formatting
  - Logging into Administrator instead of a domain user
  - Security filtering issues ("Filtered Out")

- Used tools like:
  - `gpresult /r`
  - Group Policy Management Console (GPMC)

---

## ✅ Final Outcome

- Fully functional AD environment
- Department-specific access control
- Automated drive mapping via GPO
- Security restrictions applied successfully

---

## 📸 Screenshots


## 📸 Screenshots

### 🔹 GPO Structure
images/gpo.png

### 🔹 Drive Mapping
images/drives.png

### 🔹 User Restrictions
images/restrictions.png

---

## 🚀 Next Steps
- Expand into Azure AD / Hybrid Identity

---

## 💡 Skills Demonstrated
- Active Directory Administration
- Group Policy Management (GPO)
- Windows Server
- Troubleshooting & Problem Solving

## 🔗 Access Model

User → Security Group → File Share → GPO Policy

