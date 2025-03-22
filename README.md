# 🐾 Fawn – FTP Anonymous Access Exploitation

## 🎯 Objective
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

```bash
ping 10.129.114.167
### 🖼️ Ping Command Output
![Ping Screenshot](images/ping-result.png)
