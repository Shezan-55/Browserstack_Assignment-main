# 🌐 BrowserStack Selenium Automation – End-to-End Testing Solution

---

## 📌 Project Overview

This project demonstrates a complete automation testing pipeline built using Selenium and executed across real devices and browsers using **BrowserStack Automate**.

The solution:

* Scrapes articles from the *El País Opinion* section
* Translates article titles using Google Translate API (via RapidAPI)
* Performs text frequency analysis
* Executes cross-browser tests in parallel on BrowserStack cloud infrastructure

It simulates a real-world **Customer Engineering / Pre-sales Automation scenario** involving:

* Environment validation
* Cloud execution
* API integration
* Parallel testing
* Logging & monitoring

---

## 🎯 Problem Statement

Build an automation framework that:

* Scrapes live dynamic content
* Integrates with external APIs
* Processes and analyzes text data
* Validates functionality across multiple browsers & devices
* Executes tests in parallel on cloud infrastructure

---

## 🏗 System Architecture

```
Local Python App (Selenium)
        │
        ▼
El País Website (Data Source)
        │
        ▼
Google Translate API (RapidAPI)
        │
        ▼
Text Analytics Engine
        │
        ▼
BrowserStack Cloud (Parallel Execution)
        │
        ▼
Execution Logs & Results
```

---

## 🔄 Execution Flow

### Phase 1 — Web Scraping

* Open El País Opinion section
* Extract first 5 valid articles
* Capture Spanish content
* Download article images

### Phase 2 — Data Processing

* Translate titles to English
* Normalize text
* Perform word frequency analysis

### Phase 3 — Cloud Testing

* Connect to BrowserStack Automate
* Execute Selenium tests on:

  * Windows Chrome
  * Windows Edge
  * macOS Safari
  * Samsung Galaxy S22
  * iPhone 13
* Run tests in parallel

---

## ☁ BrowserStack Test Strategy

| Category         | Coverage              |
| ---------------- | --------------------- |
| Desktop Browsers | Chrome, Edge, Safari  |
| Mobile Devices   | Android + iOS         |
| Execution Mode   | Parallel              |
| Test Type        | Functional Validation |

---

## ⚙ Technology Stack

### Automation

* Selenium 4
* WebDriver Manager

### Backend Processing

* Python 3
* Requests Library
* Collections (Text Analytics)

### Cloud Testing

* BrowserStack Automate
* Parallel Execution (Threading)

### API Integration

* RapidAPI – Google Translate

---

# 🔐 Environment Variables (.env Setup)

⚠ **Important:**
This project uses environment variables to securely store API credentials.
Do NOT hardcode sensitive keys in the source code.

---

## Step 1: Create `.env` File

Create a file named:

```
.env
```

Add the following:

```
# ==========================
# RapidAPI - Google Translate
# ==========================
RAPIDAPI_KEY=your_rapidapi_key_here

# ==========================
# BrowserStack Credentials
# ==========================
BROWSERSTACK_USERNAME=your_browserstack_username
BROWSERSTACK_ACCESS_KEY=your_browserstack_access_key
```

---

## Step 2: Install dotenv

```bash
pip install python-dotenv
```

---

## Step 3: Load Environment Variables in Python

```python
import os
from dotenv import load_dotenv

load_dotenv()

RAPIDAPI_KEY = os.getenv("RAPIDAPI_KEY")
BROWSERSTACK_USERNAME = os.getenv("BROWSERSTACK_USERNAME")
BROWSERSTACK_ACCESS_KEY = os.getenv("BROWSERSTACK_ACCESS_KEY")
```

---

## Step 4: Add `.env` to `.gitignore`

Create or update `.gitignore`:

```
.env
```

This prevents secrets from being pushed to GitHub.

---

# 🚀 Setup Instructions

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Configure Environment Variables

Create and configure your `.env` file as shown above.

### 4️⃣ Run Tests

```bash
python browserstack_test.py
```

---

## 📊 Logging & Monitoring

The framework provides:

* Device-specific execution logs
* API response validation logs
* Scraping progress tracking
* Error-safe exception handling
* Parallel execution status tracking

---

## 🧠 Engineering Highlights

✔ Dynamic website handling
✔ Explicit waits for stability
✔ Secure API credential management
✔ Cloud-based parallel automation
✔ Cross-device validation
✔ Clean modular architecture

---

---

## ⭐ Key Learning Outcomes

* Production-style Selenium automation
* API + automation system integration
* Cloud-based test infrastructure
* Parallel execution design
* Secure credential management
* Structured logging practices

---

## 👨‍💻 Author

Shaikh Shezan
Information Technology Engineering Student

---

## 🙏 Acknowledgements

* BrowserStack Cloud Testing Platform
* Selenium Open Source Community
* El País News Platform
