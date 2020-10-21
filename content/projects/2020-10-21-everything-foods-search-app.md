---
title: "Everything Food's Search App "
date: 2020-10-21T21:58:12.060Z
description: My code submission for Everything Food's search application
code: https://github.com/vBubbaa/ef-search-app
headerimage: /img/bagelheader.png
---

# Everything Food search application

This project was quickly put together for Everything Food's code submission. The guidelines where to leverage NuxtJS and TailwindCSS to create a web application which included at least one filtering option, and at least one sorting option for an API with several food items. The API was provided to use and returned food items based on query parameters.

## Features

I built the application with a search bar allowing to browse the given API by search.

The application allowed for nested filtering including "Brands" filtering and "Package Size" filtering.

The application lets users sort food by "ABBScore" and alphabetical order.

To accomplish this task, I created a UI component to display the food items and two functional components inclulding a dyanmic InputSelection component and Sort component. The search page generated the given brands and package sizes based upon the search results. These generated results are fed into the functional input components letting users filter by all of the available package sizes and brands.

## Technologies

- NuxtJS
- TailwindCSS
