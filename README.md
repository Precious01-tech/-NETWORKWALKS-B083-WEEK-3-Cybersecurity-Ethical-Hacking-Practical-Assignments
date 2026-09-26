# NETWORKWALKS B083 | WEEK 3
### Cybersecurity & Ethical Hacking Practical Assignments

This repository documents the practical labs completed during Week 3 of the Networkwalks Cybersecurity & Ethical Hacking program.

---

## 📋 Week 3 Projects

| # | Project | Skills |
|---|---------|--------|
| 01 | [Password Cracking with John the Ripper](#01-password-cracking-with-john-the-ripper) | John the Ripper, Johnny, Hash Extraction |
| 02 | [Password Cracking with Networkwalks Tools](#02-password-cracking-with-networkwalks-tools) | Hash Calculator, Browser-based Cracking |
| 03 | [Setting Up HexStrike MCP Server](#03-setting-up-hexstrike-mcp-server) | MCP Configuration, Claude Desktop, Linux |

### Skills Demonstrated
- Password security testing
- Hash extraction
- John the Ripper / Johnny
- Browser-based password-cracking tools
- Password-cracking workflows
- Linux administration
- Python virtual environments
- MCP server configuration
- Claude Desktop integration
- Troubleshooting
- Technical documentation

---

## 01. Password Cracking with John the Ripper

### Objective
Use John the Ripper (JTR) and its graphical interface, Johnny, to recover the passwords of three protected PDF files in a controlled cybersecurity learning environment.

### Tools Used
- Kali Linux / Windows
- John the Ripper (JTR) 1.9.0-jumbo-1
- Johnny GUI
- PDF Hash Extractor
- Authorized protected PDFs: `My-Locked-PDF1.pdf`, `PDF2`, `PDF3`

### Workflow

**1. Configure Johnny**
Johnny was configured to point at the John the Ripper executable, with Jumbo John selected for broader hash/attack-mode support.

**2. Extract PDF Hashes**
Hashes were extracted for all three protected PDFs.

**3. Load Hashes into Johnny**
Each extracted hash was loaded into Johnny via **Open Password File**.

**4. Start the Attack**
**Start New Attack** was run against each loaded hash.

**5. Recover the Passwords**
John the Ripper successfully cracked all three hashes, recovering each PDF's password.

**6. Verify the Results**
Each recovered password successfully unlocked its corresponding PDF.

### Result
✅ Passwords for all three authorized test PDFs were successfully recovered using John the Ripper via Johnny.

### What I Learned
- How password-protected files can be tested with John the Ripper
- How to extract a PDF hash for password-security testing
- How to use Johnny as a graphical interface for JTR
- How password complexity affects cracking time
- The importance of strong passwords for protecting sensitive files

### Evidence
| Screenshot | Description |
|---|---|
| 

![Johnny Settings](screenshots/jonny%20john.exe.png)

 | Johnny configured with the John the Ripper executable path |
| 

![PDF1 Hash](screenshots/pdf%201%20hash%20jtr.png)

 | Hash extracted for PDF1 |
| 

![PDF2 Hash](screenshots/jtr%20hash%202%20pdf%202.png)

 | Hash extracted for PDF2 |
| 

![PDF3 Hash](screenshots/jtr%20hash%203%20pdf%203.png)

 | Hash extracted for PDF3 |
| 

![Cracked PDF1](screenshots/jtr%20cracked%20password%20pdf1.png)

 | Johnny result — PDF1 password cracked |
| 

![Cracked PDF2](screenshots/jtr%20cracked%20password%20pdf%202.png)

 | Johnny result — PDF2 password cracked |
| 

![Cracked PDF3](screenshots/jtr%20cracked%20password%20pdf%203.png)

 | Johnny result — PDF3 password cracked |
| 

![Unlocked PDF1](screenshots/jtr%20unlocked%20pdf%201.png)

 | PDF1 successfully unlocked |
| 

![Unlocked PDF2](screenshots/jtr%20unlocked%20pdf%202.png)

 | PDF2 successfully unlocked |
| 

![Unlocked PDF3](screenshots/jtr%20unlocked%20pdf%203.png)

 | PDF3 successfully unlocked |

> **Security Note:** This exercise was performed in an authorized cybersecurity learning environment. Recovered passwords and hashes are lab-specific practice credentials generated for training purposes.

---

## 02. Password Cracking with Networkwalks Tools

### Objective
Use the Networkwalks Hash Calculator and Password Cracker to recover the passwords of the same three protected PDF files, using a browser-based workflow.

### Tools Used
- Networkwalks Hash Calculator
- Networkwalks Password Cracker
- Web Browser
- Authorized protected PDFs: `PDF1`, `PDF2`, `PDF3`

### Workflow

**1. Obtain the Protected PDFs**
Three authorized encrypted PDFs were used for this exercise.

**2. Extract the PDF Hashes**
Each PDF was uploaded to the Networkwalks Hash Calculator, which parsed it locally and generated a crackable hash in `pdf2john`/hashcat-compatible format.

**3. Load Hashes into the Password Cracker**
Each extracted hash was pasted into the Networkwalks Password Cracker.

**4. Start the Cracking Process**
The cracking process was run against each hash until a match was found.

**5. Recover the Passwords**
All three PDF passwords were successfully recovered.

**6. Verify the Results**
Each recovered password successfully unlocked its corresponding PDF.

### Result
✅ Passwords for all three authorized test PDFs were successfully recovered using the Networkwalks Hash Calculator and Password Cracker.

### What I Learned
- How to extract a password hash from a protected PDF
- How browser-based password-cracking tools work
- Why the complete hash must be copied correctly
- How password complexity can affect cracking time
- Why strong passwords are important for protecting files and sensitive information

### Evidence
| Screenshot | Description |
|---|---|
| 

![PDF1 Locked](screenshots/pdf%201%20locked.png)

 | PDF1 shown as protected/locked in the Hash Calculator |
| 

![PDF1 Password](screenshots/pdf%201%20password.png)

 | PDF1 password recovered by the Password Cracker |
| 

![PDF1 Unlocked](screenshots/pdf%201%20unlocked.png)

 | PDF1 successfully opened |
| 

![PDF2 Locked](screenshots/pdf%202%20locked.png)

 | PDF2 shown as protected/locked |
| 

![PDF2 Password](screenshots/pdf%202%20password.png)

 | PDF2 password recovered |
| 

![PDF2 Unlocked](screenshots/pdf%202%20unlocked.png)

 | PDF2 successfully opened |
| 

![PDF3 Locked](screenshots/pdf%203%20locked.png)

 | PDF3 shown as protected/locked |
| 

![PDF3 Password](screenshots/pdf%203%20password.png)

 | PDF3 password recovered |
| 

![PDF3 Unlocked](screenshots/pdf%203%20unlocked%20.png)

 | PDF3 successfully opened |

> **Security Note:** This exercise was performed as part of an authorized cybersecurity learning lab. Hashes and recovered passwords are lab-specific practice credentials generated for training purposes.

---

## 03. Setting Up HexStrike MCP Server

### Objective
Set up the HexStrike AI MCP Server on Kali Linux and integrate it with Claude Desktop.

### Lab Environment
- Kali Linux VM
- Claude Desktop
- HexStrike AI MCP Server
- Python
- Git
- Python virtual environment
- Local MCP server

### Workflow

**1. Install Claude Desktop**
Claude Desktop was installed on Kali Linux via the Debian repository (GPG key added, repo registered, then installed with `apt`).

**2. Download HexStrike AI**
The HexStrike AI repository was cloned from GitHub to `/home/kali/hexstrike-ai/`.

**3. Create a Python Virtual Environment**
A dedicated virtual environment, `hexstrike-env`, was created and activated.

**4. Install Dependencies**
Required Python packages were installed from `requirements.txt`.

**5. Start the HexStrike API Server**
\`\`\`bash
python3 /home/kali/hexstrike-ai/hexstrike_server.py
\`\`\`
The server started successfully, confirmed by the "HEXSTRIKE" banner and process pool workers initializing.

---

👤 Author

Name: Kehinde Precious Akinyami

Role: Cybersecurity Student / Intern (Batch B083)

Program: NetworkWalks Cybersecurity Internship

LinkedIn:** https://www.linkedin.com/in/kehinde-precious-akinyami-5015133a2

GitHub: Precious01-tech
