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

## About SafePath

With SafePath, you can discover safer walking and cycling routes across urban environments. Our mission is simple: help users travel confidently by reducing risks like low lighting, crime hotspots, blocked lanes, and unsafe road conditions.

Unlike standard navigation apps that focus only on the fastest route, SafePath intelligently blends safety, comfort, and community awareness using open data and user-reported insights.

## Who Is It For

SafePath is designed for:

- Cyclists: from beginners to daily commuters seeking safer, well-lit, and bike-friendly routes.
- Pedestrians: students, workers, or evening walkers who want to feel secure and informed about their surroundings.
- City planners and councils: to visualize community safety data and improve active-travel infrastructure.

SafePath helps users:

- Avoid unsafe or poorly lit areas.
- Find secure bike parking spots.
- Receive live alerts about hazards, weather, or blocked lanes.
- Share anonymous reports to improve city safety for everyone.

## Key Features

- Safe vs. Fast Route Options: Choose between fastest, safest, or balanced routes.
- Smart Safety Scoring: Machine learning model evaluates lighting, traffic, and crime data.
- Community Reports: Users flag hazards, potholes, and unsafe zones in real time.
- Weather & Lighting Alerts: Stay informed about visibility and bad weather.
- Secure Parking Finder: Locate nearby cycle racks and safe resting points.
- Gamification Mode (coming soon): Earn badges for safe, eco-friendly travel.
- Offline Data (planned): Access routes and safety data even without network coverage.

## Why It Matters

Urban cycling and walking are key to sustainable mobility - but safety concerns stop many from choosing these eco-friendly options. SafePath supports Dublin's Vision Zero and Climate Action goals by making active travel safer and more attractive through technology.

## Tech Stack & Dependencies

| Layer           | Technology             | Purpose                         |
|-----------------|----------------------|---------------------------------|
| Frontend        | React                | Interactive map, clean UI       |
| Backend         | Flask / Django       | RESTful APIs & data handling    |
| Database        | PostgreSQL + PostGIS | Spatial data storage            |
| Routing Engine  | OSMnx + NetworkX     | Route generation & analysis     |
| ML Model        | Python (Scikit-learn)| Safety scoring                  |
| Map Data        | OpenStreetMap        | Open geospatial base            |
| Tools           | GitHub, Jira, Figma  | Collaboration & design          |

Dependencies:

- Python ≥ 3.10
- Node.js ≥ 18
- PostgreSQL + PostGIS
- Flask, SQLAlchemy, Pandas, OSMnx, NetworkX

## Installation Guide

1. Clone the repository.
2. Follow backend and frontend setup instructions.
3. Configure your database and environment variables.

## How to Use

- Open the app and enter your origin and destination.
- Choose between Fastest, Safest, or Balanced route.
- Explore route details - lighting, traffic, and nearby facilities.
- Report hazards or rate route safety for community data.
- Save favorite routes or export maps for offline viewing.

## Troubleshooting

| Issue                | Cause                        | Solution                       |
|----------------------|------------------------------|--------------------------------|
| App won't start      | Missing environment variables| Check .env setup               |
| No routes generated  | Database not connected       | Verify PostgreSQL & PostGIS setup |
| Map not loading      | API key error               | Recheck map provider credentials |

## Contributing

We welcome contributions from developers, designers, and researchers:

- Fork the repo
- Create a feature branch (`git checkout -b feature-name`)
- Commit and push changes
- Open a pull request

See `CONTRIBUTING.md` for more details.

## Additional Documentation

- Project Plan
- Personas & User Research
- Wireframes
- Evaluation Plan
- Future Expansion Ideas

## How to Get Help

- Email: safepath.team@gmail.com
- GitHub Issues: [Report a bug](https://github.com/yourusername/SafePath/issues)

## License

This project is licensed under the MIT License.

## Acknowledgements

SafePath was created as part of the MSc in Advanced Software Development at Technological University Dublin, under the mentorship of Dr. Brendan Tierney and collaboration of a passionate student team focused on sustainable urban mobility.
