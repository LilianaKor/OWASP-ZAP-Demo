# OWASP-ZAP-Demo
This project demonstrates how to safely and legally scan a website using OWASP ZAP on macOS for educational purposes. The goal is to create a clear, recruiter-friendly GitHub project showcasing your basic cybersecurity skills.
# OWASP ZAP Demo: Legal Website Scanning for GitHub Portfolio

## Project Goal

This project demonstrates how to safely and legally scan a website using OWASP ZAP on macOS for educational purposes. The goal is to create a clear, recruiter-friendly GitHub project showcasing your basic cybersecurity skills.

## Legal Target Website for Scanning

You can only scan websites that explicitly allow security testing.

### Recommended Target:

**[http://testphp.vulnweb.com](http://testphp.vulnweb.com)**

* Provided by Acunetix
* Intentionally vulnerable
* Fully legal to scan

**Important:** Never scan real-world or commercial websites without written permission. Use only official test environments.

## Tools Used

* OWASP ZAP for macOS
* Google Chrome or Firefox
* FoxyProxy (optional)
* OBS Studio or Loom (for video recording)
* GitHub

---

## Step-by-Step: Create a ZAP Scanning Demo

### 1. Install OWASP ZAP

* Download from [https://www.zaproxy.org/download/](https://www.zaproxy.org/download/)
* Choose the macOS (Apple Silicon) version
* Drag it to Applications and launch it

### 2. Start New ZAP Session

* Open ZAP
* Select "Start a new session"
* Leave default options and click OK

### 3. Set Up Browser Proxy (Chrome example)

* Open Chrome → Settings → Advanced → System → Open Proxy Settings
* Set HTTP proxy to:

  * Host: 127.0.0.1
  * Port: 9090 (or match the port in ZAP: Tools → Options → Local Proxies)

Tip: Use the FoxyProxy extension for easy proxy switching.

### 4. Visit Target Site via Proxy

* In the browser (with proxy ON), go to [http://testphp.vulnweb.com](http://testphp.vulnweb.com)
* ZAP should display the site in the "Sites" tab

### 5. Launch Active Scan

* Right-click on `http://testphp.vulnweb.com` in ZAP
* Select: Attack → Active Scan
* Leave default settings, then Start Scan

### 6. View Results

* Track progress in the Active Scan tab
* Review vulnerabilities and recommendations

### 7. Export the Report

* Go to: Report → Generate HTML Report
* Save the report as `zap_report.html`

### 8. (Optional) Manual Payload Test Example

Test fields with the input: `"><script>alert(1)</script>`

* This is a classic XSS test string used to simulate JavaScript injection
* Use only in controlled environments like this test site

---

## Project Structure

```
OWASP-ZAP-Active-Scan-Demo/
├── zap_report.html
├── README.md
├── demo_video.mp4 (optional)
└── scan_screenshot.png (optional)
```

---

## Sample README.md 

```markdown
# OWASP ZAP Active Scan – Legal Demo Project

## Overview
This demo shows how to use OWASP ZAP to perform a legal security scan against a vulnerable test website.

## Target Website
http://testphp.vulnweb.com (provided by Acunetix)

## Tools Used
- OWASP ZAP (macOS)
- Chrome + Proxy
- GitHub

## Steps Performed
1. Launched ZAP
2. Configured browser proxy (127.0.0.1:9090)
3. Visited test site through proxy
4. Started Active Scan
5. Saved HTML report

## Ethics
This scan was performed only on a legally authorized, intentionally vulnerable test site.

## Report
See `zap_report.html` in this repository.

## Video Walkthrough
See `demo_video.mp4` (coming soon)
```


**Option B: Upload to YouTube or Loom (recommended)**

* Upload the video
* Add the video link to the `README.md` like this:

```markdown
## Video Walkthrough
Watch here: https://your-video-link.com
```
