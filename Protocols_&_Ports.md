# **📡 Protocols & Ports — Ultimate Short & Memorable Guide**

*A clean, sharp, lifetime-memory cheat sheet. Easy to expand.*

---

# 🔥 **EMAIL PROTOCOLS**

## **SMTP — Sending Email**

| Port                                        | Encryption | Purpose                 |
| ------------------------------------------- | ---------- | ----------------------- |
| **25**                                      | None       | Server relay            |
| **587**                                     | STARTTLS   | Secure email submission |
| **465**                                     | TLS        | Secure submit (SMTPS)   |
| **Memory:** 25-old, 587-modern, 465-locked. |            |                         |

## **POP3 — Retrieving Email (Download)**

| Port                                         | Encryption | Purpose             |
| -------------------------------------------- | ---------- | ------------------- |
| **110**                                      | None       | Retrieve emails     |
| **995**                                      | TLS        | Secure POP3 (POP3S) |
| **Memory:** POP starts at 110 → 995 secured. |            |                     |

## **IMAP — Retrieving Email (Sync)**

| Port                                 | Encryption | Purpose   |
| ------------------------------------ | ---------- | --------- |
| **143**                              | None       | IMAP sync |
| **993**                              | TLS        | IMAPS     |
| **Memory:** IMAP: 143 → 993 secured. |            |           |

---

# 🌐 **WEB PROTOCOLS**

## **HTTP — Web Browsing**

| Port                            | Purpose            |
| ------------------------------- | ------------------ |
| **80**                          | Normal web traffic |
| **Memory:** 80 = *default web*. |                    |

## **HTTPS — Secure Web**

| Port                            | Purpose               |
| ------------------------------- | --------------------- |
| **443**                         | Encrypted web traffic |
| **Memory:** 443 = *locked web*. |                       |

---

# 🔐 **REMOTE ACCESS / AUTH**

## **SSH — Secure Remote Login**

| Port                                 | Purpose      |
| ------------------------------------ | ------------ |
| **22**                               | Secure shell |
| **Memory:** 22 = login to "two-two". |              |

## **Telnet — Insecure Remote Login**

| Port                                                | Purpose               |
| --------------------------------------------------- | --------------------- |
| **23**                                              | Insecure remote shell |
| **Memory:** 23 right after SSH, but **not secure**. |                       |

## **RDP — Windows Remote Desktop**

| Port                                         | Purpose            |
| -------------------------------------------- | ------------------ |
| **3389**                                     | Remote Windows GUI |
| **Memory:** 3389 looks like *three screens*. |                    |

---

# 🗂️ **FILE TRANSFER PROTOCOLS**

## **FTP — Insecure File Transfer**

| Port                            | Purpose  |
| ------------------------------- | -------- |
| **21**                          | Commands |
| **20**                          | Data     |
| **Memory:** 21 talks, 20 walks. |          |

## **FTPS — FTP over SSL**

| Port    | Purpose    |
| ------- | ---------- |
| **990** | Secure FTP |

## **SFTP — SSH File Transfer**

| Port                     | Purpose               |
| ------------------------ | --------------------- |
| **22**                   | File transfer via SSH |
| **Memory:** Same as SSH. |                       |

## **TFTP — Trivial File Transfer**

| Port                               | Purpose                   |
| ---------------------------------- | ------------------------- |
| **69**                             | Simple, insecure transfer |
| **Memory:** 69 is small & trivial. |                           |

---

# 🌍 **NETWORK FOUNDATION PROTOCOLS**

## **DNS — Domain Name System**

| Port                                | Purpose               |
| ----------------------------------- | --------------------- |
| **53**                              | DNS queries (TCP/UDP) |
| **Memory:** 5-3 = letters in "DNS". |                       |

## **DHCP — Dynamic IP Assignment**

| Port                                                | Purpose       |
| --------------------------------------------------- | ------------- |
| **67/68**                                           | IP assignment |
| **Memory:** Router talks on 67 → client replies 68. |               |

## **NTP — Time Sync**

| Port                      | Purpose   |
| ------------------------- | --------- |
| **123**                   | Time sync |
| **Memory:** 1–2–3 → time. |           |

---

# 🖥️ **FILE SHARING / DIRECTORY SERVICES**

## **SMB — Windows File Sharing**

| Port                                     | Purpose          |
| ---------------------------------------- | ---------------- |
| **445**                                  | SMB file sharing |
| **Memory:** Windows 445 = *files alive*. |                  |

## **NFS — Network File System**

| Port     | Purpose            |
| -------- | ------------------ |
| **2049** | Linux file sharing |

## **LDAP — Directory Services**

| Port    | Purpose      |
| ------- | ------------ |
| **389** | LDAP queries |

## **LDAPS — Secure LDAP**

| Port                             | Purpose        |
| -------------------------------- | -------------- |
| **636**                          | Encrypted LDAP |
| **Memory:** 389 → 636 (secured). |                |

---

# 💾 **DATABASE SERVICES**

## **MySQL**

| Port     | Purpose         |
| -------- | --------------- |
| **3306** | Database access |

## **PostgreSQL**

| Port     | Purpose         |
| -------- | --------------- |
| **5432** | Database access |

## **MSSQL (SQL Server)**

| Port     | Purpose                 |
| -------- | ----------------------- |
| **1433** | Microsoft SQL DB access |

## **MongoDB**

| Port      | Purpose         |
| --------- | --------------- |
| **27017** | NoSQL DB access |

## **Redis**

| Port     | Purpose      |
| -------- | ------------ |
| **6379** | In-memory DB |

---

# 🧠 **SUPER SHORT MEMORY SUMMARY**

**SSH 22 • HTTP 80 • HTTPS 443 • DNS 53 • FTP 21/20 • SMB 445 • RDP 3389 • MySQL 3306 • SMTP 25/587/465 • IMAP 143/993 • POP3 110/995**

---

If you want, I can add **more (VoIP, VPN, ICS, Malware-relevant, Cloud, IoT, ICS/SCADA ports)** in the same format.
