# Android Forensic Investigation Report

## 1. Case Overview

**Case Title:** Case 419  
**Date:** [03/07/2025]  
**Examiner:** Dare Adelaja  
**Case Summary:**  
This investigation involves the forensic examination of an Android disk image suspected to contain evidence of fraudulent activities. The analysis uncovered messages, and online behavior patterns indicative of cybercrime, particularly online financial fraud.

---

## 2. Tools and Methodology

**Tools Used:**
- Autopsy (Windows GUI version)
- 7-Zip (for unpacking compressed forensic image)
- Built-in Windows Snipping Tool (for capturing screenshots)

**Procedure:**
1. The provided `.gz` file containing the Android disk image was extracted using **7-Zip**.
2. The `.tar` file was added as a data source in **Autopsy GUI**.
3. The following Autopsy features were used to extract and analyze data:
   - **Communications**: SMS messages, call logs, and contacts
   - **Web Artifacts**: Browser history and downloads
4. Screenshots of findings were taken using Windows **Snipping Tool**.
5. A formal report was compiled based on the findings.

---

## 3. Key Findings

### 3.1 SMS Messages  
- Multiple messages suggesting fraudulent plans.
- **Example:**
  - _“Let's create a fake investment website and lure people into investing in a non-existent cryptocurrency. We'll promise huge returns.”_

### 3.2 Call Logs  
- Frequent calls to multiple international numbers.
- Multiple mobile phones


### 3.4 Browser History  
- Search terms included:
  - “how to know if efcc is tracking you”
  - “Scared Of Being Arrested By EFCC”


---

## 4. Analysis

The totality of evidence and browsing behavior — confirms that the device owner was engaged in fraudulent financial activities. The user actively used the device to organize, execute, and document fraud-related communication.

---

## 5. Conclusion

This Android image contains clear digital evidence linking the device owner to looming online frauds. The artifacts recovered indicate deliberate and organized cybercrime plans, warranting further law enforcement investigation.

---

## 6. Recommendations

- Forward the findings to appropriate cybercrime authorities.
- Analyze additional devices linked to the same identity or phone number.
- Cross-reference recovered files with known scam databases.

---

## 7. Screenshots

Below are selected screenshots from Autopsy analysis:

![SMS Evidence](./android-investigation/screenshots/sms_log.png)  
![Browser History](./android-investigation/screenshots/browser_activity.png) 


