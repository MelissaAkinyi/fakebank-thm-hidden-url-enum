# fakebank-thm-hidden-url-enum
Enumeration and exploitation of hidden endpoints in the FakeBank web application (TryHackMe) using dirb to uncover secret URLs and demonstrate potential unauthorized fund transfer risks.

# FakeBank TryHackMe – Hidden URL Enumeration

This repository documents my approach to discovering hidden and sensitive endpoints in the **FakeBank** web application on TryHackMe using directory brute-forcing with `dirb`. 

## Overview
- **Platform:** TryHackMe  
- **Challenge:** FakeBank  
- **Objective:** Find hidden URLs that expose sensitive functionality, leading to potential unauthorized actions (e.g., fund transfers).  

## Tools Used
- **Kali Linux**  
- **dirb** (with custom and common wordlists)  
- `curl` & browser developer tools  

## Methodology
1. **Reconnaissance** – Checked for exposed files (e.g., `robots.txt`, `sitemap.xml`)  
2. **Directory Enumeration** – Ran `dirb` against the target using:  
   ```bash
   dirb http://MACHINE_IP/ /usr/share/dirb/wordlists/common.txt -X .php,.txt,.bak,.old,.zip
