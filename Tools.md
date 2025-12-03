# Penetration Testing Tools Cheatsheet

A compact reference of common tools and commands used across TryHackMe, eJPT, and general pentesting.

---

## **1. Social-Engineer Toolkit (SET)**

* **Tool:** Social-Engineer Toolkit
* **Command:** `setoolkit`
* **Purpose:** Framework for social engineering attacks.
* **Meaning:** Opens the SET interactive menu.
* **Description:** Used to craft phishing emails, payloads, and social‑engineering scenarios.

---

## **2. SearchSploit**

* **Tool:** SearchSploit
* **Command:** `searchsploit <keyword>`
* **Purpose:** Find local exploit files from Exploit‑DB.
* **Meaning:** Searches for vulnerabilities related to the keyword.
* **Description:** Helps quickly match CVEs or software versions to exploits.

---

## **3. John the Ripper**

* **Tool:** john
* **Command:** `john <hashfile>`
* **Purpose:** Crack password hashes.
* **Meaning:** Runs cracking using wordlists or incremental mode.
* **Description:** Popular offline password‑cracking tool.

---

## **4. CrackMapExec**

* **Tool:** crackmapexec
* **Command:** `crackmapexec smb <IP> -u <user> -p <pass>`
* **Purpose:** Lateral movement, enumeration, credential testing.
* **Meaning:** Checks credentials across SMB, WinRM, etc.
* **Description:** Great for AD enumeration and credential spraying.

---

## **5. SSH Login**

* **Tool:** ssh
* **Command:** `ssh user@IP`
* **Purpose:** Remote shell access.
* **Meaning:** Log in to a server through SSH.
* **Description:** Common secure remote login method.

---

## **6. FTP Login**

* **Tool:** ftp
* **Command:** `ftp IP`
* **Purpose:** Connect to an FTP server.
* **Meaning:** Opens FTP interactive shell.
* **Description:** Used to upload/download files on misconfigured servers.

---

## **7. Hashmap / Hashdump**

* **Tool:** Metasploit (post‑modules)
* **Command:** `hashdump`
* **Purpose:** Dump Windows password hashes.
* **Meaning:** Extracts hashes from SAM database.
* **Description:** Useful after privilege escalation.

---

## **8. /etc/shadow**

* **File:** `/etc/shadow`
* **Command:** `cat /etc/shadow`
* **Purpose:** View stored password hashes.
* **Meaning:** Displays hash entries for system accounts.
* **Description:** Requires root; used in Linux privilege escalation.

---

## **9. /etc/hosts**

* **File:** `/etc/hosts`
* **Command:** `cat /etc/hosts`
* **Purpose:** View hostname‑to‑IP mappings.
* **Meaning:** Helps identify local network spoofing or config issues.
* **Description:** Often checked during recon.

---

## **10. /etc/issue & /etc/* files**

* **Command:** `cat /etc/issue` or `cat /etc/*`
* **Purpose:** View OS banners or configurations.
* **Meaning:** Helps determine OS version.
* **Description:** Useful for enumeration during privilege escalation.

---

## **11. IP Address Commands**

### `ip a s` / `ip addr`

* **Tool:** iproute2
* **Command:** `ip a s` or `ip addr`
* **Purpose:** Display network interfaces.
* **Meaning:** Shows IPs, MACs, and interface states.
* **Description:** Basic recon for networking.

---

## **12. Autoroute**

* **Tool:** Metasploit
* **Command:** `run autoroute -s <subnet>`
* **Purpose:** Route traffic through a pivot.
* **Meaning:** Adds a route to reach internal networks.
* **Description:** Used after gaining access to a pivot machine.

---

## **13. Portfwd**

* **Tool:** Metasploit
* **Command:** `portfwd add -l <local> -p <remote> -r <target>`
* **Purpose:** Port forwarding during pivoting.
* **Meaning:** Maps remote ports to local ones.
* **Description:** Allows access to internal services.

---

## **14. IP Route**

* **Command:** `ip route`
* **Purpose:** Show routing table.
* **Meaning:** Displays how packets travel.
* **Description:** Important for understanding pivot paths.

---


