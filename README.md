# SafePath - Smarter, Safer Journeys for Cyclists and Pedestrians

## Table of Contents
- [About SafePath](#about-safepath)
- [Who Is It For](#who-is-it-for)
- [Key Features](#key-features)
- [Why It Matters](#why-it-matters)
- [Tech Stack & Dependencies](#tech-stack--dependencies)
- [Installation Guide](#installation-guide)
- [How to Use](#how-to-use)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [Additional Documentation](#additional-documentation)
- [How to Get Help](#how-to-get-help)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## About SafePath

SafePath helps users discover safer walking and cycling routes across urban areas. Unlike standard navigation apps that focus only on the fastest route, SafePath evaluates **safety, comfort, and community-reported hazards**, helping users travel confidently.  

The goal is simple: provide smart route choices that minimize risks such as poor lighting, blocked lanes, or unsafe road conditions.

---

## Who Is It For

SafePath is designed for:

- Cyclists – beginners to daily commuters seeking safer, bike-friendly routes.  
- Pedestrians – students, workers, and evening walkers who want secure routes.  
- City planners and councils – to visualize community safety data and improve infrastructure.

Users can:

- Avoid unsafe or poorly lit areas  
- Find secure bike parking  
- Receive live alerts about hazards, weather, or blocked lanes  
- Share anonymous reports to improve safety

---

## Key Features

- Safe vs. Fast route options  
- Smart Safety Scoring based on lighting, traffic, and hazard data  
- Community Reports for real-time hazard tracking  
- Weather and lighting alerts  
- Secure parking finder for bicycles  
- Planned features: offline data access and gamification  

---

## Why It Matters

Active travel contributes to sustainable mobility, but safety concerns prevent many from cycling or walking. SafePath supports sustainable city initiatives by making walking and cycling safer, more convenient, and more attractive.

---

## Tech Stack & Dependencies

| Layer           | Technology             | Purpose                         |
|-----------------|----------------------|---------------------------------|
| Frontend        | React                | Interactive map and UI          |
| Backend         | Flask / Django       | REST APIs and data handling     |
| Database        | PostgreSQL + PostGIS | Spatial data storage            |
| Routing Engine  | OSMnx + NetworkX     | Route generation                |
| ML Model        | Python (Scikit-learn)| Safety scoring                  |
| Map Data        | OpenStreetMap        | Base maps                       |
| Tools           | GitHub, Jira, Figma  | Collaboration and design        |

**Dependencies:**

- Python ≥ 3.10  
- Node.js ≥ 18  
- PostgreSQL + PostGIS  
- Flask, SQLAlchemy, Pandas, OSMnx, NetworkX

---

## Installation Guide

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/SafePath.git
cd SafePath
