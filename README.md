# 🚀 Tomcat + Ansible + Vagrant Setup

This project provisions a virtual machine using **Vagrant** and **Ansible** to automatically install:

- ☕ Java (OpenJDK 11)
- 🐱 Apache Tomcat 9
- 🔁 NGINX as a reverse proxy (optional)
- ⚙️ Runs on Ubuntu 22.04 with 2GB RAM

## 🛠️ What it does

- Provisions Ubuntu 22.04 with 2GB RAM using Vagrant.
- Installs Java and deploys Apache Tomcat.
- Tomcat is managed as a systemd service.
- Tomcat port is changed to **7575**.
- Port **8080 (guest)** is forwarded to **9090 (host)**.

## 📂 Files

- `Vagrantfile` – defines the VM and Ansible provisioning.
- `playbook.yml` – installs Java, Tomcat, and configures the service.

## 🚀 Usage

```bash
git clone https://github.com/mr3bd/tomcat-ansible-vagrant-setup.git
cd tomcat-ansible-vagrant-setup
vagrant up
```

##  Access

[http://localhost:9090](http://localhost:9090)


## 📌 Notes:
- You can optionally add NGINX and configure it to reverse proxy to Tomcat.
- The Tomcat service runs on port 7575 internally.

----

## 👨‍💻 Author

[Abdullrahman Wasfi](https://www.linkedin.com/in/abdullrahmanwasfi)