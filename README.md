# 🧩 Ansible MySQL Server Deployment

Ansible-based automation for installing, configuring, and managing a **MySQL server** on one or more Linux nodes.  
This project simplifies the setup of a secure and production-ready MySQL instance with reusable **Ansible roles**.

---

## 📘 Table of Contents
- [Overview](#overview)
- [Design & Architecture](#design--architecture)
- [Prerequisites](#prerequisites)
- [Repository Structure](#repository-structure)
- [Usage](#usage)
- [Configuration Variables](#configuration-variables)
- [Testing & Validation](#testing--validation)
- [License](#license)
- [Contributing](#contributing)
- [Contact](#contact)

---

## 🚀 Overview

This repository contains:
- A **reusable Ansible role** for MySQL installation and configuration.
- A **playbook** (`mysql_setup.yml`) that applies the role to target nodes.
- An **inventory file** (`nodes.ini`) to define managed hosts.

✅ **Features**
- Automated MySQL installation  
- Secure root password setup  
- User and database creation  
- Configuration templating with Jinja2 (`my.cnf.j2`)  
- Service management (start/enable)  
- Fully idempotent tasks  

---

## 🧱 Design & Architecture

### Architecture Diagram
```text
+-------------------+           +------------------------+
|   Control Node    |  SSH →    |     Managed Node(s)    |
|  (Ansible host)   | --------> |  MySQL installation     |
| ansible-playbook  |           |  Configuration + Start  |
+-------------------+           +------------------------+