## **15. Netcat**

* **Tool:** nc
* **Command:** `nc -lvnp <port>`
* **Purpose:** Listener for reverse shells.
* **Meaning:** Waits for incoming connections.
* **Description:** Used heavily in exploitation for shell access.

---

## **16. Nmap**

* **Tool:** nmap
* **Command:** `nmap -sC -sV <IP>`
* **Purpose:** Service and version detection.
* **Meaning:** Runs default scripts and identifies versions.
* **Description:** First step in enumeration.

---

## **17. Gobuster / Dirsearch**

* **Tool:** gobuster
* **Command:** `gobuster dir -u <URL> -w <wordlist>`
* **Purpose:** Directory brute forcing.
* **Meaning:** Scans for hidden web paths.
* **Description:** Used for web enumeration.

---

## **18. Hydra**

* **Tool:** hydra
* **Command:** `hydra -l user -P wordlist.txt <service>://<IP>`
* **Purpose:** Password brute forcing.
* **Meaning:** Attempts logins using credentials.
* **Description:** Works on SSH/FTP/HTTP and many more.

---

## **19. LinPEAS**

* **Tool:** linpeas.sh
* **Command:** `./linpeas.sh`
* **Purpose:** Automated Linux privilege‑escalation scan.
* **Meaning:** Highlights misconfigurations.
* **Description:** Finds kernel exploits, creds, SUIDs, etc.

---

## **20. WinPEAS**

* **Tool:** winpeas.exe
* **Command:** `winpeas.exe`
* **Purpose:** Windows privilege escalation.
* **Meaning:** Scans for vulnerabilities in system configs.
* **Description:** Equivalent of LinPEAS for Windows.

---

## **21. Netstat**

* **Tool:** netstat
* **Command:** `netstat -tunlp`
* **Purpose:** Show listening ports.
* **Meaning:** Displays active connections.
* **Description:** Helps find hidden services.

---

## **22. SUID Check**

* **Command:** `find / -perm -4000 2>/dev/null`
* **Purpose:** Identify SUID binaries.
* **Meaning:** Lists binaries running as root.
* **Description:** Common Linux priv‑esc point.

---

## **23. Crontab Check**

* **Command:** `cat /etc/crontab`
* **Purpose:** Look for scheduled tasks.
* **Meaning:** Finds misconfigured jobs.
* **Description:** Often leads to escalation through writable scripts.

---

## **24. SCP File Transfer**

* **Tool:** scp
* **Command:** `scp file user@IP:/path`
* **Purpose:** Secure file transfer.
* **Meaning:** Sends files over SSH.
* **Description:** Useful for uploading priv‑esc scripts.

---

## **25. Netcat File Transfer**

* **Command:** `nc -lvp 4444 > file` and `nc <IP> 4444 < file`
* **Purpose:** Send/receive files.
* **Meaning:** Simple data transfer using netcat.
* **Description:** Works when SCP is unavailable.

---

## **26. Python Web Server**

* **Tool:** python3
* **Command:** `python3 -m http.server 8000`
* **Purpose:** File hosting.
* **Meaning:** Opens local HTTP server.
* **Description:** Used for serving payloads.

---

## **27. Msfconsole**

* **Tool:** Metasploit
* **Command:** `msfconsole`
* **Purpose:** Exploitation framework.
* **Meaning:** Opens Metasploit CLI.
* **Description:** Center of exploitation workflow.

---

## **28. Meterpreter Shell Commands**

* **Commands:** `shell`, `download`, `upload`, `ps`, `getuid`
* **Purpose:** Post‑exploitation actions.
* **Description:** Used after gaining a session.

---

## **29. Enum4linux**

* **Tool:** enum4linux
* **Command:** `enum4linux -a <IP>`
* **Purpose:** Enumerate SMB shares and users.
* **Meaning:** Gathers domain and user info.
* **Description:** Helpful for Windows boxes.

---

## **30. SMBClient**

* **Tool:** smbclient
* **Command:** `smbclient //<IP>/share`
* **Purpose:** Connect to SMB shares.
* **Meaning:** Opens SMB shell.
* **Description:** Used for listing and downloading files.
