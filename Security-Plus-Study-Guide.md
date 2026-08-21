# CompTIA Security+ (SY0-701) Study Guide

A glossary-style set of study notes covering the CompTIA Security+ (SY0-701) exam objectives, organized by domain. Written to be a quick, plain-English reference for anyone studying for the exam.

## Table of Contents

- [Domain 1.0 - General Security Concepts](#domain-10---general-security-concepts)
- [Domain 2.0 - Threats, Vulnerabilities, and Mitigations](#domain-20---threats-vulnerabilities-and-mitigations)
- [Domain 3.0 - Security Architecture](#domain-30---security-architecture)
- [Domain 4.0 - Security Operations](#domain-40---security-operations)
- [Domain 5.0 - Security Program Management and Oversight](#domain-50---security-program-management-and-oversight)

---

# Domain 1.0 - General Security Concepts

## Security Controls

Security controls are the safeguards an organization puts in place to reduce risk. SY0-701 groups them into **4 categories**: Technical, Managerial, Operational, Physical.

### Technical (Logical) Controls
Built into technology and carried out automatically by systems, not manually by a person.
- **Firewall** - monitors and filters network traffic in/out of a network based on rules.
- **Encryption** - scrambles data with an algorithm/key so only someone with the key can read it.
- **IDS / IPS** - a system that watches for suspicious activity. IDS detects and alerts; IPS also actively blocks the threat.
- **ACL (Access Control List)** - rules attached to a resource defining who/what is allowed or denied access.
- **Authentication protocols** - mechanisms that verify identity automatically:
  - **PAP** - sends username/password in plaintext - weak, outdated.
  - **CHAP** - authenticates via challenge/response instead of sending the password directly.
  - **MS-CHAP** - Microsoft's improved version of CHAP.
  - **RADIUS** - a full AAA protocol centralizing Authentication, Authorization, and Accounting for network access.
  - **TACACS+** - similar to RADIUS but separates Authentication, Authorization, and Accounting so each can be managed independently.

### Managerial (Administrative) Controls
Governance, planning, and paperwork - decisions set by management, documented in policy rather than enforced by a machine.
- **Security policy** - a document stating an organization's security rules and expectations.
- **Risk assessment** - identifying threats/vulnerabilities and evaluating how much risk they pose.
- **Security audit** - a formal review of systems/policies/processes to check compliance and find gaps.
- **Asset management** - tracking and overseeing an organization's assets (what they are, who owns them, their lifecycle).

### Operational Controls
Day-to-day processes, mainly carried out by people, that keep security running smoothly.
- **Security awareness training** - teaching employees about risks (like phishing) so human error isn't a weak point.
- **Configuration management** - tracking and controlling changes to a system's settings.
- **Contingency planning** - preparing a plan for what to do if something goes wrong.
- **System backups** - actually performing backups day-to-day (the strategy behind them is Managerial).
- **Patch management** - the recurring process of finding, testing, and applying updates.

### Physical Controls
Protect tangible things - buildings, hardware, people.
- **Locks, fences, guards, cameras** - barriers or monitoring that stop unauthorized physical access.
- **Lighting** - deters intruders and helps guards/cameras see clearly; also improves employee safety.
- **Access control vestibule** (formerly "mantrap") - a small double-door entryway that only lets one person through at a time, preventing tailgating.
- **Bollards vs. barricades** - a bollard is a sturdy post designed to stop a vehicle even at speed (some retractable); a barricade is the more general term, blocking either vehicle or pedestrian traffic.
- **Security guards** - a flexible compensating control: can substitute for a broken camera, patrol a damaged fence section, or respond to alarms.
- **Signage** - acts as both a deterrent (warning of consequences) and wayfinding (directing people to the right area, making suspicious behavior easier to spot).
- **Alarms** - trigger on fire/heat, unauthorized entry, glass-break sensors, or PIDS (Perimeter Intrusion Detection System - e.g. fence-vibration sensors).

## Security Control Types (by function)

Separate from the 4 categories above - control **types** describe what a control *does* in relation to an incident.

- **Preventive** - stops an incident before it happens (encryption, firewalls, antivirus, sandboxing).
- **Deterrent** - discourages an attacker without physically stopping them (warning signs, lighting, fencing/bollards).
- **Detective** - notices/alerts that something happened, without stopping it (IDS, sensors, log monitoring, audits, CCTV, vulnerability scanning).
- **Corrective** - fixes/limits damage after an incident (restoring from backup, patching, executing an IRP).
- **Compensating** - an alternative control when the ideal one isn't available (a UPS when power can't be relied on, MFA when a strong password policy can't be enforced, network segmentation for an unpatchable system).
- **Directive** - mandates a specific action via written policy (an AUP, required security awareness training).

## Core Security Principles

- **CIA Triad** - the foundational goals every control ultimately serves:
  - **Confidentiality** - data is private, accessible only to authorized people.
  - **Integrity** - data is accurate and unaltered.
  - **Availability** - systems/data are accessible when needed.
- **Non-repudiation** - the inability to deny responsibility for an action. Proves *who did it* (not the same as confidentiality). Achieved mainly through digital certificates and signatures. A shared account (multiple people, one login) breaks non-repudiation.

## Zero Trust Architecture

A security model with **no implicit trust** - every user/device must be continuously verified before being granted access, regardless of whether they're already "inside" the network.

- **Control Plane** - the decision-making side:
  - **Policy Decision Point (PDP)** = **Policy Engine** (evaluates policy/context, makes the decision) + **Policy Administrator** (relays that decision to enforcement).
  - **Adaptive identity** - considers identity, device security, and network context for dynamic access decisions.
  - **Threat scope reduction** - limiting what an attacker could reach even if they get in.
- **Data Plane** - the enforcement side:
  - **Policy Enforcement Point (PEP)** - actually enforces the access decision.
  - **Subject** - the user or device requesting access (being evaluated, not doing the enforcing).
  - **Implicit trust zones** - the old, risky model Zero Trust eliminates.
  - **Microsegmentation** - dividing a network into small isolated zones to limit how far an attacker can move.

Control Plane decides; Data Plane enforces.

## Deception Technology

- **Honeypot** - a decoy system mimicking a real one to attract and study attackers.
- **Honeynet** - a whole network of honeypots.
- **Honeyfile** - a decoy file with fake data, placed to attract attackers and trigger alerts if accessed.
- **Honeytoken** - a fake credential/API key/database entry designed to signal unauthorized activity if used.

## PKI & Cryptography Basics

- **PKI (Public Key Infrastructure)** - the system for creating, managing, storing, distributing, and revoking digital certificates.
- **Asymmetric key pair** - a public key (shared openly, encrypts data / verifies signatures) and a private key (kept secret, decrypts data / creates signatures).
- **Key escrow** - storing copies of encryption keys with a trusted third party for recovery if the owner loses their key.
- **RA (Recovery Agent)** - one way (not the only way) to implement key escrow.

## Encryption Technologies

- **SED (Self-Encrypting Drive)** - a storage device with encryption built into its hardware.
- **FDE (Full Disk Encryption)** - software encrypting an entire storage device.
- **EFS (Encrypting File System)** - a Windows feature encrypting individual files/folders.
- **GPG / PGP** - software specifically for encrypting communications and storage (emails, files).

**Encryption levels**, broadest to most granular: Full-disk → Partition → Volume → File → Database → Record.

## Secure Network Protocols

- **HTTPS** - HTTP secured with SSL/TLS; secure web browsing.
- **SMTPS** - deprecated protocol for secure email sending, superseded by STARTTLS (upgrades an existing connection to encrypted rather than requiring a separate always-encrypted protocol).
- **S/MIME** - adds encryption, authentication, and integrity to email (built on MIME).
- **IMAPS / POP3S** - securely retrieve email from a server. IMAPS also keeps mail on the server and syncs across devices; POP3S downloads and typically removes it.
- **SFTP** - secure file transfer over SSH (not an extension of FTP).
- **FTPS** - FTP with SSL/TLS added (uses its own ports, typically 989/990 - not port 22, which is SFTP).
- **SSH** - secure remote login/command execution; the secure replacement for Telnet (which sends everything, including credentials, in plaintext).
- **RTP / SRTP** - RTP delivers real-time audio/video with no security; SRTP is the encrypted, authenticated version.
- **TLS** - the direct successor to SSL, the current standard for securing network communications.

## IPsec & VPN

- **VPN** - creates a private, encrypted connection over a public network.
- **IPsec** - a protocol suite for encryption, authentication, and integrity, commonly used to build VPNs:
  - **AH (Authentication Header)** - authentication and integrity only, **no encryption**.
  - **ESP (Encapsulating Security Payload)** - authentication, integrity, **and** encryption.
  - **IKE (Internet Key Exchange)** - sets up the secure connection and exchanges keys.

## Wireless Security Protocols

- **TKIP** - a quick fix for WEP's weaknesses, used in original WPA (since replaced by CCMP).
- **CCMP** - the AES-based encryption protocol used in WPA2.
- **PSK (Pre-Shared Key)** - a shared-secret authentication method used in WPA/WPA2/EAP.

**SSID basics:** the wireless network's broadcast name. Changing the default SSID is recommended, since manufacturer defaults are well-known and can cause confusion/accidental connections. Client and access point security settings must match for a connection to succeed.

**WPA3 (current standard):**
- Offers the highest level of protection of common wireless schemes.
- **AES-GCMP** - WPA3's encryption protocol (an upgrade from WPA2's AES-CCMP).
- **SAE (Simultaneous Authentication of Equals)** - the client authentication method in WPA3-Personal, replacing PSK; resistant to offline dictionary attacks.

**Personal vs. Enterprise mode:** Personal uses a shared passphrase (PSK/SAE), no auth server needed. Enterprise uses IEEE 802.1X + a RADIUS authentication server for individual user authentication - suited for large networks.

**EAP family** (used within WPA2/WPA3-Enterprise and RADIUS):
- **EAP** - the general authentication framework.
- **PEAP** - wraps authentication inside an encrypted TLS tunnel.
- **EAP-TLS** - requires certificates on both client and server for mutual authentication.
- **LEAP** - a deprecated, Cisco-proprietary protocol with known weaknesses.

## Cryptographic Algorithms

- **Symmetric encryption** (secret-key) - the same key encrypts and decrypts; faster, but the key must be shared secretly beforehand. Examples: AES, DES, 3DES, IDEA, RC4.
- **Asymmetric encryption** (public-key) - a key pair, where a public key encrypts and only the matching private key decrypts (and vice versa). Examples: RSA, DHE, ECC, ECDSA.
- **AES** - the current gold-standard symmetric algorithm, recommended replacement for DES.
- **RSA** - an asymmetric cryptosystem using large prime numbers, used for key exchange, digital signatures, and encryption.
- **ECC (Elliptic Curve Cryptography)** - asymmetric encryption with small keys and low compute cost, well suited to IoT and mobile devices.
- **Deprecated/insecure:** DES, MD5, SHA-1, SSL, RC4, IDEA.
- **Key length** - longer keys generally mean stronger encryption (more possible combinations). Among AES options, 256-bit is the strongest.

## Cipher Building Blocks & Modes

- **IV (Initialization Vector)** - a random value ensuring identical plaintext doesn't produce identical ciphertext.
- **XOR** - a logical operation commonly used as a building block in encryption/obfuscation.
- **Block cipher modes:**
  - **ECB** - simplest and weakest; identical plaintext blocks produce identical ciphertext (leaks patterns) - not recommended.
  - **CBC** - chains ciphertext blocks together so each depends on the previous one.
  - **CFB** - turns a block cipher into a stream cipher.
  - **CTR** - combines a counter with the key to generate a pseudorandom keystream.
  - **GCM** - combines CTR-style encryption with authentication, providing both confidentiality and integrity.

## Key Exchange & Forward Secrecy

- **DHE (Diffie-Hellman Ephemeral)** - generates a new temporary key per session, providing forward secrecy.
- **ECDHE** - the same concept using ECC math for better efficiency.
- **PFS (Perfect Forward Secrecy)** - the overall property these protocols achieve.
- **KEK (Key Encryption Key)** - a key used specifically to encrypt other keys.

## Change Management

Managing changes to systems safely so security doesn't get broken along the way.
- **Business processes:** approval process, ownership, stakeholders, impact analysis, test results, backout plan, maintenance window, SOP.
- **Technical implications:** allow/deny lists, restricted activities, downtime, service restarts, legacy application compatibility, dependencies.
- **Documentation and version control** keep records in sync with reality and allow rollback.

## Hashing

- **Hash function** - maps data of any size to a fixed-size output (a digest/checksum), sensitive to even a single-bit input change - useful for detecting tampering.
- **MD5** - an older hash function, now deprecated due to known collision weaknesses.
- **SHA (Secure Hash Algorithm)** - a family of hash functions (SHA-1, SHA-2, SHA-3); SHA-3 offers the highest security of the family.
- **HMAC** - combines a hash function with a secret key, verifying both authenticity and integrity (plain hashing alone only verifies integrity).
- **CRC (Cyclic Redundancy Check)** - a non-cryptographic hash, used for basic error-checking, not security.

## Digital Signatures

- **Digital signature** - verifies authenticity and integrity of a document using the sender's private key.
- **Algorithms:** RSA, DSA, ECDSA.
  - **DSA** - signing only, not designed for encryption.
  - **RSA** - multi-purpose: encryption *and* signatures.
  - **ECDSA** - signing only, more efficient than DSA thanks to elliptic curve math, well suited to IoT/mobile.

## Certificates

- **Digital certificate** - verifies the identity of an individual, device, service, or organization online.
- **CA (Certificate Authority)** - the trusted third party that issues, revokes, and manages certificates.
- **RA (Registration Authority)** - accepts and verifies certificate requests before passing them to the CA (doesn't issue certificates itself).
- **CRL (Certificate Revocation List)** - a periodically published list of revoked certificates.
- **OCSP (Online Certificate Status Protocol)** - real-time, on-demand check of one certificate's status - faster than downloading a full CRL.
- **Self-signed certificates** - not trusted by default, not backed by a trusted CA, typically used in internal/test environments. Third-party certificates cost money, require identity validation, and are trusted by default.
- **Root of trust** - the root CA, the foundation the whole PKI hierarchy derives trust from.
- **CSR (Certificate Signing Request)** - the file an entity generates to request a certificate from a CA.
- **Wildcard certificate** - secures a domain and all its subdomains.
- **SAN certificate** - secures multiple, possibly unrelated domain names with one certificate.

## Blockchain

- **Blockchain** - a distributed, tamper-resistant ledger where each new entry is cryptographically linked to the previous one, making past entries very hard to alter undetected.

## Cryptographic Hardware

- **TPM (Trusted Platform Module)** - a chip built into a device that securely stores encryption keys.
- **HSM (Hardware Security Module)** - a dedicated external device for managing keys at scale.
- **Secure enclave** - an isolated, protected processor area for handling sensitive data/keys.

---

# Domain 2.0 - Threats, Vulnerabilities, and Mitigations

## Threat Actors

| Threat Actor | Internal/External | Resources | Sophistication | Typical Motivation |
|---|---|---|---|---|
| Nation-state | External | High | High | Espionage, political beliefs, disruption, war |
| Unskilled attacker | Internal/External | Low | Low | Disruption, financial gain, revenge |
| Hacktivist | External | Low–Medium | Low–Medium | Ethical/political beliefs, disruption |
| Insider threat | Internal | Low–High | Low–High | Revenge, financial gain, service disruption |
| Organized crime | External | Medium–High | Medium–High | Financial gain, extortion |
| Shadow IT | Internal | Low–Medium | Low–Medium | Convenience, unmet needs |

- **APT (Advanced Persistent Threat)** - a sophisticated, prolonged attack campaign, typically well-funded (classically nation-state).

## Threat Vectors & Attack Surfaces

- **Attack surface** - the total sum of potential entry points an attacker could use.
- **Threat vector** - the specific method/path used to actually deliver an attack.

**By channel:** Email (spoofing, phishing, BEC, malicious links/attachments), SMS (smishing), Voice (vishing), Instant messaging, Image-based (steganography, deepfakes), File-based (malicious documents, scripts, executables), Removable devices.

**By software type:** Client-based (requires software on the device) vs. Agentless (exploits the network/protocol directly).

**Other vectors:** Unsupported systems (no more patches for known flaws), unsecure wireless/wired/Bluetooth networks, open service ports, default credentials, supply chain risk (via MSPs/vendors/suppliers).

## Social Engineering

Exploits people/trust rather than technical flaws. Best overall countermeasure: user education.

- **Phishing** - disguising a fraudulent request as legitimate to steal information. Sub-types: Vishing (voice), Smishing (SMS), BEC (Business Email Compromise - impersonating an executive/partner).
- **Misinformation vs. disinformation** - false info spread unintentionally vs. deliberately.
- **Impersonation** - pretending to be someone else. **Pretexting** - inventing a fabricated scenario; often paired with impersonation.
- **Watering hole attack** - compromising a website the target is known to visit.
- **Typosquatting** - registering misspelled lookalike domains to catch mistyped traffic or host phishing.

**Signs of phishing:** poor spelling/grammar, requests for personal info, urgency, suspicious links/attachments.

## Vulnerabilities

- **Application:** memory injection, pointer dereference, memory leaks, DLL injection, buffer overflow, race conditions (TOC/TOU), malicious updates.
- **OS-based:** access control issues, vulnerable installed software, memory issues, patch management gaps, misconfigurations, network issues (all count as OS-based vulnerabilities).
- **Web-based:** SQL injection (malicious input manipulating a database query), XSS (a malicious script runs in the victim's browser via a trusted site - distinct from CSRF, where the victim's browser is tricked into sending an unauthorized request the website trusts).
- **Hardware:** firmware issues, EOL (product discontinued) vs. EOS (no more support/patches, even if still in use).
- **Virtualization:** VM escape, resource reuse, resource exhaustion.
- **Cloud:** insecure APIs, poor access controls, misconfigured storage.
- **Mobile:** sideloading, jailbreaking (iOS), rooting (Android), carrier unlocking.
- **Zero-day** - a vulnerability already present but unknown to the developer, so no patch exists yet.

## Malware Attacks

- **Ransomware** - encrypts/locks a system, demanding payment for restored access.
- **Trojan** - malware disguised as a legitimate program.
- **RAT (Remote Access Trojan)** - a Trojan giving an attacker remote control.
- **Worm** - self-propagates across a network on its own, no host file needed (unlike a virus, which needs a host application to run).
- **Fileless malware** - operates entirely in memory, evading file-based antivirus detection.
- **Spyware / Keylogger** - secretly collects user info / records keystrokes.
- **Bloatware** (pre-installed by manufacturer, performance impact) vs. **PUP** (broader - any source, impacts performance, privacy, and security).
- **Virus** - needs a host application to run, self-replicates once activated.
- **Logic bomb** - dormant malicious code triggered by a specific event/condition.
- **Rootkit** - hides an intrusion and maintains admin-level access undetected.
- **Backdoor** - a hidden method of bypassing normal authentication.
- **Cryptomalware (cryptojacking)** - hijacks system resources to mine cryptocurrency.
- **Bot / Botnet** - a compromised device under remote control; many together form a botnet.

## Network Attacks

- **DDoS** - many compromised systems (a botnet) attack a target.
  - **Amplified DDoS** - a small request triggers a much larger response directed at the victim.
  - **Reflected DDoS** - the attacker spoofs the victim's IP so third-party servers send responses back to the victim.
- **DNS attacks:** DNS spoofing/cache poisoning (feeding false DNS info), domain hijacking (losing control of your own domain), URL hijacking (typosquatting-style redirection).
- **Credential attacks:** credential stuffing (leaked credentials tried on other services), Sybil attack (many fake identities gaining influence).
- **Downgrade attack** - forcing a fallback to a weaker, exploitable protocol/encryption version.
- **Wireless attacks:** bluesnarfing (unauthorized Bluetooth access), deauthentication/jamming (DoS-style), IV attacks (exploits WEP's weak IVs), war driving, SSID spoofing (evil twin).
- **On-path attack** (formerly MITM) - intercepting/modifying traffic between two devices.
- **Replay / session attacks:** replay attack (resending captured data), session hijacking (taking over a valid session), pass the hash (authenticating with a captured hash, no cracking needed).
- **Cryptographic attacks:** collision attack (finding two inputs with the same hash), birthday attack (statistical shortcut to finding collisions).
- **Physical attacks:** RFID cloning, environmental attacks (HVAC/fire-suppression tampering).
- **Password attacks:** password spraying (one password, many accounts - evades lockouts), brute force (many passwords, one account).

## Application Attacks

- **LDAP injection** - malicious input manipulating LDAP directory queries.
- **XML injection** - malicious XML content injected into an app that processes XML.
- **Privilege escalation** - gaining higher access than intended, via vulnerabilities, misconfigurations, or social engineering.
- **Directory traversal** - using dot-dot-slash path sequences to escape the intended directory and access restricted files.

## Indicators of Malicious Activity

- **IoC (Indicators of Compromise)** - forensic evidence of unauthorized access or malicious activity.
- **Account lockout** - often indicates a brute-force attempt.
- **Impossible travel** - logins from geographically distant locations too close in time to be physically possible.
- **Missing logs** - a classic sign of an attacker covering their tracks.

## Mitigation Techniques

- **Segmentation** - isolating network zones to contain an attacker who gets into one part.
- **Application allow list** - only pre-approved applications may run.
- **Least privilege** - minimum access needed to do the job.
- **Configuration enforcement** - keeping systems in their secure, approved state.
- **Hardening:** endpoint protection (AV/EDR), host-based firewalls, HIPS, disabling unused ports/protocols, changing default passwords, removing unnecessary software.

---

# Domain 3.0 - Security Architecture

## Architecture and Infrastructure Models

- **Cloud:** responsibility matrix (who's responsible for what - you vs. provider), hybrid considerations, third-party vendors.
- **IaC (Infrastructure as Code)** - managing infrastructure through code/config rather than manual setup.
- **Serverless** - running code without managing the underlying servers.
- **Microservices** - building an application as many small, independent services.
- **Physical isolation (air-gapped)** vs. **logical segmentation** (separated via config, not physical disconnection).
- **SDN (Software-Defined Networking)** - managing network behavior via software.
- **Containerization** - packaging an app with its dependencies into a portable, isolated unit (e.g. Docker) - lighter than a full VM.
- **ICS/SCADA** - systems controlling physical industrial processes.
- **RTOS (Real-Time Operating System)** - guarantees a strict response time; often trades off some security hardening (e.g. buffer overflow protection) for that guarantee.

## Data Protection Concepts

- **PII** - any info identifying a specific individual (broad, general term).
- **PHI** - health-related personal data, protected under HIPAA.
- **PCI DSS** - protects credit cardholder data specifically.
- **DPO (Data Protection Officer)** - oversees an organization's data-protection compliance.

**Data states:** at rest (stored), in transit (moving across a network), in use (actively processed - usually requires the data to be unencrypted).

**Encryption by state:** at rest → FDE, SED, EFS. In transit → VPN, IPsec, TLS.

**Obfuscation techniques:**
- **Encryption** - reversible with the right key.
- **Hashing** - one-way, not meant to be reversed.
- **Data masking** - replaces sensitive data with fictitious data while keeping the original format.
- **Tokenization** - replaces sensitive data with a non-sensitive token, mapped back to the real data elsewhere.
- **Obfuscation** - the broader umbrella term for making data hard to understand.

**Segmentation as data protection:** limits attack spread, helps meet regulatory requirements, improves access control - but doesn't itself encrypt data in transit or guarantee recovery from deletion.

## Secure Enterprise Infrastructure

- **Security zones** - separating network areas by trust level (e.g. a DMZ for public-facing services vs. internal network).
- **Failure modes:** fail-open (allows traffic through on failure, prioritizes availability) vs. fail-closed (blocks traffic on failure, prioritizes security).
- **Network appliances:** jump server (hardened gateway for accessing other systems), proxy server (relays/filters/hides traffic), load balancer (distributes traffic across servers).
- **802.1X** - port-based network access control requiring authentication before a device gets network access.
- **Firewall types:** WAF (protects web apps specifically), UTM (all-in-one appliance bundling multiple security functions), NGFW (adds deep packet inspection and app awareness).
- **SD-WAN** - managing wide-area network connections via software.
- **SASE** - combines networking and security into a cloud-delivered service.

## Resilience & Recovery

**RAID levels:**
- **RAID 0 (striping)** - improves performance, **no fault tolerance** - any drive failing loses everything.
- **RAID 1 (mirroring)** - needs ≥2 drives; identical copies on each, so one drive failing doesn't lose data.
- **RAID 5 (striping with parity)** - needs ≥3 drives; tolerates one drive failure.
- **RAID 6 (striping with double parity)** - needs ≥4 drives; tolerates two simultaneous drive failures.
- **RAID 10 (stripe of mirrors)** - needs ≥4 drives; combines mirroring and striping for both performance and fault tolerance.

**Load balancing** (distributes workload for performance) vs. **clustering** (groups servers for high availability/fault tolerance).

**Disaster recovery site types:**
- **Hot site** - fully operational duplicate, near-complete backups, fastest recovery, most expensive.
- **Warm site** - some pre-installed hardware/software, not fully operational.
- **Cold site** - just the physical space, least expensive, slowest to activate.

**Backup techniques:** snapshot (point-in-time VM state), replication (real-time copy to a separate system), journaling (logs changes for recovery to the exact point of failure).

**Power redundancy:** PDU (distributes/monitors power), UPS (short-term backup power), backup generator (long-term backup power).

---

# Domain 4.0 - Security Operations

## Vulnerability Management

- **Vulnerability scanning** - passive; identifies gaps and misconfigurations without exploiting them.
- **Penetration testing** - active; bypasses controls and exploits vulnerabilities to prove real impact.
- **Responsible disclosure / bug bounty programs** - formal processes to encourage and reward vulnerability reporting.
- **Static code analysis** - examines code without executing it, used early in the SDLC.
- **Dynamic code analysis** - executes the code and observes runtime behavior, used later in the SDLC.
- **Package monitoring** - tracking third-party libraries/dependencies for known-vulnerable versions.
- **Threat intelligence:** OSINT (public sources), AIS (US-government real-time indicator sharing), STIX (the format for describing threat info), TAXII (the transport mechanism for sharing it), TTP (attacker tactics/techniques/procedures), ATT&CK (a framework built around understanding TTPs).
- **Detection accuracy:** false positive (flags something safe as malicious), false negative (fails to flag an actual threat), FRR (wrongly rejects a legitimate user), FAR (wrongly accepts an illegitimate user), CER (the point where FRR = FAR).
- **CVE** - a standardized catalog of publicly known vulnerabilities. **CVSS** - the scoring system for how severe a vulnerability is. **NVD** - adds CVSS scores and analysis to CVE entries.
- **SIEM** - collects and correlates log/event data to detect suspicious activity centrally. **SOAR** - automates the actual incident response.
- **EF (Exposure Factor)** - the % of an asset's value lost if a threat is realized.
- **Remediation techniques:** patching, insurance, segmentation, compensating controls, formal exceptions/exemptions.

## Access Control Models

- **MAC** - strictest; admin-set sensitivity labels/clearances, no user discretion.
- **DAC** - the resource owner decides who gets access.
- **RBAC** - permissions tied to job role.
- **Rule-based (RuBAC)** - access governed by explicit if/then rules (role + time + location, etc.).
- **ABAC** - most granular; combines multiple attributes (subject, action, resource, environment).
- **Time-of-day restrictions** - limiting when access is allowed.
- **Least privilege** - minimum access needed for the job.

## Password Concepts

- **Length and complexity** are the two key strength factors - complexity means mixing at least 3 of 4 character groups (upper/lower/digit/symbol).
- **Password expiration / maximum password age** - forces a mandatory change after a set period.
- **Minimum password age** - how long before a password can be changed again (prevents rapid cycling to dodge history rules).
- **Password history** - blocks reusing recent passwords.
- **Password reuse policy** - most effective at reducing breach risk across multiple accounts.
- **Passwordless authentication** - biometrics, hardware tokens, QR codes, OTPs, passkeys.
- **Salt** - random data added before hashing so identical passwords hash differently, defeating rainbow-table attacks.
- **Key stretching** - repeatedly hashes a password/key, making brute-force attempts computationally expensive.
- **Password attacks:** dictionary (word list vs. one account), spraying (a few passwords vs. many accounts, evades lockouts), brute force (exhaustive computing power vs. one account).

## Incident Response Activities

**4 stages, in order:**
1. **Preparation** - building the IR capability before anything happens (team, policy, tools, training).
2. **Detection and analysis** - identifying and understanding an incident's scope/impact/root cause.
3. **Containment, eradication, and recovery** - mitigating impact, eliminating the threat, restoring normal operations.
4. **Post-incident activity** - updating plans/policies based on lessons learned, reporting, root cause analysis.

- **Tabletop exercise** - discussion-based, no systems activated.
- **Simulation** - more hands-on, can involve activating real systems.
- **Root cause analysis** - investigating *why* an incident happened, to prevent recurrence.
- **Threat hunting** - proactively searching for indicators of compromise before they escalate.
- **Chain of custody** - a documented record of who handled evidence, preserving its integrity and court admissibility.
- **E-discovery** - collecting/producing electronically stored information for legal proceedings.

## Application Security

- **Input validation** - sanitizing user-submitted data before processing it, the core countermeasure against injection attacks.
- **Error/exception handling** - handling failures gracefully without leaking sensitive information.
- **Secure cookie** - only transmitted over HTTPS.
- **Fuzzing** - feeding an application malformed input to find how it breaks.
- **Code signing** - confirms an application's source and that it hasn't been tampered with.
- **Sandboxing** - safely executing untrusted code in an isolated environment.
- **ASLR** - randomizes memory locations to defend against memory-based attacks like buffer overflows.
- **CAPTCHA** - distinguishes humans from automated bots.

## Asset Management

- **Acquisition/procurement**, **ownership**, **classification** (categorizing by sensitivity), **inventory** (tracking assets), **enumeration** (actively discovering what's on the network).
- **Disposal:** sanitization (securely wiping data), destruction (physically destroying media), certification (documented proof of proper disposal).

## Alerting and Monitoring

- **Log aggregation** - collecting logs centrally.
- **Alert tuning** - adjusting sensitivity to reduce noise/false positives.
- **SCAP** - a standard for automating vulnerability and compliance checks.
- **NetFlow** - a tool for analyzing network traffic flow.

## Enterprise Capabilities

- **Screened subnet** (DMZ-style isolated segment for public-facing services).
- **Web filtering:** agent-based (software on the device) vs. centralized proxy.
- **Email security:** DMARC (policy for handling failed-authentication mail), DKIM (cryptographically signs email), SPF (lists servers allowed to send for a domain).
- **NAC (Network Access Control)** - enforces security requirements before allowing a device onto the network.
- **EDR / XDR** - EDR monitors/responds on individual endpoints; XDR extends that across network, email, and cloud.
- **UBA (User Behavior Analytics)** - detects anomalies against normal behavior patterns.

## Identity and Access Management

- **Federation** - trusting an identity from one organization across others, without a separate account everywhere.
- **SSO (Single Sign-On)** - log in once, access multiple systems. Enabled by LDAP, OAuth, SAML.
- **MFA factors:** something you know, something you have, something you are, somewhere you are.
- **PAM (Privileged Access Management):** just-in-time permissions, password vaulting, ephemeral credentials.

## Automation and Orchestration

- **Guard rails** - automated constraints preventing unsafe actions.
- **CI (Continuous Integration)** - frequent code merges with automated build/test, catching issues early.
- **Considerations:** complexity, cost, single points of failure, technical debt, ongoing supportability.

## Data Sources for Investigation

- Log types: firewall, application, endpoint, OS-level, IPS/IDS, network.
- Other sources: vulnerability scans, automated reports, dashboards, packet captures.

---

# Domain 5.0 - Security Program Management and Oversight

## Agreement Types

- **SLA (Service Level Agreement)** - performance requirements (uptime, response times).
- **MSA (Master Service Agreement)** - legally binding, foundational terms governing future agreements.
- **MOU (Memorandum of Understanding)** - nonbinding, general statement of intent.
- **MOA (Memorandum of Agreement)** - formal, often binding, specific terms.
- **SOW (Statement of Work)** - a specific project's scope, timeline, and cost.
- **WO (Work Order)** - authorizes and tracks a specific job/task.
- **NDA (Non-Disclosure Agreement)** - a confidentiality contract.
- **BPA (Business Partnership Agreement)** - a partnership's rights/responsibilities.
- **ISA (Interconnection Security Agreement)** - security requirements for connecting two organizations' systems.

## Penetration Testing

**Exercise teams:** Red (attacker), Blue (defender), White (referee/overseer), Purple (facilitates collaboration between red and blue).

**Knowledge levels:** White-box (full knowledge), Black-box (no prior knowledge), Gray-box (partial knowledge).

**Reconnaissance:** Passive (no direct interaction - OSINT, public records) vs. Active (direct interaction - pinging, port scanning, OS fingerprinting).

## Risk Management Concepts

**Process, in order:** Risk identification (finding risks) → Risk assessment (evaluating impact/likelihood) → ongoing risk management.

**Assessment frequency:** Ad hoc (reactive, event-triggered), Recurring (scheduled), One-time (defined project), Continuous (real-time).

**Qualitative** (subjective judgment, e.g. High/Medium/Low) vs. **Quantitative** (hard numbers/financial values).

**Quantitative formulas:**
- **SLE (Single Loss Expectancy) = AV × EF**
- **ALE (Annualized Loss Expectancy) = SLE × ARO**

**Risk tracking:**
- **Risk register** - the master document tracking identified risks over time.
- **Risk appetite** - general, strategic attitude toward risk.
- **Risk tolerance** - the specific level of risk an organization accepts for a given objective.

**Risk response strategies:** Avoidance (eliminate the risk), Transference (shift it, e.g. insurance), Mitigation (reduce impact/likelihood), Acceptance (proceed as-is - via exemption, a standing decision to skip a control, or exception, a temporary one).

**Recovery/reliability metrics:**
- **RTO** - maximum acceptable downtime.
- **RPO** - maximum acceptable data loss, in time.
- **MTTR** - average time to repair a failure.
- **MTBF** - average time between failures for a repairable system.
- **MTTF** - average time to first failure for a non-repairable system.

## Security Governance

- **Guidelines** (recommended) vs. **Standards** (mandatory).
- **Policies:** AUP, information security, business continuity, disaster recovery, incident response, SDLC, change management.
- **Roles:** Owner (accountable for the asset), Controller (decides how/why data is processed), Processor (processes data on the controller's behalf), Custodian/steward (day-to-day data management).

## Third-Party Risk Management

- **Vendor assessment:** penetration testing, right-to-audit clauses, evidence of internal audits, supply chain analysis.
- **Vendor selection:** due diligence (investigation before engaging a vendor).
- **Vendor monitoring** - ongoing oversight after onboarding.

## Security Compliance

- **Consequences of non-compliance:** fines, sanctions, reputational damage, loss of license.
- **Compliance monitoring:** due diligence/care, attestation and acknowledgement.
- **Privacy:** data subject (the individual data is about), right to be forgotten (e.g. under GDPR).

## Audits and Assessments

- **Internal audits:** compliance checks, audit committee, self-assessments.
- **External audits:** regulatory, independent third-party.
- **Penetration testing angles:** physical, offensive, defensive, integrated.

## Security Awareness Practices

- **Phishing campaigns** - simulated phishing tests for training.
- **Anomalous behavior categories:** risky, unexpected, unintentional.
- **User training topics:** insider threat awareness, password management, removable media risks, social engineering awareness, OPSEC, remote work security.
