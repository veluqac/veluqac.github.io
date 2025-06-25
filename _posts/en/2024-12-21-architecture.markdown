---
layout: post
title:  "Everything is connected"
date:   2024-12-21 16:00:00 +0200
categories: update
lang: en
author: Damien
---
In this article, we briefly present the general architecture of the Veluqac platform, focusing mainly on the hardware aspect and the potential uses related to the users.

![Architecture of the Veluqac]({% link /assets/img/blog/architecture.drawio.png %})

1. **A person pedaling.**
At the heart of the system is a person who, by pedaling, generates energy. This simple action transforms physical effort into electricity, while opening the door to educational, ecological, and interactive uses.

1. **Data collection.**
The bike-desk will be equipped with sensors measuring various parameters such as the number of cycles, voltage, current, and generated energy. This data, along with the device ID and optionally the user ID, will be sent over the Internet to a remote server.

1. **Processing and storage on the server.**
The server will receive the data in real time, process it if necessary, and store it in a database. To manage this, we plan to use a backend-as-a-service (BaaS) solution such as [Supabase](https://supabase.com), [PocketBase](https://pocketbase.io), [Appwrite](https://appwrite.io) or [Firebase](https://firebase.google.com). This server will act as a central exchange point, enabling redistribution of the data to other connected systems.

1. **Multiple uses depending on context.**
Once available on the server, the data can be leveraged by a variety of devices, depending on educational or experimental needs. Here are a few examples:
  - On a smartphone, an app could display information to the user about their energy production or offer motivational challenges.
  - On a personal computer, an online dashboard could visualize all the data to monitor the use of several devices within a room or facility.
  - On a single-board computer (such as a [Raspberry Pi](https://www.raspberrypi.com)), the data could be used to simulate powering a projector or manage classroom lighting, concretely demonstrating the impact of physical effort on energy consumption.