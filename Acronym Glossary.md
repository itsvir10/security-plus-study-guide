# Acronym Glossary

Every acronym from the CompTIA Security+ (SY0-701) exam objectives, alphabetical, one line each.

- **AAA** - Authentication, Authorization, Accounting (verify identity, grant permissions, log activity)
- **ABAC** - Attribute-Based Access Control (access based on multiple attributes: user+resource+environment)
- **ACL** - Access Control List (rules defining who can access a resource)
- **AES** - Advanced Encryption Standard (strongest common symmetric cipher)
- **AH** - Authentication Header (IPsec component: auth+integrity, NO encryption)
- **AIS** - Automated Indicator Sharing (US gov real-time threat-indicator sharing)
- **ALE** - Annualized Loss Expectancy ($ lost per year = SLE × ARO)
- **APT** - Advanced Persistent Threat (prolonged, well-funded attack campaign)
- **ARO** - Annualized Rate of Occurrence (how often per year)
- **ARP** - Address Resolution Protocol (maps IP → MAC address)
- **ASLR** - Address Space Layout Randomization (randomizes memory locations, blocks buffer overflow exploits)
- **AUP** - Acceptable Use Policy (rules for using company systems)
- **AV** - Asset Value (used in SLE = AV × EF)
- **BEC** - Business Email Compromise (phishing impersonating an executive)
- **BIA** - Business Impact Analysis (assesses impact of disruptions on business functions)
- **BPA** - Business Partnership Agreement (defines a business partnership's terms)
- **CA** - Certificate Authority (issues/manages digital certificates)
- **CBC** - Cipher Block Chaining (block cipher mode, chains blocks together)
- **CCMP** - the AES-based encryption protocol used in WPA2
- **CER** - Crossover Error Rate (point where FAR = FRR in biometrics)
- **CFB** - Cipher Feedback (turns a block cipher into a stream cipher)
- **CHAP** - Challenge Handshake Authentication Protocol (challenge/response auth, no plaintext password)
- **CIA** - Confidentiality, Integrity, Availability (core security triad)
- **CI** - Continuous Integration (frequent code integration + automated testing)
- **COOP** - Continuity of Operations Plan (US gov plan to keep essential functions running)
- **CRC** - Cyclic Redundancy Check (non-cryptographic hash, error-checking only)
- **CRL** - Certificate Revocation List (list of revoked certs)
- **CSR** - Certificate Signing Request (request sent to a CA for a cert)
- **CSRF** - Cross-Site Request Forgery (tricks browser into sending unwanted requests)
- **CVE** - Common Vulnerabilities and Exposures (catalog of known vulnerabilities)
- **CVSS** - Common Vulnerability Scoring System (severity score 0-10)
- **DAC** - Discretionary Access Control (resource owner decides access)
- **DHE** - Diffie-Hellman Ephemeral (key exchange with forward secrecy)
- **DKIM** - DomainKeys Identified Mail (cryptographic email signature = authenticity)
- **DLL** - Dynamic Link Library (shared Windows code library)
- **DLP** - Data Loss Prevention (stops sensitive data leaving the org)
- **DMARC** - Domain-based Message Authentication, Reporting & Conformance (policy layer using SPF+DKIM results)
- **DMZ** - Demilitarized Zone (isolated network segment for public-facing services)
- **DNS** - Domain Name System (translates domain names → IP addresses)
- **DPO** - Data Protection Officer (oversees data-protection law compliance)
- **DRP** - Disaster Recovery Plan (plan to restore systems after a disaster)
- **DSA** - Digital Signature Algorithm (signing only, no encryption)
- **EAP** - Extensible Authentication Protocol (framework for auth methods, used with 802.1X)
- **ECB** - Electronic Codebook (weakest/simplest block cipher mode - avoid)
- **ECC** - Elliptic Curve Cryptography (asymmetric, small keys, efficient - good for IoT)
- **ECDHE** - Elliptic Curve Diffie-Hellman Ephemeral (ECC-based forward-secrecy key exchange)
- **ECDSA** - Elliptic Curve Digital Signature Algorithm (efficient signing, no encryption)
- **EDR** - Endpoint Detection and Response (monitors/responds to threats on one device)
- **EF** - Exposure Factor (% of asset value lost)
- **EFS** - Encrypting File System (Windows per-file encryption)
- **EOL** - End-of-Life (product discontinued/no longer sold)
- **EOS** - End-of-Support (no more patches, even if still in use)
- **ESP** - Encapsulating Security Payload (IPsec component: auth+integrity+encryption)
- **FAR** - False Acceptance Rate (wrongly accepts unauthorized user)
- **FDE** - Full Disk Encryption (encrypts entire storage device)
- **FRR** - False Rejection Rate (wrongly rejects authorized user)
- **FTPS** - FTP + SSL/TLS encryption
- **GCM** - Galois/Counter Mode (CTR encryption + authentication = confidentiality + integrity)
- **GDPR** - General Data Protection Regulation (EU personal-data privacy law)
- **GPS** - Global Positioning System (device location tech)
- **HIPAA** - Health Insurance Portability and Accountability Act (US law protecting PHI)
- **HIPS** - Host-based Intrusion Prevention System (blocks threats on one device)
- **HMAC** - Hash-based Message Authentication Code (hash + secret key = authenticity+integrity)
- **HSM** - Hardware Security Module (external device managing encryption keys at scale)
- **HTTPS** - HTTP + SSL/TLS (secure web browsing)
- **IDEA** - International Data Encryption Algorithm (deprecated symmetric cipher, replaced by AES)
- **IKE** - Internet Key Exchange (sets up IPsec VPN key exchange)
- **IMAPS** - secure IMAP (retrieves + manages email on the server)
- **IRP** - Incident Response Plan (documented plan for handling incidents)
- **ISA** - Interconnection Security Agreement (security terms for connecting two orgs' systems)
- **IV** - Initialization Vector (randomizes encryption so identical plaintext ≠ identical ciphertext)
- **KEK** - Key Encryption Key (encrypts other keys)
- **LDAP** - Lightweight Directory Access Protocol (accessing directory/identity info, enables SSO)
- **LEAP** - Lightweight EAP (deprecated Cisco wireless auth protocol)
- **MAC** - Mandatory Access Control (admin-set labels/clearances, strictest model)
- **MFA** - Multi-Factor Authentication (2+ factors: know/have/are/somewhere-you-are)
- **MOA** - Memorandum of Agreement (formal, often binding, specific terms)
- **MOU** - Memorandum of Understanding (informal, non-binding, general intent)
- **MSA** - Master Service Agreement (umbrella contract for future work)
- **MTBF** - Mean Time Between Failures (avg time between failures, repairable system)
- **MTTF** - Mean Time To Failure (avg time to first failure, non-repairable device)
- **MTTR** - Mean Time To Repair (avg time to fix a failure)
- **NAC** - Network Access Control (checks device posture before network access)
- **NDA** - Non-Disclosure Agreement (confidentiality contract)
- **NGFW** - Next-Generation Firewall (app-aware, deep packet inspection)
- **NIDS** - Network Intrusion Detection System (network-level threat detection)
- **NVD** - National Vulnerability Database (adds CVSS scores to CVEs)
- **OCSP** - Online Certificate Status Protocol (real-time cert validity check)
- **OID** - Object Identifier (identifier for PKI objects)
- **OPSEC** - Operational Security (protecting sensitive operational info)
- **OSINT** - Open-Source Intelligence (threat intel from public sources)
- **PA** - Policy Administrator (Zero Trust: relays PE decision to PEP)
- **PAP** - Password Authentication Protocol (plaintext password auth - weak)
- **PDP** - Policy Decision Point (Zero Trust: decides access = PE + PA)
- **PDU** - Power Distribution Unit (supplies/monitors power to outlets)
- **PEAP** - Protected EAP (auth wrapped in encrypted TLS tunnel)
- **PE** - Policy Engine (Zero Trust: makes the grant/deny decision)
- **PEP** - Policy Enforcement Point (Zero Trust: enforces the access decision)
- **PFS** - Perfect Forward Secrecy (session keys stay safe even if one is compromised)
- **PHI** - Protected Health Information (health data, protected by HIPAA)
- **PII** - Personally Identifiable Information (data identifying a specific person)
- **PKI** - Public Key Infrastructure (system of certs/keys/CAs)
- **PSK** - Pre-Shared Key (shared passphrase auth, e.g. WPA2-Personal)
- **PUP** - Potentially Unwanted Program (broader than bloatware: perf+privacy+security risk)
- **RADIUS** - AAA protocol for network access, combines authN+authZ
- **RA** - Registration Authority (accepts/verifies cert requests, doesn't issue) - also Recovery Agent (key escrow context)
- **RAT** - Remote Access Trojan (gives attacker remote control)
- **RBAC** - Role-Based Access Control (access tied to job role)
- **RCE** - Remote Code Execution (attacker runs code on your system remotely)
- **RPO** - Recovery Point Objective (max acceptable DATA loss, in time)
- **RSA** - asymmetric cryptosystem for signatures/key exchange/encryption (large primes)
- **RTO** - Recovery Time Objective (max acceptable DOWNTIME)
- **RTOS** - Real-Time Operating System (guaranteed strict response time, weaker buffer overflow protection)
- **SAE** - Simultaneous Authentication of Equals (WPA3-Personal auth, replaces PSK)
- **SAML** - Security Assertion Markup Language (XML-based SSO auth exchange)
- **SASE** - Secure Access Service Edge (networking + security, cloud-delivered)
- **SCAP** - Security Content Automation Protocol (automates vuln/compliance checks)
- **SDLC** - Software Development Lifecycle (secure software-building process)
- **SDN** - Software-Defined Networking (manage network via software, not hardware)
- **SED** - Self-Encrypting Drive (hardware-level encrypted storage device)
- **SEH** - Structured Exception Handling (Windows error/exception handling)
- **SFTP** - SSH File Transfer Protocol (secure file transfer OVER SSH, port 22)
- **SHA** - Secure Hash Algorithm (family of hash functions)
- **SIEM** - Security Information and Event Management (centralizes/correlates logs)
- **SIP** - Session Initiation Protocol (VoIP call setup, port 5060)
- **SLA** - Service Level Agreement (defines expected performance)
- **SLE** - Single Loss Expectancy ($ lost in one incident = AV × EF)
- **SMTPS** - deprecated secure SMTP (sending email), replaced by STARTTLS
- **SOAR** - Security Orchestration, Automation, and Response (automates incident response)
- **SOP** - Standard Operating Procedure (documented standard task process)
- **SOW** - Statement of Work (specific project scope/timeline/cost)
- **SPF** - Sender Policy Framework (lists servers allowed to send mail for a domain)
- **SRTP** - Secure RTP (encrypted real-time audio/video)
- **SSH** - Secure Shell (secure remote login/command execution - replaces Telnet)
- **SSID** - Service Set Identifier (Wi-Fi network name)
- **SSO** - Single Sign-On (one login for multiple systems)
- **STIX** - Structured Threat Information eXpression (language for describing threat intel)
- **TACACS+** - AAA protocol, separates authN/authZ/accounting (vs. RADIUS which combines)
- **TAXII** - Trusted Automated eXchange of Indicator Information (transport for threat intel)
- **TKIP** - Temporal Key Integrity Protocol (quick fix for WEP, used in original WPA)
- **TLS** - Transport Layer Security (successor to SSL)
- **TPM** - Trusted Platform Module (on-device chip storing keys)
- **TTP** - Tactics, Techniques, and Procedures (attacker methods/tools)
- **UBA** - User Behavior Analytics (flags anomalies vs. normal behavior)
- **UPS** - Uninterruptible Power Supply (short-term backup power)
- **UTM** - Unified Threat Management (all-in-one security appliance)
- **VPN** - Virtual Private Network (private encrypted connection over a public network)
- **WAF** - Web Application Firewall (protects web apps specifically)
- **WEP** - Wired Equivalent Privacy (old, broken Wi-Fi security - avoid)
- **WO** - Work Order (authorizes/tracks a specific job/task)
- **WPA/WPA2/WPA3** - Wi-Fi Protected Access (wireless security standards, 3 = newest/strongest)
- **WPS** - Wi-Fi Protected Setup (brute-forceable PIN flaw - weak)
- **XDR** - Extended Detection and Response (EDR extended across network/email/cloud)
- **XOR** - Exclusive OR (logical operation used in encryption/obfuscation)
- **XSS** - Cross-Site Scripting (malicious script injected into a trusted site)

## Fastest-confused clusters (drill these pairs/groups specifically)

- **RTO vs RPO vs MTBF vs MTTR vs MTTF** - downtime / data-loss / time-between-failures / time-to-repair / time-to-first-failure
- **EF vs SLE vs ARO vs ALE** - % lost / $ per incident / frequency per year / $ per year
- **SOW vs MSA vs SLA vs MOU vs MOA vs BPA vs NDA** - project scope / umbrella contract / performance terms / informal intent / formal specific terms / partnership terms / confidentiality
- **DKIM vs SPF vs DMARC** - signs the email / lists allowed servers / policy for failures
- **RBAC vs ABAC vs DAC vs MAC vs Rule-based** - by role / by multiple attributes / owner decides / admin labels, strictest / if-then rules
- **CA vs RA** - issues certs / only verifies requests
- **NGFW vs UTM vs WAF** - app-aware+DPI / all-in-one bundle / web-app-specific
- **AES vs HMAC vs SHA vs RSA vs DSA vs ECDSA** - symmetric encryption / hash+key auth / hash family / asymmetric multi-use / sign-only / efficient sign-only
- **AH vs ESP** - auth+integrity only / auth+integrity+encryption

## Common Ports - full list

| Port | Protocol/Service |
|---|---|
| 21 | FTP (control - unencrypted) |
| 22 | SSH / SFTP (secure login + secure file transfer over SSH) |
| 23 | Telnet (unencrypted - insecure, replaced by SSH) |
| 25 | SMTP (sending email) |
| 49 | TACACS+ (AAA, device admin) |
| 53 | DNS |
| 80 | HTTP (unencrypted web) |
| 88 | Kerberos (authentication) |
| 110 | POP3 (retrieve email) |
| 143 | IMAP (retrieve + sync email) |
| 161/162 | SNMP (device monitoring) |
| 389 | LDAP (directory services, unencrypted) |
| 443 | HTTPS (encrypted web) |
| 445 | SMB (Windows file/print sharing) |
| 587 | SMTP submission (modern secure mail sending, STARTTLS) |
| 636 | LDAPS (LDAP secure) |
| 989/990 | FTPS (FTP + TLS) |
| 993 | IMAPS (secure IMAP) |
| 995 | POP3S (secure POP3) |
| 1433 | MS SQL Server |
| 1812/1813 | RADIUS (AAA, network access) |
| 3389 | RDP (Windows remote desktop) |
| 5060 | SIP (VoIP call setup) |

**Domain Controller fingerprint:** seeing 53 + 80 + 88 + 389 (± 636) open together on one host = classic Active Directory / Windows Domain Controller signature.

### Fastest-confused pairs (ports)

- **FTP (21, plaintext) vs SFTP (22, over SSH) vs FTPS (989/990, FTP+TLS)**
- **POP3 (110) / IMAP (143) vs their secure versions POP3S (995) / IMAPS (993)**
- **SMTP (25, sending) vs SMTP submission (587, modern secure)** - both sending, don't confuse with the retrieving ports above
- **LDAP (389) vs LDAPS (636)** - same protocol, unencrypted vs. encrypted
- **RADIUS (1812/1813, combines authN+authZ) vs TACACS+ (49, separates them)**
