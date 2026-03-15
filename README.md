# 🏠 HomeNodeShowcase

**HomeNode** is a lightweight Raspberry Pi dashboard designed to monitor your home or apartment environment in real time.

It runs on a small desk-side display and provides a clean, always-on interface for viewing useful information like system stats, network activity, internet status, and weather.

HomeNode is built with simplicity in mind — minimal dependencies, a clean UI, and modular Python services.

## ✨ Features

* 🕒 **Live Time & Date**
* 🌤 **Local Weather**
* 🌐 **Network Device Monitor**
* 💻 **System Resource Monitoring**
* 📡 **Internet Connectivity Status**
* 📊 **Custom Personal Stats**

All information is displayed on a **minimal dashboard optimized for small displays**.

## 🖥 Example Dashboard Layout

```
┌───────────────┬───────────────┐
│ TIME          │ WEATHER       │
├───────────────┼───────────────┤
│ NETWORK       │ SYSTEM        │
├───────────────┼───────────────┤
│ INTERNET      │ STATS         │
└───────────────┴───────────────┘
```

Designed to run on a **Raspberry Pi with a small HDMI display** as a desk-side monitoring system.

## ⚙️ Tech Stack

**Backend**

* Python
* Flask
* psutil
* requests
* scapy

**Frontend**

* HTML
* CSS Grid
* Vanilla JavaScript

**Hardware**

* Raspberry Pi
* HDMI Display (7–10")

## 🧱 Architecture

HomeNode uses a modular design where each service collects data independently.

```
Modules
   ↓
Scheduler
   ↓
Cache
   ↓
Flask API
   ↓
Dashboard UI
```

This ensures the dashboard stays responsive while minimizing API calls and system load.

## 📂 Project Structure

```
homenode/

app.py
config.py
requirements.txt

modules/
    weather_module.py
    network_module.py
    system_module.py
    internet_module.py
    stats_module.py

services/
    scheduler.py
    cache.py

templates/
    dashboard.html

static/
    css/style.css
    js/dashboard.js

data/
    known_devices.json
```

## 🚀 Goals

HomeNode is designed to be:

* Lightweight
* Modular
* Expandable
* Easy to deploy on Raspberry Pi

Future modules may include:

* 📦 Package tracking
* 📊 Network bandwidth graphs
* 🔌 Smart plug energy monitoring
* 🧠 Home automation integrations

## 📸 Screenshots

*(Screenshots will be added once the dashboard UI is finalized.)*

## 🛠 Development

The active development version of HomeNode lives in a **separate private repository** used for testing and iteration before features are pushed to this showcase project.

## 📖 Usage

- Deploy on a Raspberry Pi connected to an HDMI display.
- Customize modules in the `modules/` directory for your needs.
- The dashboard auto-refreshes data via the scheduler service.

