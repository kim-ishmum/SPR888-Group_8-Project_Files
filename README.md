# SPR888-Group_8-Project_Files

This repository contains the configuration files and documentation for the SPR888 Group 8 project paper.

---

## Wazuh Manager

The configuration files for the **Wazuh Manager** are located in the `manager/` directory.

This includes:
* Custom decoders
* Local rules
* Other configuration (`.conf`) files

---

## Agent 1: LAMP Server (DVWA)

This agent is a **Damn Vulnerable Web Application (DVWA)** instance running on a standard **LAMP** stack (Linux, Apache, MySQL, PHP). While any generic LAMP server can be used, DVWA provides a simple environment for security testing.

* **DVWA Setup**: For installation instructions, please refer to the official guide: [https://github.com/digininja/DVWA](https://github.com/digininja/DVWA)
* **SSH Brute-Force Detection**: **OpenSSH** is also installed on this agent to test brute-force detection capabilities. You can install it using the following command:
    ```bash
    sudo apt install openssh-server openssh-client -y
    ```

---

## Agent 2: Amazon Linux

This agent is configured to perform several monitoring tasks. The relevant configuration files can be found in the `amazon/` directory.

* **File Integrity Monitoring**: Wazuh is configured to monitor a specific directory.
* **FTP Brute-Force Testing**: An FTP server is installed to test brute-force attack detection.
* **Database Monitoring**: MySQL is installed and monitored by Wazuh.

---

## Agent 3: Docker Host

This agent is configured to monitor **Docker containers**. Our specific configuration files are located in the `docker/` directory.

* **Setup Guide**: For a detailed guide on setting up Docker container monitoring with Wazuh, please follow the official tutorial: [Wazuh Blog: Docker Container Security Monitoring](https://wazuh.com/blog/docker-container-security-monitoring-with-wazuh/)

---

## Agent 4: Windows Workstation

This agent is a **Windows 11 Virtual Machine** set up to demonstrate vulnerability detection.

* **Scenario**: An outdated version of **VLC Media Player (v3.0.17.4)** is installed. The scenario involves detecting the known vulnerabilities and then verifying that they are resolved after updating the application.
* **Download Links for VLC v3.0.17.4**:
    * `https://get.videolan.org/vlc/3.0.17.4/win64/vlc-3.0.17.4-win64.msi`
    * `https://images.videolan.org/vlc/releases/3.0.17.html`
    * `https://www.linuxfromscratch.org/blfs/view/11.2-systemd/multimedia/vlc.html`
