# Analyse du réseau de vélos en libre-service à New York 🚲

## Introduction

### Contexte
Ce projet s’inscrit dans une réflexion plus large sur l’usage du vélo dans les grandes métropoles, en particulier à travers les systèmes de vélos en libre-service tels que **Vélib’ à Paris** ou **Citi Bike à New York**.

Notre analyse repose exclusivement sur les données **Citi Bike**, les données françaises de trajets étant difficilement accessibles pour des raisons de **RGPD et de confidentialité**. Le vélo constitue aujourd’hui un levier majeur des politiques publiques en matière de **transition écologique**, de réduction des émissions et de transformation de l’espace urbain. Son développement s’accompagne d’aménagements structurants : pistes cyclables, stations de vélos, et intégration avec les transports collectifs.

---

## Problématique

Le vélo reste un mode de transport **physiquement contraignant** et peu adapté aux longues distances. Dans les grandes villes, les zones d’activités économiques sont souvent concentrées (quartiers d’affaires, pôles administratifs), tandis que les lieux de résidence peuvent être plus éloignés.

Ainsi, le vélo apparaît principalement comme un **mode de transport intermédiaire**, utilisé pour relier :
- le domicile à un transport principal (métro, train, bus),
- ou un transport collectif au lieu de travail.

La question centrale de ce projet est donc la suivante :

> **L’intermodalité du vélo dans une grande ville comme New York est-elle observable et vérifiable à partir des données Citi Bike ?**

---

## Objectifs

Les usages du vélo sont fortement influencés par des facteurs externes :
- conditions météorologiques (pluie, froid),
- temporalité (semaine vs week-end),
- périodes de vacances,
- normes sociales et culturelles.

L’objectif de ce projet est d’**analyser et de décrire la place du vélo dans la mobilité new-yorkaise**, en mettant en évidence :
- ses usages dominants,
- ses avantages et ses limites,
- et le rôle de l’intermodalité dans les déplacements urbains.

Ces constats s’inscrivent dans la continuité de travaux existants, notamment :

> *« Le développement du vélo participe à la mise en œuvre de politiques de mobilité durable efficaces visant à améliorer la qualité de l’air et à lutter contre le changement climatique. »*  
(GART, 2015)

> *« Dans une chaîne multimodale de déplacements, le potentiel du vélo est le plus important. »*  
(GART, 2015)

---

## Données et Méthodologie

### Données utilisées
L’analyse repose sur les données Citi Bike de **New York**, incluant :
- durée des trajets,
- heures de départ et d’arrivée,
- identifiants et noms des stations,
- coordonnées géographiques (latitude, longitude),
- informations sur les vélos.

Certaines variables (genre, type d’utilisateur) ont été volontairement écartées afin de se concentrer sur l’analyse spatiale et temporelle des flux.

### Outils mobilisés
- **Python** (Pandas, Matplotlib, bibliothèques de cartographie),
- **Gephi** pour l’analyse de réseaux,
- **Inkscape** pour la superposition et la mise en forme cartographique.

---

## Analyse du Réseau

### Une concentration au cœur de Manhattan
Le réseau de vélos se concentre très fortement à **Manhattan**, notamment dans les quartiers :
- Midtown,
- Union Square,
- Chelsea,
- Financial District.

<img width="413" height="451" alt="Capture d’écran 2025-12-23 054112" src="https://github.com/user-attachments/assets/26fb4bc9-27e9-4c99-91cc-30b0a83d9414" />


Des stations comme **Pershing Square North**, située à proximité immédiate de **Grand Central Terminal**, jouent un rôle central dans les départs et arrivées. Cette concentration s’explique par :
- la densité d’emplois,
- la présence de hubs de transport,
- la proximité entre zones résidentielles, touristiques et économiques.

### Rôle des autres arrondissements
- **Brooklyn** présente un réseau significatif mais moins dense, avec peu de trajets inter-arrondissements.
- **Queens** affiche une utilisation plus faible, probablement liée à une moindre densité d’activités et d’infrastructures cyclables.

Ces résultats indiquent que la majorité des trajets observés sont **intra-Manhattan**, soulignant le rôle central de cet arrondissement dans la mobilité à vélo.

---

## Visualisations et Mesures

Les heatmaps mettent en évidence les stations les plus utilisées :

<img width="435" height="396" alt="Capture d’écran 2025-12-23 054231" src="https://github.com/user-attachments/assets/ea63a25b-3a65-4b17-bbdc-d60fd2208310" />

<img width="470" height="298" alt="Capture d’écran 2025-12-23 054446" src="https://github.com/user-attachments/assets/972b1a98-75e4-4e87-9ef8-0e68c6d735da" />


- **Pershing Square North** :  
  - 6 437 départs  
  - 6 373 arrivées  
  Située près de Grand Central Terminal, elle constitue un **hub intermodal majeur**.

- **W 21 St & 6 Ave (Chelsea)** :  
  - usage équilibré entre départs et arrivées, typique de trajets circulaires.

- **W 41 St & Ave** :  
  - principalement station d’arrivée, probablement liée à l’attractivité de Times Square.

Les stations les plus fréquentées sont systématiquement situées à proximité :
- de pôles de transport,
- de zones touristiques,
- de centres d’activités économiques.

---

## Analyse temporelle des trajets

### Matin (7h – 10h)
Les trajets sont dominés par des flux **domicile-travail / domicile-école**, reliant des quartiers résidentiels à des zones d’affaires ou administratives.

### Fin de journée (17h – 20h)
Les flux se concentrent autour de hubs comme **Pershing Square North**, illustrant le rôle clé de l’intermodalité dans les retours du travail.

### Soirée (19h – 22h)
Les trajets deviennent plus **locaux**, notamment à Brooklyn (Williamsburg), et sont davantage liés aux loisirs et aux activités sociales.

Les trajets entre Manhattan et Brooklyn restent peu nombreux, suggérant une préférence pour d’autres modes de transport pour les distances plus longues.

---

## Conclusion

L’analyse met clairement en évidence que :
- l’**intermodalité du vélo** est bien présente à New York,
- le vélo est utilisé comme un **complément aux transports collectifs**,
- Manhattan constitue le cœur du réseau, tant pour les départs que pour les arrivées.

Cependant, ces résultats doivent être nuancés :
- l’analyse porte sur une période limitée (janvier),
- les usages sont sensibles aux conditions météorologiques et sociales.

Comme le soulignent les études existantes :

> *« L’intermodalité est cruciale pour surmonter les limites du vélo en termes de distance. »*  
(GART, 2015)

> *« L’usage du vélo reste sensible aux conditions météorologiques. »*  
(CERTU, 2013)

---

## Perspectives
Pour aller plus loin, plusieurs pistes peuvent être explorées :
- analyse sur plusieurs saisons,
- intégration de données météorologiques,
- étude plus fine des flux horaires,
- comparaison avec d’autres grandes villes.

Ce projet met en lumière le rôle stratégique du vélo dans les mobilités urbaines durables et son intégration croissante dans les chaînes de déplacement multimodales.
