# Server Engineering Practices

This repository contains the server engineering practices completed as part of the course requirements in **Computer Engineering** at the **University of Granada**. Each practice focuses on different server management tools and techniques, with instructions provided for each setup.

## Practice 3: RAID, Zabbix, and Ansible Setup

### 1. RAID Disk Monitoring and Reconstruction
- **Objective**: Identify, monitor, and reconstruct a RAID disk on Ubuntu.
- **Process**: 
  - Use `cat /proc/mdstat` to check RAID status.
  - Hot-unplug one disk to simulate a failure and verify it with `lsblk`.
  - Add a new disk and configure it with `fdisk`, install GRUB, and add the partitions to RAID with `mdadm`.

### 2. Zabbix Installation and Configuration
- **Objective**: Install and configure Zabbix on Ubuntu and Rocky Linux for monitoring SSH and HTTP.
- **Steps**:
  - Install Zabbix, MariaDB, and configure databases.
  - Configure `zabbix_server.conf`, `zabbix_agentd.conf`, and set up firewall ports.
  - Monitor HTTP and SSH by configuring host items in the Zabbix web interface.

### 3. Ansible Installation and Basic Command Execution
- **Objective**: Use Ansible to manage virtual machines.
- **Steps**:
  - Install Ansible and set up the `/etc/ansible/hosts` file.
  - Execute basic commands, such as `ls /home`, across all machines.
  - Run scripts like `mon-raid.py` on multiple machines.

### 4. Timer Service Activation
- **Objective**: Automate RAID monitoring with a timer service.
- **Steps**:
  - Configure `mon_raid.service` and `mon_raid.timer` in `/etc/systemd/system/`.
  - Start the timer with `systemctl start mon-raid.timer` and check status with `journalctl`.

---

## Practice 4: Phoronix and JMeter Benchmarking

### 1. Phoronix Benchmark on Ubuntu and Rocky
- **Objective**: Compare the performance of Ubuntu and Rocky Linux using Phoronix.
- **Steps**:
  - Install Phoronix on each system.
  - Run `pts/sudokut` and `pts/pybench` benchmarks to test system and CPU performance.
  - Results: Ubuntu displayed slightly faster processing times compared to Rocky.

### 2. JMeter Testing on Docker Containers
- **Objective**: Perform load testing on a web application deployed with Docker containers.
- **Steps**:
  - Set up Docker and Docker Compose to deploy the application.
  - Create a JMeter test plan with different thread groups for students and administrators.
  - Configure CSV data, random timers, and HTTP header managers for authentication and data retrieval.

---

## Requirements
- **Ubuntu** and **Rocky Linux** virtual machines
- **Zabbix**, **Ansible**, **Docker**, **JMeter**, and **Phoronix**

## Installation and Setup
Refer to each section above for detailed setup instructions, configurations, and troubleshooting tips.

---

## Troubleshooting
- **Zabbix**: Ensure MariaDB is correctly installed and configured before proceeding with Zabbix setup.
- **Ansible**: Use SSH key authentication between machines to avoid connection issues.
- **JMeter**: Verify Docker containers are running and accessible on the specified ports.

## References
- [Zabbix Documentation](https://www.zabbix.com/documentation)
- [Ansible Documentation](https://docs.ansible.com)
- [JMeter Documentation](https://jmeter.apache.org)
- [Phoronix Test Suite](https://www.phoronix-test-suite.com)

## Author
**Diego de Luis Ballesteros**  
[University of Granada]

If you wish to contribute to this project, feel free to fork the repository and submit a pull request with your improvements.

This project is licensed under the MIT License. See the LICENSE file for more details.
