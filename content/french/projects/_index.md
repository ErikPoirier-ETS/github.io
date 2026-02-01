---
title: "Projets"
description: "Les projets de construction analysés dans le cadre de notre recherche."
image: "/images/projects.png"
layout: "projects"
draft: false
---

## Carte interactive des projets

<div id="map" style="width: 100%; height: 480px; border-radius: 16px; border: 1px solid #e5e5e5; margin-bottom: 2rem;"></div>

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script>
document.addEventListener('DOMContentLoaded', function() {
    const projects = [
        { name: "Bâtiment administratif SQI", address: "Québec, QC", type: "Institutionnel", owner: "SQI", coords: [46.8139, -71.2080] },
        { name: "Infrastructure routière MTMD", address: "Montréal, QC", type: "Infrastructure", owner: "MTMD", coords: [45.5017, -73.5673] },
        { name: "Logements sociaux SHQ", address: "Laval, QC", type: "Résidentiel", owner: "SHQ", coords: [45.6066, -73.7124] },
        { name: "Poste HQ", address: "Trois-Rivières, QC", type: "Énergie", owner: "Hydro-Québec", coords: [46.3432, -72.5477] },
        { name: "Centre communautaire", address: "Montréal, QC", type: "Municipal", owner: "Ville de Montréal", coords: [45.5231, -73.6004] },
        { name: "Édifice patrimonial", address: "Québec, QC", type: "Municipal", owner: "Ville de Québec", coords: [46.8123, -71.2145] },
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

## Projets pilotes (exemples)

{{< notice "note" >}}
Les projets présentés ci-dessous sont des exemples représentatifs. Notre échantillon complet comprend **450 projets** répartis entre 200 projets sans BIM et 250 projets avec BIM.
{{< /notice >}}

| Projet | Localisation | Propriétaire | Type |
|--------|--------------|--------------|------|
| Bâtiment administratif | Québec, QC | SQI | Institutionnel |
| Infrastructure routière | Montréal, QC | MTMD | Infrastructure |
| Logements sociaux | Laval, QC | SHQ | Résidentiel |
| Poste de transformation | Trois-Rivières, QC | Hydro-Québec | Énergie |
| Centre communautaire | Montréal, QC | Ville de Montréal | Municipal |
| Édifice patrimonial | Québec, QC | Ville de Québec | Municipal |

---

## Méthodologie

Le projet est livré suivant une approche de **Recherche-Action-Design (RAD)**, menée au sein des six organisations partenaires.

{{< accordion "Étapes de la méthodologie" >}}

1. **Formulation du problème** — Définition des stratégies de mesure
2. **Développement et intervention** — Collecte de données sur 450 projets
3. **Réflexion et apprentissage** — Analyse et validation des indicateurs
4. **Formalisation** — Déploiement et transfert

{{< /accordion >}}

### Statistiques clés

| Métrique | Valeur |
|----------|--------|
| Projets analysés | 450 |
| Durée du projet | 5 ans |
| Chercheurs | 11 |
| Étudiants | 29 |
| Partenaires | 6 |
