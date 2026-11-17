# NETWORKWALKS-Amna-B084-W3-CyberSecurity-Password-Cracking-
Password cracking and cryptographic hash analysis lab (W3-PM1 &amp; W3-PM2) using John the Ripper (Johnny) and Networkwalks Tools.
## 📌Overview
During Week 3 of the Networkwalks Cybersecurity Internship, I focused on password security auditing, cryptographic hash extraction, and offline/online password recovery. Using both local GUI tools and browser-based utilities, I audited four encrypted PDF files (`$pdf$4*4*128*` format) to demonstrate how weak or predictable passwords can be recovered during authorized security assessments.

### Modules Completed
* **W3-PM1:** Offline Password Recovery with John the Ripper (Johnny GUI)
* **W3-PM2:** Online Hash Extraction & Auditing with Networkwalks Tools

---

## 🛠️ Tools & Environment
| Tool / Component | Purpose |
| :--- | :--- |
| **Windows OS** | Host environment for running local cracking tools |
| **Johnny (JTR GUI)** | Graphical frontend for John the Ripper used for offline dictionary attacks |
| **File Conversion Tool** | Extracts raw password hashes from encrypted PDF files into `.txt` format |
| **Networkwalks Hash Calculator** | Browser-based utility for extracting hashes from protected PDFs |
| **Networkwalks Password Cracker** | Online wordlist auditing tool used to test hash strength |

---

## 🚀 Practical Execution & Methodology

### 1. W3-PM1 — Password Cracking with Johnny (John the Ripper GUI)
**Objective:** Extract cryptographic hashes from three password-protected PDF documents, execute offline dictionary attacks using Johnny GUI, and unlock each file to retrieve the hidden flags.

**Steps Performed:**
1. Configured **Johnny** (John the Ripper GUI) on my Windows machine.
2. Used the **File Conversion Tool** to extract the underlying password hashes from `My Locked PDF1.pdf`, `My Locked PDF2.pdf`, and `My Locked PDF3.pdf`, saving them as `hash1.txt`, `hash2.txt`, and `hash3.txt`.
3. Loaded each hash file into Johnny (`Open password file`) and initiated a dictionary attack (`Start new attack`).
4. Achieved a **100% recovery rate** across all three targets and unlocked the PDFs to verify access and capture the embedded flags.

#### 📊 W3-PM1 Results Summary
| Target Document | Hash File | Recovered Password | Status |
| :--- | :--- | :--- | :--- |
| `My Locked PDF1.pdf` | `hash1.txt` | `good-luck` | ✅ Unlocked & Flag Captured |
| `My Locked PDF2.pdf` | `hash2.txt` | `password1` | ✅ Unlocked & Flag Captured |
| `My Locked PDF3.pdf` | `hash3.txt` | `1qaz2wsx` | ✅ Unlocked & Flag Captured |

---

### 2. W3-PM2 — Password Cracking with Networkwalks Tools
**Objective:** Perform online hash extraction and password auditing on a fourth encrypted document (`My Locked PDF1 (for NW Tools Lab WK3-PM2).pdf`) using Networkwalks' web utilities, and cross-verify previous results.

**Steps Performed:**
1. Opened the **Networkwalks Hash Calculator** and uploaded `My Locked PDF1 (for NW Tools Lab WK3-PM2).pdf` to extract its password hash.
2. Submitted the extracted hash into the **Networkwalks Password Cracker** to test against available wordlists.
3. Successfully recovered the plaintext password (`password1`), unlocked the PDF, and retrieved the final flag.
4. Cross-checked the three PDFs from W3-PM1 using the Networkwalks online portal, confirming identical recovery results across both offline and online methods.

#### 📊 W3-PM2 Results Summary
| Target Document | Tool Used | Recovered Password | Status |
| :--- | :--- | :--- | :--- |
| `My Locked PDF1 (for NW Tools Lab WK3-PM2).pdf` | Networkwalks Online Tools | `password1` | ✅ Unlocked & Flag Captured |

---

## 💡 Key Takeaways & Security Recommendations
* **Predictable Patterns Are Vulnerable:** Passwords like `password1` and keyboard walks like `1qaz2wsx` appear in almost every standard wordlist and are cracked within seconds.
* **Enforce Length & Complexity:** Use passphrases of **12+ characters** combining uppercase, lowercase, numbers, and special symbols.
* **Avoid Password Reuse:** Never reuse passwords across multiple documents, portals, or accounts—a single leaked hash can compromise everything.
* **Use Strong Hashing Algorithms:** Systems should store credentials using modern, slow, salted hashing algorithms (such as `bcrypt`, `Argon2`, or `yescrypt`) rather than fast, legacy hashes.

---
##  Ethical Disclaimer
All password-cracking exercises and hash audits documented in this repository were conducted strictly within an authorized educational lab environment using sample files provided by Networkwalks Academy. Unauthorized password recovery or system access is illegal and unethical.

##  Acknowledgment
Special thanks to **Networkwalks Academy** and my mentor **Waqas Karim (CCIE)** for designing hands-on labs that bridge theoretical cryptography with practical security auditing.

Compiled during Week 3 of the Networkwalks Cybersecurity Program (Batch B084).

Amna Khan  

Cybersecurity & Digital Forensics Student | Batch B084 

LinkedIn:https://www.linkedin.com/in/amna-k-1b8ba83a9/ 
