# Certificate-Based-Authentication-easyrsa-OpenVPN-Setup-on-Ubuntu-EC2

Here is a **professional README.md** file for your repository 👇
(You can copy & paste into GitHub)

---

# Certificate-Based Authentication & OpenVPN Setup on Ubuntu EC2

This repository contains two presentation files that explain how to configure **certificate-based authentication using Easy-RSA** and how to **configure an OpenVPN server on Ubuntu EC2**.

## 📁 Files Included

| File Name                                                                         | Description                                                                                                                                                 |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Certificate-Based Authentication using Easy-RSA on Ubuntu EC2.pptx**            | Explains how to generate certificates using Easy-RSA on an Ubuntu EC2 instance. Includes CA, server, client certificates, DH parameters, CRL, and commands. |
| **Configuring OpenVPN Server on Ubuntu EC2 with Certificate Authentication.pptx** | Step-by-step OpenVPN server setup, firewall rules, TA key, server configuration, and client connection.                                                     |

---

## 🛡️ What is Certificate-Based Authentication?

Certificate-based authentication uses **digital certificates** to verify identity instead of passwords.

### Why it is used:

✔ Secure VPN connections
✔ Stronger than passwords
✔ Prevent unauthorised access
✔ Uses PKI (Public Key Infrastructure)

---

## ⚙️ Key Components

* **CA (Certificate Authority)**
* **Server certificate**
* **Client certificate**
* **Private key**
* **Public certificate**
* **CRL (Certificate Revocation List)**
* **DH parameters (dh.pem)**
* **TLS auth key (ta.key)**

---

## 🧩 Tools Used

* **Ubuntu EC2 Instance**
* **OpenVPN**
* **Easy-RSA**
* **PuTTY / EC2 Instance Connect**
* **WinSCP (to download certificates)**
* **Firewall (UFW)**

---

## 🚀 Process Overview

### 🔑 Phase 1: Certificate Generation using Easy-RSA

1. Create and connect to EC2
2. Install OpenVPN and Easy-RSA
3. Initialize PKI
4. Build CA
5. Generate server & client certificates
6. Generate **dh.pem**
7. Download certificates using **WinSCP**

---

### 🌐 Phase 2: Configure OpenVPN Server

Steps include:

* Generate `ta.key`
* Create `server.conf`
* Enable IP forwarding
* Configure `iptables`
* Allow port `1194/udp`
* Start OpenVPN service

---

### 👨‍💻 Client Configuration

* Install OpenVPN Client
* Create `.ovpn` profile
* Add:

  * `ca.crt`
  * `client.crt`
  * `client.key`
  * `ta.key`
  * `dh.pem`
* Import profile and **Connect**

---

## 🖥️ Testing VPN

Verify connection using:

* [https://whatismyipaddress.com/](https://whatismyipaddress.com/)

If IP location changes → **VPN works correctly**

---

## ⚠️ Important Note

If the EC2 instance is deleted **before saving certificates**, they are **lost permanently**.

> Always copy all certificate files to your system using **WinSCP**.

---

## 📎 License

This project is created for **learning and demonstration** purposes.
Feel free to use, modify, and share.

---

## 🙌 Prepared By

**Parashurama**

---
