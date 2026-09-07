# SheeikLy (شيّك لي)
> **A Web-Based Tool for E-Commerce Trustworthiness & Credibility Detection**

![Status](https://img.shields.io/badge/Status-Completed%20%2F%20Portfolio%20Showcase-success)
![Python](https://img.shields.io/badge/Python-3.x-blue)
![Framework](https://img.shields.io/badge/Framework-Flask-green)
![Domain](https://img.shields.io/badge/Domain-Cybersecurity%20%2F%20GRC-red)

---

## Project Overview
As online shopping rapidly expands in Saudi Arabia under **Vision 2030**, distinguishing between legitimate stores and fraudulent/unregulated platforms has become a major consumer protection challenge. 

**SheeikLy (شيّك لي)** is an automated, web-based analytical tool designed to verify the credibility of e-commerce stores instantly. By simply submitting a target store URL, the system performs dynamic security analysis, extracts regulatory credentials, and outputs a transparent **Trustworthiness Report** with a weighted Trust Score (0%–100%).

> **Academic & Institutional Context:** Developed as a practical cybersecurity solution in collaboration with the **Ministry of Commerce (Abha Branch)** and **University of Bisha**.

---

## Key Features & Capabilities

- **Automated SSL & Domain Verification:** Real-time socket and SSL analysis to assess technical domain integrity.
- **Regulatory Credentials Extraction:** Automated detection and pattern matching for:
  - 10-digit Commercial Registrations (CR).
  - Freelance Certificates (`FL-` prefixes).
  - Saudi Business Center (SBC) authentication badges.
- **AI-Powered OCR Analysis:** Computer vision pipelines (Pillow + Tesseract OCR) to extract text directly from visual certificates and footer badges.
- **Policy & Contact Scraping:** NLP-driven regex search to confirm refund/privacy policies, WhatsApp channels, and Saudi phone formats.
- **Stealth Automation & Resilience:** Anti-bot bypass configurations (Nodriver) combined with robust exception handling for restricted or blocked websites.

---

## System Architecture & Workflow

The verification execution pipeline operates across 6 distinct phases:
[ User Inputs URL ]
│
▼
[ Phase 1: SSL & Socket Domain Analysis ]
│
▼
[ Phase 2: Stealth Browser Rendering & Screenshot Capture ]
│
▼
[ Phase 3: AI-Vision OCR Parsing + HTML Text Cleaning (BeautifulSoup) ]
│
▼
[ Phase 4: NLP Regex Matching (CRs, Policies, Contact Info) ]
│
▼
[ Phase 5: Weighted Scoring Algorithm Engine ]
│
▼
[ Phase 6: Color-Coded Trust Report (Safe / Suspicious / Unsafe) ]
### Weighted Trust Score Calculation
The final Trust Score is calculated dynamically using predefined metrics:
- **Commercial Registration (CR):** 45%
- **Platform Authentication (Salla / Zid):** 30%
- **Domain Security (SSL):** 20%
- **Contact & Policy Transparency:** 15%
- **Content Quality & Media Verification:** 5%

---

## Tech Stack & Dependencies

- **Backend & Web Server:** Python, Flask, Asyncio
- **Automation & Scraping:** Nodriver, BeautifulSoup4
- **Computer Vision & OCR:** Tesseract OCR, Pillow (PIL)
- **Security & Data Analytics:** Python SSL/Socket Libraries, Regex (Regular Expressions)

---

## System UI & Test Cases

| Scenario | Result / Report Output |
| :--- | :--- |
| **Fully Compliant Store (Green)** | High Trust Score (95%-100%) with verified CR and SSL. |
| **Missing Documentation (Orange)** | Flagged warnings for missing/unverified official licenses. |
| **Restricted / Protected Site (Red/Notice)** | Graceful fallback prompting manual inspection guidelines. |

---

## License & Intellectual Property Notice

**Copyright (c) 2026 Yasmin Saeid Alamri. All Rights Reserved.**

This repository is published **strictly for display, exhibition, and portfolio showcase purposes**. The complete source code, core proprietary algorithms, and backend implementation are kept in a **private repository** for intellectual property and security reasons.

**Strict Restrictions:**
- No permission is granted to copy, clone, duplicate, or reverse-engineer the codebase or concept.
- Modification, distribution, or commercial usage of any part of this project is strictly prohibited.
