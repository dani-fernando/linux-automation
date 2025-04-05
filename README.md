# **Linux Automation Project**

Welcome to the **Linux Automation Project**! 🌟 This repository contains automation scripts and tools designed to streamline server provisioning, configuration management, and deployment tasks for both Linux and systems. Whether you're managing a single server or an entire infrastructure, this project aims to make your life as a sysadmin easier.

---
![Linux Automation](https://raw.githubusercontent.com/dani-fernando/linux-automation/refs/heads/main/image/home.jpg)   

## **Table of Contents**
1. [Overview](#overview)
2. [Features](#features)
3. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Installation](#installation)
4. [Usage](#usage)
5. [Contributing](#contributing)
6. [License](#license)

---

## **Overview**
This project provides automation scripts and playbooks to simplify common sysadmin tasks such as:
- Server provisioning
- Configuration management
- Backup automation
- Monitoring setup

The tools used in this project include:
- **Ansible** for configuration management
- **Shell scripting** for lightweight automation
- **Terraform** for infrastructure provisioning (optional)

---

## **Features**
✅ Automate server setup for both Linux  
✅ Provision VMs/containers with ease  
✅ Deploy services like Nginx, Apache, and more  
✅ Backup automation with `rsync` and `cron`  
✅ Monitor system resources with custom scripts  

---

## **Getting Started**

### **Prerequisites**
Before you begin, ensure you have the following installed on your system:
- **Python 3.x** (for Ansible)
- **Ansible** (`pip install ansible`)
- **SSH access** to target servers
- **Git** (to clone this repository)

### **Installation**
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/dani-fernando/linux-automation.git
   cd linux-automation
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure SSH Access**:
   Ensure your SSH key is added to the target servers for passwordless login. You can add your public key to the `~/.ssh/authorized_keys` file on each server.

4. **Customize Inventory**:
   Edit the `inventory.yml` file to include the IP addresses or hostnames of your target servers:
   ```yaml
   all:
     hosts:
       server1:
         ansible_host: 192.168.1.10
       server2:
         ansible_host: 192.168.1.11
   ```

---

## **Usage**

### **1. Run Ansible Playbooks**
To automate server setup using Ansible:
```bash
ansible-playbook -i inventory.yml playbooks/setup-server.yml
```

### **2. Automate Backups**
Run the backup script manually or schedule it via `cron`:
```bash
./scripts/backup.sh
```

To schedule daily backups, add the following to your crontab:
```bash
0 2 * * * /path/to/scripts/backup.sh
```

### **3. Monitor Resources**
Run the monitoring script to check CPU usage:
```bash
./scripts/monitor-cpu.sh
```

---

## **Contributing**
We welcome contributions from the community! Here's how you can help:
1. Fork the repository.
2. Create a new branch for your feature/fix:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add feature/fix description"
   ```
4. Push to your fork:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request on GitHub.

Please ensure your code follows best practices and includes appropriate documentation.

---

## **License**
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## **Contact**
If you have any questions or need further assistance, feel free to reach out:
- Email: hello@danifernando.com
- GitHub: [Dani Fernando](https://github.com/dani-fernando)

Happy automation 🤖✨

---
