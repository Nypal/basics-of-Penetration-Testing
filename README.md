# 🐾 Fawn – FTP Anonymous Access Exploitation

## 🎯 Goal
Understand how to enumerate and exploit a misconfigured FTP service allowing anonymous access using basic tools.

## 🧭 Step 1: Targeting a Misconfigured FTP
We begin by identifying and connecting to a simple FTP server with anonymous access enabled. This is common in poorly secured internal systems.

### 🔧 Tools Required
- VPN connection (HTB lab)
- Terminal
- `ping`
- `ftp`
- `nmap`

### 🛠️ Initial Check – Is the Target Reachable?
Use `ping` to ensure the target is live: 

ping 10.129.114.167
### 🖼️ Ping Command Output
![image](https://github.com/Nypal/basics-of-Penetration-Testing/blob/2cbca40bfb063aaae389bfb6616efe511aa1d32e/ping-result.png)

### 🔎 Nmap Scan – Detecting Open Services

Use `nmap` to identify which services are running on the target:

sudo nmap 10.129.89.120
### 🖼️ Nmap Command Output
![Nmap Scan Result](https://github.com/Nypal/basics-of-Penetration-Testing/blob/fbfb27169ebdfdfa67907dadbd17b70bf31aacc8/nmapresult.png?raw=true)

### 🔍 Nmap Version Scan – Identifying Service Versions

We now run Nmap with the `-sV` flag to detect the **versions** of the services running on open ports. This helps determine if they are outdated or vulnerable.

sudo nmap -sV 10.129.89.120
![Nmap Scan Result](https://github.com/Nypal/basics-of-Penetration-Testing/blob/12a13efa3e29d3cb76a6e0a28d708bc508a0d9a2/vSnmapresult.png?raw=true)

