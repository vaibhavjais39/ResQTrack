# ResQTrack – Smart IoT Emergency Response System

An interactive mobile app UI/UX prototype for a real-time IoT-powered emergency response platform that integrates CCTV-based AI accident detection, automated alerting, and ambulance dispatch with intelligent routing.

---

## How to View the Prototype

Simply open `index.html` in any modern web browser — no build step, server, or dependencies required.

```bash
# Option 1: double-click index.html in your file explorer
# Option 2: open from terminal
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows
```

The prototype is self-contained: all CSS and JavaScript are embedded in the single HTML file.

---

## System Overview

ResQTrack connects CCTV cameras installed on roads and highways with an AI-powered computer vision engine. When the system detects a serious disturbance (car accident, landslide, fire, road hazard), it:

1. Classifies the incident and assigns a severity level (Minor / Moderate / Critical)
2. Automatically sends alerts to the **nearest police station** and **nearest hospital**
3. The hospital reviews the alert and dispatches an ambulance
4. The system calculates the **shortest, least-traffic route** and guides the ambulance driver in real time

---

## Screen-by-Screen Description

### Screen 1 – Login / Welcome
Role-based login screen with animated logo, live system statistics (camera count, active alerts, uptime), and three login buttons for **Police**, **Hospital**, and **Ambulance Driver** roles.

### Screen 2 – Live Monitoring Dashboard
Full overview with a styled SVG road map showing CCTV camera positions and pulsing red incident markers. Status strip shows Normal / Warning / Critical zone counts. Scrollable horizontal alert cards list active incidents. Quick-stats grid shows today's totals.

### Screen 3 – Incident Detection
Simulated CCTV feed with a detection bounding box overlay and AI confidence score. Incident details card shows location (NH-48, KM 234), GPS coordinates, severity badge (Critical), incident type, and detection timestamp. Alert banner confirms automatic notifications were sent to police and hospital.

### Screen 4 – Hospital Alert
Pulsing red emergency banner announces an incoming alert. Accident information card includes a mini-map showing hospital-to-incident distance (3.2 km), injured-person estimate, and elapsed time. Available ambulance units are listed; selecting one and pressing the large **DISPATCH AMBULANCE** button triggers a dispatch animation and navigates to the navigation screen.

### Screen 5 – Ambulance Navigation
Full-screen map showing the highlighted shortest route with turn-by-turn arrows. Top overlay card displays destination, ETA (8 min), and distance. Traffic condition chips (Clear / Moderate / Heavy) are positioned along the route. Bottom panel shows current speed, next turn instruction, a toggleable Siren button, and a Report Road Block button.

### Screen 6 – Emergency Status
Vertical timeline tracks every stage of the response (Detected → Alerts Sent → Dispatched → En Route → Arrived → Pickup → To Hospital → ER). An animated ambulance dot moves across a mini-map. Key metrics cards show Response Time, ETA, Distance Remaining, and Ambulance Unit. Communication buttons allow calling the ambulance, hospital, or police.

---

## Technology Context

| Layer | Technology |
|-------|-----------|
| IoT Sensors | CCTV cameras on roads / highways |
| AI Engine | Computer vision model for accident / hazard detection |
| Communication | Automated SMS / push alerts to police & hospital |
| Mapping | GPS coordinates + real-time traffic API for route optimisation |
| Navigation | Turn-by-turn routing with siren / road-block management |
| Frontend | Single-page HTML5 + CSS3 + Vanilla JS (this prototype) |

---

## File Structure

```
index.html   – Complete interactive prototype (HTML + CSS + JS)
README.md    – This file
```

---

## Credits

Built for academic presentation — ResQTrack IoT Emergency Response System Demo.
