# 🛡️ Splunk SIEM — Interactive Study Guide & Lab Simulator

![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Splunk](https://img.shields.io/badge/Splunk_SIEM-000000?style=for-the-badge&logo=splunk&logoColor=white)
![Languages](https://img.shields.io/badge/Languages-ES_%7C_EN_%7C_TR-10B981?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

An interactive, multilingual (**Spanish 🇪🇸, English 🇬🇧, and Turkish 🇹🇷**) educational web application designed to help cybersecurity students and SOC analysts master the core architecture, data pipeline, and **SPL (Search Processing Language)** fundamentals of **Splunk SIEM**.

Built directly from handwritten study notes, this project transforms static diagrams into an interactive learning environment featuring live log parsing simulations, SPL visualizations, active-recall flashcards, and self-assessment quizzes.

---

## 🚀 Live Demo

Once deployed via **GitHub Pages**, you can access the live interactive application here:
> 🔗 **[View Live Application on GitHub Pages](https://tiag0-infosec.github.io/splunk-siem-notes/)** 
---

## 🎯 Purpose of This Repository

Understanding how a **SIEM (Security Information and Event Management)** platform ingests, normalizes, indexes, and visualizes security telemetry is a foundational skill in cybersecurity operations. 

This application bridges the gap between theoretical notes and practical SOC workflows by allowing users to:
1. **Visualize the End-to-End Architecture**: Explore how raw network and host logs travel from data sources into Splunk.
2. **Simulate Data Processing**: Observe how raw logs are parsed into key-value pairs and queried using **SPL**.
3. **Retain Key Concepts**: Practice with built-in flashcards and interactive quizzes across three languages.

---

## 🧠 Core Concepts Covered

### 1. The Three Pillars of Splunk SIEM
```text
Network ──(Logs)──► Splunk SIEM ──► [ Monitoring | Visibility | Observability ]
```
* **Monitoring**: Continuous real-time tracking of security events, system states, and network traffic.
* **Visibility**: Eliminating blind spots across the entire infrastructure (web servers, endpoints, Linux hosts, databases).
* **Observability**: Gaining deep insight into internal system states from external outputs (logs, metrics, traces) to investigate root causes and security incidents.

### 2. Splunk Architecture Pipeline

| Component | Role in Architecture | Key Details & Functions Covered |
| :--- | :--- | :--- |
| **1. Forwarder** | **Data Ingestion** *(Agent installed ➔ Sending data to Splunk instance)* | Collects telemetry from 4 primary sources:<br>• **Web Server** *(Web traffic)*<br>• **Windows Sysmon data** *(Windows Event, PowerShell)*<br>• **Linux** *(Host-centric logs)*<br>• **Database** *(DB requests, responses, errors)* |
| **2. Indexer** | **Main Role** *(Processing & Storage)* | Processes incoming raw streams in 4 stages:<br>• **Parses** *(Breaks streams into events & timestamps)*<br>• **Normalizes** *(Standardizes fields)*<br>• **Categorizes** *(Tags by host, source, sourcetype)*<br>• **Store** *(Compresses and writes to disk buckets)* |
| **3. Search Head** | **Analytics & Visualization** | Provides the analyst workspace:<br>• **Search and Report App**<br>• **SPL** *(Search Processing Language)*<br>• **Create Dashboard** *(Line, Pie, and Bar charts)*<br>• **Tables** *(Structured tabular outputs)* |

---

## ✨ Key Features of the Application

* 🗺️ **1. Interactive Architecture Map**: Clickable diagram of the Forwarder, Indexer, and Search Head with real-world raw log samples and detailed explanations.
* 💻 **2. End-to-End Pipeline & SPL Simulator**: Select any of the 4 log sources, inspect the raw log captured by the Forwarder, see how the Indexer extracts fields, and execute **SPL queries** to render live Bar Charts, Pie Charts, Line Charts (`timechart`), and Tables.
* 🗂️ **3. Active-Recall Flashcards**: Flip-cards with progress tracking ("Mastered" counter) to memorize every component and definition.
* 🏆 **4. Self-Assessment Quiz**: Multiple-choice practice exam with instant grading and detailed explanations for every answer.
* 📓 **Original Notebook Modal**: A built-in reference modal displaying the exact transcription of the original handwritten study sheet.
* 🌍 **Trilingual Interface**: Instant language switching between **Spanish (`ES`)**, **English (`EN`)**, and **Turkish (`TR`)**.
* 🌗 **Dark / Light Theme Toggle**: Designed with a cybersecurity SOC dark theme by default, with full support for light mode.

---

## 📁 Repository Structure

```text
📦 splunk-siem-study-guide
 ┣ 📄 index.html       # Self-contained single-file web application (React 18 + Tailwind CSS + Babel)
 ┣ 📄 App.jsx          # Modular React source component (for Vite / Node.js environments)
 ┗ 📄 README.md        # Project documentation
```

---

## 🛠️ How to Run Locally or Deploy

### Option 1: Zero-Setup Local Run (Single-File HTML)
Because `index.html` bundles React 18 and Tailwind CSS via CDN, no Node.js installation is required:
1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   ```
2. Double-click `index.html` to open it directly in any modern web browser.

### Option 2: Deploy on GitHub Pages
1. Push `index.html` and `README.md` to the `main` branch of your GitHub repository.
2. Go to your repository's **Settings** ➔ **Pages**.
3. Under **Build and deployment** ➔ **Branch**, select `main` and `/ (root)`, then click **Save**.
4. Wait ~60 seconds and visit `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`.

---

## 🤝 Contributing

Contributions, suggestions, and additional SPL query examples are welcome! Feel free to fork the repository and submit a pull request.

## 📄 License

This project is open-source and available under the **MIT License**.
