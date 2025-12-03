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

If you want, I can continue adding more eJPT, Metasploit, Linux priv‑esc, and TryHackMe common commands.
