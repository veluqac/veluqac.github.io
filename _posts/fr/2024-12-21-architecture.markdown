---
layout: post
title:  "Tout est connecté"
date:   2024-12-21 16:00:00 +0200
categories: update
lang: fr
author: Damien
---
Dans cet article, nous présentons brièvement l’architecture générale de la plateforme Véluqac, en nous concentrant principalement sur l’aspect matériel et les usages potentiels liés aux personnes utilisatrices.

![Architecture du veluqac]({% link /assets/img/blog/architecture.drawio.png %})

1. **Une personne qui pédale.**
Au coeur du système se trouve une personne qui, en pédalant, génèrera de l’énergie. Ce geste simple transformera l’effort physique en électricité, tout en ouvrant la porte à des usages pédagogiques, écologiques et interactifs.

1. **Collecte de données.**
Le vélo-bureau sera équipé de capteurs qui mesurent différents paramètres tels que le nombre de cycles effectués, la tension, le courant et l’énergie générée. Ces données, accompagnées de l’identifiant de l’appareil et éventuellement de celui de la personne utilisatrice, seront transmises via Internet à un serveur distant.

1. **Traitement et stockage sur serveur.**
Le serveur recevra les données en temps réel, les traitera si nécessaire, puis les enregistrera dans une base de données. Pour assurer cette gestion, nous prévoyons d’utiliser une dorsale (_backend_) en tant que service (BaaS pour _Backend as a Service_) telles que [Supabase](https://supabase.com), [PocketBase](https://pocketbase.io), [Appwrite](https://appwrite.io) ou [Firebase](https://firebase.google.com). Ce serveur agira ainsi comme un point central d’échange, permettant de redistribuer les données à d’autres systèmes connectés.

1. **Des usages multiples selon les contextes.**
Une fois disponibles sur le serveur, les données peuvent être exploitées par une variété d’appareils, en fonction des besoins pédagogiques ou expérimentaux. Voici quelques exemples :
  - Sur un téléphone intelligent, une application peut afficher à la personne utilisatrice des informations sur sa production d’énergie ou proposer des défis motivants.
  - Sur un ordinateur personnel, un tableau de bord en ligne peut visualiser l’ensemble des données pour suivre l’utilisation de plusieurs appareils dans une salle ou un établissement.
  - Sur un ordinateur monocarte (comme un [Raspberry Pi](https://www.raspberrypi.com)), les données peuvent être utilisées pour simuler l’alimentation d’un vidéoprojecteur ou gérer l’éclairage d’une salle de classe, démontrant concrètement l’impact de l’effort physique sur la consommation énergétique.