
# 🖥️ Active Directory Home Lab (Windows Server)

## 📌 Overview
This project demonstrates the setup and configuration of a Windows Server Active Directory environment with real-world system administration tasks, including user management, file sharing, and Group Policy (GPO).

---

## 🧱 Lab Environment
- Windows Server (Domain Controller)
- Windows 11 Client Machine
- VirtualBox for virtualization

---

## ⚙️ What I Built

### ✅ Active Directory Structure
- Organisational Units:
  - HR
  - IT
  - Finance

---

### ✅ User & Group Management
- Created users for each department
- Implemented Role-Based Access Control (RBAC) using:
  - HR_Users
  - IT_Users
  - Finance_Users

---

### ✅ File Server Setup
- Created shared folders:
  - \\DC01\HR
  - \\DC01\IT
  - \\DC01\Finance
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

(Add your 3 screenshots here)

---

## 🚀 Next Steps
- Implement account lockout policies
- Configure password policies
- Expand into Azure AD / Hybrid Identity

---

## 💡 Skills Demonstrated
- Active Directory Administration
- Group Policy Management (GPO)
- Windows Server
- Troubleshooting & Problem Solving

