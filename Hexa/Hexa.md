# Monolithique

L’architecture hexagonale est un pattern architectural dont le but est de rendre la logique métier (le « cœur » de l’application) indépendante des détails techniques externes (interface utilisateur, base de données, infrastructure, etc.). Elle découpe l’application selon des ports (interfaces abstraites) et des adaptateurs (implémentations concrètes), pour que le cœur puisse interagir avec l’extérieur sans connaître les technologies utilisées

# Caractéristiques : 

- Cœur métier indépendant	Le cœur (business logic / domain) ne dépend pas des technologies externes comme la base de données, les UI, les API externes. Les dépendances techniques sont inversées via les ports/adapters. 

- Ports (interfaces abstraites)	Ce sont des abstractions (interfaces) définies dans le cœur, qui décrivent les points d’entrée/sortie vers l’extérieur (ex : port pour persistance, port pour envoi de messages, port pour API, etc.). 

- Adaptateurs (implémentations concrètes)	Les adaptateurs concrétisent les ports, pour interagir avec les bases de données, les APIs externes, l’interface utilisateur, les protocoles, etc. Ces adaptateurs sont situés à l’extérieur du cœur. 

- Direction des dépendances	Toutes les dépendances structurelles (codage) vont du périphérique (adaptateurs / infrastructure) vers le cœur métier ; le cœur ne connaît pas les adaptateurs. 

- Isolation / testabilité	Le cœur peut être testé de façon isolée (avec des mocks ou adaptateurs simulés). Les changements technologiques dans les adaptateurs ne doivent pas affecter le cœur. 

- Modularité Il est plus facile d’ajouter de nouveaux adaptateurs (par exemple un nouveau type d’interface utilisateur, un nouveau service externe) sans toucher au cœur.

# Exemple de projet

- Hexagonal Architecture Example (Spring Boot)	Java / Spring Boot, WebFlux, R2DBC	Exemple simple montrant séparation en “domain / application / infrastructure adapters” avec accès db réactif. 

- Hex-Microservice (Ports & Adapters)	Go	Monolithe ou microservice utilisant le pattern, séparation nette des dossiers / modules. 

- Modular-Architecture-Hexagonal-Demo-Project	Java	Démo autour de Ticketing / Paiement, production-ready, montre comment plusieurs adaptateurs, services, etc., s’intègrent. 

# Projet connus 

- Nubank : banque numérique, mentionnée souvent comme exemple réaliste utilisant l’architecture hexagonale / ports & adapters pour ses microservices. Cela permet de bien isoler domaine métier et d’évoluer les composants externes.

# Schéma 

![Texte](https://media.licdn.com/dms/image/sync/v2/D4D27AQFCm0KJSqEBiQ/articleshare-shrink_800/articleshare-shrink_800/0/1754403128818?e=2147483647&v=beta&t=pWFjU8q51cD5uu6cOHiGKnZs2vtv0YSM1cp4SLCz57k)

# Source

- Cahtgpt
- Dev community
- Github
- Wikipédia
- Softwarearchitecture
- Rebaze
- AWS Docs
