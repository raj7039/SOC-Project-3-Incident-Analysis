# 📧 Phishing Email Analysis

## 📌 Objective
Analyze a suspicious phishing email to identify malicious indicators, 
extract IOCs, and validate threat using threat intelligence tools.

## 🛠 Tools Used
- VirusTotal
- Manual email header analysis
- IOC extraction techniques

## 🎯 MITRE ATT&CK
- Technique: T1566 — Phishing
- Sub-technique: T1566.002 — Spear Phishing Link

## ⚙️ How It Works

### Step 1 — Email Received
- Received suspicious email reported by simulated user
- Email claimed to be from a legitimate organization
- Contained urgent language and suspicious link

### Step 2 — Header Analysis
- Extracted sender email address and IP
- Identified spoofed display name vs actual sender domain
- Checked SPF, DKIM, DMARC records

### Step 3 — IOC Extraction
- Extracted all URLs from email body
- Extracted sender IP address
- Extracted domain name
- Noted suspicious attachment (if any)

### Step 4 — VirusTotal Validation
- Submitted extracted URL to VirusTotal
- Submitted sender IP to VirusTotal
- Submitted domain to VirusTotal
- Reviewed detection results from multiple security vendors

### Step 5 — Verdict
- URL flagged as malicious by multiple vendors
- Domain identified as phishing infrastructure
- Email confirmed as malicious phishing attempt

## 📊 IOCs Found
- Malicious URL: identified and blocked
- Spoofed sender domain: identified
- Attacker IP: flagged on VirusTotal

## 🛡️ SOC Response Steps
1. Block sender domain at email gateway
2. Search SIEM for same email received by other users
3. Alert all users about phishing campaign
4. Submit IOCs to threat intelligence platform
5. Document incident with full IOC list
6. Escalate if any user clicked the link

## 🎓 Skills Demonstrated
- Phishing email analysis
- IOC extraction (URL, domain, IP, sender)
- VirusTotal threat intelligence validation
- Incident documentation
- MITRE ATT&CK mapping — T1566
