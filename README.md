# CVE-2020-10558: Tesla Model S/3/X Denial of Service (DoS)
**Security Researcher:** Jacob Archuleta ([@nullze](https://github.com/nullze))

## 📝 Vulnerability Overview
A critical Denial of Service (DoS) vulnerability was discovered in the Tesla Model 3, Model S, and Model X (all versions prior to 2020.4.10). This vulnerability allowed a remote attacker to crash the Chromium-based Infotainment system (MCU) via a specially crafted web page, resulting in the loss of critical vehicle functions including:
* Speedometer display
* Climate controls
* Autopilot visualizations and alerts
* Turn signal audio/visual feedback



## 🛠️ Technical Analysis
The vulnerability stems from an improper handling of specific web-based instructions within the vehicle's integrated browser. By leveraging a resource-exhaustion or process-termination vector, an attacker can force the `Model3-Icefish` (or equivalent MCU) process into an unresponsive state.

### **Attack Vector**
1. **Initial Access:** The victim navigates to a malicious URL via the Tesla in-car browser.
2. **Payload Execution:** The crafted HTML/JavaScript triggers the kernel-level process crash.
3. **Impact:** The CID (Center Information Display) goes black or freezes, effectively disabling the driver's interface to the vehicle's secondary systems.

## 🛡️ Remediation & Disclosure
I followed responsible disclosure protocols through the **Tesla Bugcrowd Bug Bounty Program**. Tesla verified the finding and issued a fleet-wide OTA (Over-the-Air) update (v2020.4.10) to mitigate the issue.

* **NVD Link:** [CVE-2020-10558](https://nvd.nist.gov/vuln/detail/CVE-2020-10558)
* **Status:** Resolved / Fixed
* **Accolades:** Recognized in the **Tesla Hall of Fame** for Security Research.

---
*Disclaimer: This repository is for educational and historical documentation purposes only. I am committed to the safety and security of the automotive ecosystem.*

Write-up available here: https://cylect.io/blog/Tesla_Model_3_Vuln/

Press:

https://cyber.vumetric.com/vulns/tesla/risk/high/

https://news.ycombinator.com/item?id=22641197

https://portswigger.net/daily-swig/web-based-attack-crashes-tesla-driver-interface

https://securityboulevard.com/2020/08/tesla-model-3-vulnerability-what-you-need-to-know-about-the-web-browser-bug/

https://dimov.pro/tesla-model-3-vulnerability-what-you-need-to-know-about-the-web-browser-bug/

https://www.securityweek.com/vulnerability-exposed-tesla-central-touchscreen-dos-attacks/

https://gridinsoft.com/blogs/is-researcher-found-that-the-tesla-model-3-interface-is-vulnerable-to-dos-attacks/

https://eurocybcar.com/enhttps:/eurocybcar.com/casos_crackeos/researcher-hacks-into-a-teslas-screen/

https://neomotor.epe.es/actualidad/tesla-model-3-este-es-el-problema-que-encontro-un-hacker-en-su-pantalla-DFNM4104

https://hackercar.com/que-descubrio-un-hacker-en-la-pantalla-de-este-tesla/

https://bugcrowd.com/nullze

https://sploitus.com/exploit?id=C087F7C1-D3CA-5595-B8C8-B1545B0F8B61

https://vulners.com/cve/CVE-2020-10558

https://www.cybersecurity-help.cz/vdb/SB2020032310

https://www.cisa.gov/news-events/bulletins/sb20-090-0

https://www.flu-project.com/2020/04/cve-2020-10558-en-tesla-model-3-Denegacion-servicio-completa-pantalla.html

https://www.secquest.co.uk/white-papers/exploring-common-vulnerabilities-in-self-driving-cars

https://labs.northit.co.uk/cve/2020/10558/

https://www.genians.com/platform/Tesla_Model_S_Car/?id=29144

Academia:

https://www.mdpi.com/2078-2489/15/1/14
