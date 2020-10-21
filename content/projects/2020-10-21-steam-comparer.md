---
title: Steam Comparer
date: 2020-10-21T01:09:25.283Z
description: SteamComparer is a Django-Rest-Framework and NuxtJS web application that monitors steam applications, and lets users extensively search our app database as well as compare Steam app libraries.
frontendcode: https://github.com/vBubbaa/steamcomparer-nuxt
backendcode: https://github.com/vBubbaa/django-steamkit-integration
headerimage: /img/scheader-7.png
livesite: https://steamcomparer.com/
---

# Steamcomparer

SteamComparer started as a project where users could login via OpenID into the popular PC gaming platform [steam](https://store.steampowered.com/) and compare game libraries with their friends. The problem was there wasn't an easy way to see what games you had in common with friends, the solution is [SteamComparer](https://steamcomparer.com/).

Along with library comparison, SteamComparer allows users to view a shareable profile overview page which allows for viewing detailed account information which is not easily accessible on Steam itself. We rely on Steam's extensive [WebAPI](https://steamcommunity.com/dev). We pull user information regarding their game library as well as useful information such as game bans, playtime, and much more detailed information.

We incorporate a Steamkit2 python [port](https://github.com/ValvePython/steam) which allows us to connect to the steam client itself. We use this client to have monitoring scripts which automatically get notified when an Steam app or package gets updated. We then take the change number and use an extensive script to process the Steam Client response about the App Details and save the application to our database, or update any fields that were changed.

We have a backend has several foreign keys relating to various fields such as Developers, Publishers, etc. and allows us to have pages like the [Developer](https://steamcomparer.com/developers) page. Users get to extensively search and browse whatever steam has to offer, as well browse an app search page with advanced filters allowing user to find whatever app they wish in our growing database with 10s of thousands of apps.

## Technologies

- Python
- Django-Rest-Framework
- NuxtJS
- Vuetify
- Steam Web API
- Steam Package (Steamkit2 Python Port)
- Django AllAuth