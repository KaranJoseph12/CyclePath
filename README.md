# SafePath — Safety-Aware Routing

SafePath helps people choose safer walking or cycling routes. Alongside the fastest route, the app shows alternative routes that consider simple safety signals from public data and basic user reports. 

---

## 1) Problem and Goal

Most navigation tools optimise for speed/distance and rarely consider risk on street segments (for example, incident hotspots, poorly lit streets, hazardous junctions). SafePath adds a lightweight safety layer so users can compare Fastest vs Safer vs Safest options and make informed choices.

Goals
- Offer at least three route options per origin–destination query (Fastest, Safer, Safest).
- Use open data to compute a simple safety score for segments and surface risk cues.
- Gather basic user hazard reports to iteratively improve safety signals.

---

## 2) Target Users

- Students and young commuters  
- International residents and visitors  
- Daily urban walkers and cyclists  
- Local councils and planners  
- Community-oriented users who prefer to travel with others for safety and motivation

---

## 3) MVP Scope

- Web app (desktop and mobile-web friendly) focused on Manhattan  
- O/D input returns three route options visible on a map  
- Segment-level safety scoring from public data; simple risk cues on the map  
- Basic hazard reporting form for users

---

## 4) System Architecture (current choices)

Frontend
- React.js with Leaflet.js and OpenStreetMap tiles (no API key required)

Backend / API
- Python Flask REST API  
- Routing/graphs: OSMnx + NetworkX  
- Optional caching: Redis  
- Future scoring pipeline: scikit-learn (simple model)

Database
- PostgreSQL + PostGIS for geospatial data and user hazard reports

Rationale
- React + Leaflet keeps the prototype lightweight and fast to iterate.
- Flask + PostGIS supports geospatial queries with minimal overhead.
- OSMnx/NetworkX accelerate graph building/routing on open data.

---

## 5) Data Sources

- NYC Open Data: crime/incident and collision datasets  
- OpenStreetMap via OSMnx: street network and attributes  
- Optional contextual signals: weather where available  
- In-app user hazard reports (basic form)

Note: Store only small samples in `data/`. Keep large or frequently changing datasets external and link to the source.

---

## 6) Safety Score (baseline concept)

- Aggregate incident/collision counts to segments or nearby buffers.  
- Normalise by segment length and optionally time-of-day buckets.  
- Compose a simple score (for example, a weighted sum) and expose it as a per-segment risk cue in the UI.  
- Iterate using expert feedback and user reports.

This is intentionally simple for the MVP; refine weighting and signals during evaluation sprints.

---

## 7) Features (first cut)

- Map UI with three route options (Fastest, Safer, Safest)  
- Route details: inline risk cues (for example, incident density)  
- Hazard reporting: quick form tied to location  
- Placeholder panel for real-time alerts and simple rerouting (later sprint)

---

## 8) Evaluation Plan

Quantitative
- Historical validation: compare our Safer/Safest against a baseline on NYC data  
- Algorithm performance: response time, reliability, and simple scalability checks  
- Score validation: correlation with expert judgement and incident data  
- Route quality: safety-efficiency trade-offs and coverage across neighbourhoods

Qualitative
- Expert feedback (urban planning / road safety)  
- Literature/benchmark comparison  
- Case studies contrasting high- vs low-risk routes across NYC

Use evaluation results to tune weights in the short term and plan feature improvements in the medium term.

---

## 9) Success Criteria (MVP)

- Processes at least 95% of route requests successfully  
- Under 3 seconds average response time (local dev conditions)  
- At least 70% user satisfaction in early trials  
- Clear preference patterns and readiness to expand beyond Manhattan

---

## 10) Project Management

- Method: SCRUM with short, regular sprints (two weeks typical)  
- Rituals: daily stand-ups; sprint planning; sprint reviews and retrospectives  
- Tooling: Jira for sprint boards, backlog and task ownership; WhatsApp/Teams for comms

Indicative sprints
- Sprints 1–2: data pipeline and baseline routing  
- Sprints 3–4: safety scoring and frontend integration  
- Sprints 5–6: validation and optimisation, plus staging deploy

---

## 11) Security, Privacy, and Misuse

- Avoid exposing exact sensitive points in public UI; aggregate where possible  
- Keep personal data out of logs and exports  
- Consider request throttling and basic abuse monitoring  
- Keep any presence/matching features strictly opt-in with clear controls  
- Provide a simple reporting path for harmful content

---

## 12) Local Development — Setup and Run

Prerequisites
- Node.js 18+  
- Python 3.10+  
- PostgreSQL 14+ with PostGIS  
- Git installed

Clone
```bash
git clone https://github.com/<org-or-user>/<repo>.git
cd <repo>
