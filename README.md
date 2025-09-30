# Alexandria Emergency Alert Dashboard

A real-time emergency alert dashboard for Alexandria, VA that integrates live data from NOAA/NWS, USGS, Dominion Energy, and other OSINT (Reddit, Twitter, etc.) to provide street-level situational awareness for emergency managers and residents.

## 🚀 Features

Live NOAA/NWS Alerts
Pulls active weather alerts (flood, storm, coastal, etc.) from the NWS API


Automatic Updates
Dashboard refreshes every 30 seconds — no manual reload required.

Alert Prioritization
Alerts sorted by urgency (Urgent → Moderate → Minor).

Interactive Feedback
Users can mark alerts as 👍 or 👎 (only one can be active at a time).

Clean UI
Navy blue theme, urgency badges, time/location stamps, and icons for provenance.

Extensible
Planned integrations for Dominion Energy power outages, 911 dispatch, and social signal monitoring (Reddit/Twitter).


## 🖥️ Tech Stack

Frontend:

HTML5, CSS3

Vanilla JavaScript (ES6+)

Font Awesome for icons

Backend (optional):

Python (Flask or FastAPI) can be used as a proxy to fetch NOAA/NWS alerts (avoids CORS issues).

## 📡 Data Sources

NOAA/NWS Alerts API – api.weather.gov/alerts

NOAA CO-OPS Tides – water levels for Alexandria tide stations

USGS NWIS – Potomac and Four Mile Run river gauges

Dominion Energy Outage Map (ArcGIS REST) – localized power outages with ETAs

911 Dispatch / PulsePoint – Fire/EMS active calls (if public feed available)

Social Signals – Reddit, Twitter for protest/civil unrest detection

## ⚙️ Installation

Clone this repository:

git clone https://github.com/yourusername/alexandria-alert-dashboard.git
cd alexandria-alert-dashboard


Open the dashboard:

open alexandria_emergency_dashboard.html


(or just double-click the file in your file explorer)

If you’re using a backend proxy:

Set up Flask or FastAPI

Expose endpoint /api/alerts

Update fetchAlerts() in the JavaScript to point to your backend instead of directly to NOAA.

## 🔄 Auto-Refresh

The dashboard automatically updates every 30 seconds.
Change this interval in the JS code:

this.refreshInterval = 30000; // 30s

## 📌 Roadmap

 Integrate Dominion Energy outage polygons

 Add Alexandria Open Data (911/CAD feed)

 Hook up Reddit & Twitter API for civic signals

 Display map with live alert zones (Leaflet/Mapbox)

 Add user accounts + persistence for relevance feedback

## 🛡️ Disclaimer

This project is for educational and civic technology demonstration purposes only.
Data is pulled from public APIs (NOAA, USGS, Dominion Energy).
Always verify alerts with official sources (NOAA/NWS, City of Alexandria).
