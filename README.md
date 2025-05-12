# 📈 YouTube Trend Detector using n8n

A smart, automated **YouTube trend detection system** built using [n8n](https://n8n.io/). This workflow fetches recent video data from multiple channels, filters trending videos based on custom metrics (views, duration, etc.), and stores the data into Google Sheets for analysis or alerts.

---

## 🔧 Features

* ⏱ Automated using **Schedule Trigger** or manual run
* 📺 Fetches latest videos from YouTube channels
* 📊 Aggregates video statistics (views, duration, etc.)
* 🧹 Filters based on custom rules (e.g. views > X, duration < Y)
* 📩 Sends email summaries via Gmail
* 📄 Logs results in Google Sheets
* 🔁 Iterates over multiple channels from a single sheet

---

## 🧠 Workflow 1: Video Analysis & Email Summary

This workflow reads a list of channels from Google Sheets, fetches their recent videos, processes the data, and sends a summary via Gmail.

### 🔁 Flow Steps:

1. **Manual Trigger** – Start workflow
2. **Read Channel List** – Get list from Google Sheets
3. **Loop Over Each Channel**
4. **Aggregate Data** – Collect video stats
5. **Code Node** – Apply calculations (e.g., trending formula)
6. **Send Email via Gmail**
7. **Append Filtered Results to Sheet**



---

## 🧠 Workflow 2: Scheduled Trending Video Logger

This version is scheduled to run periodically and updates the Google Sheet with fresh data about videos from listed channels.

### 🔁 Flow Steps:

1. **Schedule Trigger** – Runs every X hours/days
2. **Read Channels from Sheet**
3. **Loop Over Channels**
4. **Fetch Recent Videos (getAll)**
5. **Get Video Details**
6. **Filter Trending Videos**
7. **Append to Google Sheet**


---


