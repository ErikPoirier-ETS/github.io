---
title: "Projects"
description: "Construction projects analyzed as part of our research."
image: "/images/projects.png"
layout: "projects"
draft: false
---

## Interactive Project Map

<div id="map" style="width: 100%; height: 480px; border-radius: 16px; border: 1px solid #e5e5e5; margin-bottom: 2rem;"></div>

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script>
document.addEventListener('DOMContentLoaded', function() {
    const projects = [
        { name: "SQI Administrative Building", address: "Québec, QC", type: "Institutional", owner: "SQI", coords: [46.8139, -71.2080] },
        { name: "MTMD Road Infrastructure", address: "Montréal, QC", type: "Infrastructure", owner: "MTMD", coords: [45.5017, -73.5673] },
        { name: "SHQ Social Housing", address: "Laval, QC", type: "Residential", owner: "SHQ", coords: [45.6066, -73.7124] },
        { name: "HQ Substation", address: "Trois-Rivières, QC", type: "Energy", owner: "Hydro-Québec", coords: [46.3432, -72.5477] },
        { name: "Community Center", address: "Montréal, QC", type: "Municipal", owner: "City of Montreal", coords: [45.5231, -73.6004] },
        { name: "Heritage Building", address: "Québec, QC", type: "Municipal", owner: "City of Quebec", coords: [46.8123, -71.2145] },
    ];
    
    const map = L.map('map').setView([46.5, -72.5], 6);
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', { attribution: '© OpenStreetMap' }).addTo(map);
    
    const icon = L.divIcon({
        className: 'marker',
        html: '<div style="width:24px;height:24px;background:#1e40af;border:3px solid white;border-radius:50%;box-shadow:0 2px 6px rgba(0,0,0,0.3);"></div>',
        iconSize: [24, 24],
        iconAnchor: [12, 12],
        popupAnchor: [0, -16]
    });
    
    projects.forEach(function(p) {
        L.marker(p.coords, { icon: icon })
            .addTo(map)
            .bindPopup('<strong>' + p.name + '</strong><br>' + p.address + ' · ' + p.owner + '<br><span style="background:#dbeafe;color:#1e40af;padding:2px 8px;border-radius:12px;font-size:0.75rem;">' + p.type + '</span>');
    });
});
</script>

---

## Pilot Projects (examples)

{{< notice "note" >}}
The projects shown below are representative examples. Our complete sample includes **450 projects** split between 200 non-BIM and 250 BIM-enabled projects.
{{< /notice >}}

| Project | Location | Owner | Type |
|---------|----------|-------|------|
| Administrative Building | Québec, QC | SQI | Institutional |
| Road Infrastructure | Montréal, QC | MTMD | Infrastructure |
| Social Housing | Laval, QC | SHQ | Residential |
| Electrical Substation | Trois-Rivières, QC | Hydro-Québec | Energy |
| Community Center | Montréal, QC | City of Montreal | Municipal |
| Heritage Building | Québec, QC | City of Quebec | Municipal |

---

## Methodology

The project is delivered following an **Action-Design Research (ADR)** approach, undertaken within six partner organizations.

{{< accordion "Methodology Steps" >}}

1. **Problem Formulation** — Define measurement strategies
2. **Development and Intervention** — Data collection on 450 projects
3. **Reflection and Learning** — Analysis and validation of indicators
4. **Formalization** — Deployment and transfer

{{< /accordion >}}

### Key Statistics

| Metric | Value |
|--------|-------|
| Projects analyzed | 450 |
| Project duration | 5 years |
| Researchers | 11 |
| Students | 29 |
| Partners | 6 |
