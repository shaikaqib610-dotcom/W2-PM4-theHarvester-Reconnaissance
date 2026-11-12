# W2-PM4 – Footprinting & Reconnaissance Using theHarvester

## Project Information

- **Project:** Week 2 – Project Module 4 (W2-PM4)
- **Training Organization:** NetworkWalks
- **Batch:** B084
- **Author:** Shaik Mahboob Mohiuddin
- **Tool:** theHarvester 4.11.1
- **Operating System:** Kali Linux
- **Target Domain:** `microsoft.com`

## 1. Project Overview

This project focuses on performing footprinting and reconnaissance using theHarvester in Kali Linux.

TheHarvester is an OSINT tool used to collect publicly available information about a target domain, including hostnames, subdomains, email addresses, and other relevant information from supported sources.

The practical exercise involved running searches using different data sources and exporting the collected results into JSON and XML formats.

## 2. Objectives

- Understand domain footprinting and reconnaissance.
- Explore theHarvester tool in Kali Linux.
- Identify publicly available hostnames and subdomains.
- Perform searches using different search engines.
- Export reconnaissance results in JSON and XML formats.
- Understand the importance of OSINT in cybersecurity.

## 3. Tools and Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Operating system |
| theHarvester 4.11.1 | OSINT and reconnaissance |
| Baidu | Information gathering source |
| DuckDuckGo | Information gathering source |
| JSON | Exported result format |
| XML | Exported result format |

## 4. Practical Implementation

### Task 1 – Reconnaissance Using Baidu

Command:

```bash
theHarvester -d microsoft.com -l 1000 -b baidu
```

**Results:**
- IP addresses: 0
- Email addresses: 0
- People: 0
- Hostnames: 9

### Task 2 – Reconnaissance Using DuckDuckGo

Command:

```bash
theHarvester -d microsoft.com -l 50 -b duckduckgo
```

**Results:**
- IP addresses: 0
- Email addresses: 0
- People: 0
- Hostnames: 27

Some discovered hostnames included:

- account.microsoft.com
- azure.microsoft.com
- careers.microsoft.com
- copilot.microsoft.com
- developer.microsoft.com
- docs.microsoft.com
- learn.microsoft.com
- support.microsoft.com
- visualstudio.microsoft.com

## 5. Exporting Results

The scan results were exported using the following commands:

**Baidu:**

```bash
theHarvester -d microsoft.com -l 1000 -b baidu -f task1-baidu
```

**DuckDuckGo:**

```bash
theHarvester -d microsoft.com -l 50 -b duckduckgo -f task2-duckduckgo
```

The tool generated the following files:

- `task1-baidu.json`
- `task1-baidu.xml`
- `task2-duckduckgo.json`
- `task2-duckduckgo.xml`

## 6. Important Technical Note

The project guide specified the use of the `all` data source. However, the installed theHarvester version 4.11.1 did not support the `all` source.

An attempt to execute the command resulted in an invalid source error. DuckDuckGo was therefore used as an alternative source.

The initial Baidu search returned 9 hostnames, while the subsequent Baidu export run returned 0 hostnames. The exported Baidu JSON and XML files reflect the later run.

## 7. Repository Structure

```text
W2-PM4-theHarvester-Reconnaissance/
│
├── README.md
│
├── Kali_Linux_Commands_Outputs.pdf
│
├── W2-PM4_theHarvester_Report.pdf
│
└── Output/
    ├── task1-baidu.json
    ├── task1-baidu.xml
    ├── task2-duckduckgo.json
    └── task2-duckduckgo.xml
