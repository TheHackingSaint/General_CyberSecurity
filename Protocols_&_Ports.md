# Protocols and Ports Reference (Sorted by Port Number)

Comprehensive consolidated table of common protocols, their port numbers, purpose, and detailed descriptions.

---

| Protocol           | Port(s)    | What It Is            | Short Info                  | Detailed Description                                       |
| ------------------ | ---------- | --------------------- | --------------------------- | ---------------------------------------------------------- |
| **ICMP**           | N/A        | Network Control       | Echo requests               | Layer 3 protocol used by ping; no ports.                   |
| **Echo**           | 7          | Diagnostics           | Basic test service          | Used for testing and debugging; usually disabled.          |
| **Discard**        | 9          | Diagnostics           | Discards all data           | Useful for testing; can reveal active hosts.               |
| **Daytime**        | 13         | Diagnostics           | Returns server time         | Legacy protocol still seen on old systems.                 |
| **Chargen**        | 19         | Character Generator   | Outputs characters          | Abused for DDoS amplification; never expose.               |
| **FTP**            | 20, 21     | File Transfer         | File transfers              | Port 21 for control, 20 for active data transfer.          |
| **SSH**            | 22         | Secure Shell          | Secure remote login         | Encrypted remote access; supports tunneling and key auth.  |
| **Telnet**         | 23         | Remote Terminal       | Unencrypted login           | Everything plaintext; dangerous if open.                   |
| **SMTP**           | 25         | Email Transfer        | Sends email                 | Used for server-to-server mail. Allows enumeration.        |
| **DNS**            | 53         | Name Resolution       | Resolves domains            | UDP for lookups, TCP for zone transfers.                   |
| **DHCP**           | 67, 68     | IP Assignment         | Auto IP configuration       | Used for assigning IP details. Attackers abuse rogue DHCP. |
| **TFTP**           | 69         | File Transfer         | Simple file transfer        | No authentication; used in embedded systems.               |
| **HTTP**           | 80         | Web Protocol          | Serves web pages            | Basis of browsing; prone to injection vulnerabilities.     |
| **POP3**           | 110        | Mail Retrieval        | Downloads email             | Plaintext; insecure without POP3S.                         |
| **NTP**            | 123        | Time Sync             | Sync system time            | Vulnerable to reflection-based DDoS attacks.               |
| **IMAP**           | 143        | Email Protocol        | Retrieve email              | Supports folders and server-side storage.                  |
| **SNMP**           | 161, 162   | Network Management    | Device monitoring           | Default strings exposed often; information leakage.        |
| **LDAP**           | 389        | Directory Services    | Directory lookups           | Common in AD environments; supports enumeration.           |
| **HTTPS**          | 443        | Secure HTTP           | Encrypted web traffic       | TLS-protected browsing.                                    |
| **SMTPS (Legacy)** | 465        | Secure SMTP           | Encrypted mail              | Old SSL-wrapped SMTP.                                      |
| **Syslog**         | 514        | Logging               | Network log forwarding      | Supports UDP-based SIEM logging.                           |
| **Telnets**        | 992        | Secure Telnet         | Encrypted Telnet            | Rare; still unsafe.                                        |
| **IMAPS**          | 993        | Secure IMAP           | Encrypted email retrieval   | IMAP using TLS.                                            |
| **POP3S**          | 995        | Secure POP3           | Encrypted email retrieval   | POP3 secured by TLS.                                       |
| **SOCKS Proxy**    | 1080       | Proxy Protocol        | Forward traffic             | Used for tunneling and bypassing restrictions.             |
| **NetBIOS**        | 137–139    | Windows Name Services | File & name sharing         | Legacy Windows networking; enumeratable.                   |
| **IPP**            | 631        | Printing Protocol     | Network printing            | Reveals printer configs and leaks info.                    |
| **LDAP LDAPS**     | 636        | Secure LDAP           | Encrypted directory service | LDAP over SSL/TLS.                                         |
| **MySQL**          | 3306       | Database              | SQL database port           | Often brute-forced; misconfigs expose data.                |
| **RDP**            | 3389       | Remote Desktop        | GUI remote access           | High-value target for attackers.                           |
| **PostgreSQL**     | 5432       | Database              | Advanced SQL DB             | Target for SQL bruteforce and misconfig tests.             |
| **MSSQL**          | 1433       | Database              | Microsoft SQL Server        | Attackers target weak credentials and xp_cmdshell.         |
| **Oracle DB**      | 1521       | Database Listener     | Oracle database service     | Version disclosure and brute force attacks common.         |
| **MQTT**           | 1883       | IoT Messaging         | Lightweight messaging       | Widely used in IoT; insecure by default.                   |
| **MQTTS**          | 8883       | Secure MQTT           | TLS-secured IoT messaging   | Encrypted variant of MQTT.                                 |
| **RADIUS**         | 1812, 1813 | Auth Service          | AAA authentication          | Used in enterprise networks and VPNs.                      |
| **NFS**            | 2049       | File Sharing          | Linux file sharing          | Exposes exported directories; can leak home dirs.          |
| **Docker API**     | 2375       | Container API         | Docker control              | If open, attackers can take over host.                     |
| **MongoDB**        | 27017      | NoSQL DB              | Database port               | Often exposed without authentication.                      |
| **VNC**            | 5900       | Remote GUI            | Remote desktop              | No encryption; needs strong passwords.                     |
| **Elasticsearch**  | 9200       | Search Engine API     | Elastic REST API            | Exposed APIs allow data theft.                             |
| **Tor ORPort**     | 9001       | Onion Routing         | Tor relay traffic           | Handles encrypted Tor relay connections.                   |
| **Tor DirPort**    | 9030       | Tor Directory         | Mirror info                 | Stores Tor network directory data.                         |
| **Splunk Web**     | 8000       | Dashboard             | SIEM UI                     | Web interface for Splunk.                                  |
| **Grafana**        | 3000       | Monitoring            | Dashboards                  | Used for visualizing metrics.                              |
| **Kibana**         | 5601       | Dashboard             | Elastic frontend            | Visualizes Elasticsearch data.                             |
| **Prometheus**     | 9090       | Metrics DB            | Time-series data            | Stores and queries monitoring metrics.                     |
| **WinRM**          | 5985, 5986 | Windows Remote Mgmt   | Windows shell               | Used by pentesting tools like CME.                         |
| **RabbitMQ**       | 5672       | Message Broker        | Queue service               | Used for distributed message queues.                       |
| **Zookeeper**      | 2181       | Cluster Coordination  | Distributed systems         | Leaks cluster state if exposed.                            |
| **Memcached**      | 11211      | Caching               | Memory cache system         | Amplification attack vector.                               |
| **X11**            | 6000–6005  | Display Server        | Remote GUI                  | Can allow screen hijacking.                                |
| **Metasploit RPC** | 55553      | MSF RPC               | Automation interface        | Controls Metasploit remotely.                              |

---

