---
layout: post
title:  "Tout est connecté"
date:   2024-12-21 16:00:00 +0200
categories: update
lang: fr
author: Damien
---
Dans cet article, nous présentons l’architecture générale de la plateforme Véluqac, en nous concentrant principalement sur l’aspect matériel et les usages potentiels liés aux personnes utilisatrices.

1. **Une personne qui pédale.**
Au coeur du système se trouve une personne qui, en pédalant, génère de l’énergie. Ce geste simple transforme l’effort physique en électricité, tout en ouvrant la porte à des usages pédagogiques, écologiques et interactifs.

2. **Collecte de données.**
Le vélo-bureau est équipé de capteurs qui mesurent différents paramètres tels que le nombre de cycles effectués, la tension, le courant et l’énergie générée. Ces données, accompagnées de l’identifiant de l’appareil et éventuellement de celui de la personne utilisatrice, sont transmises via Internet à un serveur distant.

3. **Traitement et stockage sur serveur.**
Le serveur reçoit les données en temps réel, les traite si nécessaire, puis les enregistre dans une base de données. Nous prévoyons d’utiliser une infrastructure comme Supabase ou Firebase pour assurer cette gestion. Ce serveur agit ainsi comme un point central d’échange, permettant de redistribuer les données à d’autres systèmes connectés.

4. **Des usages multiples selon les contextes.**
Une fois disponibles sur le serveur, les données peuvent être exploitées par une variété d’appareils, en fonction des besoins pédagogiques ou expérimentaux. Voici quelques exemples :
  - Sur un téléphone intelligent, une application peut afficher à la personne utilisatrice des informations sur sa production d’énergie ou proposer des défis motivants.
  - Sur un ordinateur personnel, un tableau de bord en ligne peut visualiser l’ensemble des données pour suivre l’utilisation de plusieurs appareils dans une salle ou un établissement.
  - Sur un ordinateur monocarte (comme un Raspberry Pi), les données peuvent être utilisées pour simuler l’alimentation d’un vidéoprojecteur ou gérer l’éclairage d’une salle de classe, démontrant concrètement l’impact de l’effort physique sur la consommation énergétique.