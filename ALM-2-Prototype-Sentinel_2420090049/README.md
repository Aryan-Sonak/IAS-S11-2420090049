# Sentinel — Network Security Prototype

**Student:** Aryan Sonak  
**Roll Number:** 2420090049  
**Section:** 11

## Overview

Sentinel is a network security simulator that demonstrates how a firewall and an Intrusion Detection System (IDS) can be used to monitor network activity. It generates sample network traffic, checks packets against firewall rules and detection rules, and displays alerts on a dashboard.

All traffic is simulated inside the application. The project does not capture or block traffic on a real network interface.

## Main Features

- **Firewall management:** create, edit, enable and disable rules based on protocol, IP address and port.
- **Bastion host:** set a host as the main entry point for external traffic.
- **Traffic generator:** create normal traffic and sample activities such as port scans, SSH login attempts and SYN floods.
- **Intrusion detection:** detect suspicious activity using nine signature-based rules.
- **Anomaly detection:** compare traffic statistics with a baseline and raise alerts for unusual activity.
- **Alert dashboard:** view, filter, acknowledge and investigate alerts.
- **Guided labs:** try the detection features using the built-in scenarios.

## Technologies

- Python and FastAPI
- SQLite
- React and JavaScript
- Server-Sent Events for live updates

## Requirements

- Python 3.10 or later
- Node.js 18 or later
- npm

## Run the Project

From the project folder, start both parts using the launcher.

**Windows:**

```powershell
.\start-all.ps1
```

**Linux or macOS:**

```bash
./start-all.sh
```

You can also run the backend and frontend separately.

**Backend:**

```bash
cd backend
python -m venv .venv
pip install -r requirements.txt
uvicorn app.main:app --port 48731 --reload
```

**Frontend — in a second terminal:**

```bash
cd frontend
npm install
npm run dev
```

Open the frontend address shown in the terminal. The backend API documentation is available at `http://localhost:48731/docs`.

## Testing

Run the backend tests from the `backend/` folder:

```bash
python -m pytest -q
```

The `qa/` folder also contains API and browser-based test scripts.

## Screenshots

Project screenshots can be stored in `docs/img/`. The main pages to capture are the overview, firewall manager, hosts, traffic generator, alerts and anomaly detector.
