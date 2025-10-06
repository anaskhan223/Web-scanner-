# Web-scanner-
# Enhanced Ethical Web Vulnerability Scanner

**A Python-based educational web vulnerability scanner** — designed for authorized penetration testing and learning.  
It crawls a target site (same domain), tests for common issues (reflected XSS, SQL error indicators), checks security headers, probes common sensitive files, and generates a clean HTML report.

> ⚠️ **Legal / Ethical Notice:** Only run this scanner against systems you own or have explicit written permission to test. Unauthorized scanning may be illegal and unethical.

---

## Features

- Same-domain website crawling with configurable depth and page limits  
- Reflected XSS detection (query parameters + form inputs) using non-destructive payloads  
- SQL injection detection (error-based checks) with common SQL error signature matching  
- Security header analysis (CSP, HSTS, X-Frame-Options, X-Content-Type-Options)  
- Sensitive files / paths discovery (e.g., `.env`, `robots.txt`, `.git/`)  
- HTML report generation with summary, detailed findings, timestamps, and recommendations  
- CLI with configurable options (delay, user-agent, max pages, depth, output file)

---

## Requirements

- Python 3.8 or later  
- Recommended packages:
  - `requests`
  - `beautifulsoup4`

Install dependencies:

```bash
python3 -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
pip install -r requirements.txt
