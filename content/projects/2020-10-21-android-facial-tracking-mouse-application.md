---
title: Android Facial Tracking Mouse Application
date: 2020-10-21T22:08:16.345Z
description: An application using facial tracking to control a mouse on mobile
  screen with control functionality.
code: https://github.com/vBubbaa/android-mouse
headerimage: /img/androidmouse-header.jpg
---

# Android Mouse via Facial Tracking

While in University obtaining my Bachelors in Information Technology, my parter and I were tasked with building out a senior capstone project. After several iterations of idea, we decided to build an Android application that controlls a mobile android device by placing a mouse object on the screen and is controlled purely by facial gestures and head movements.

The idea is simple, just like how a computer uses a mouse that moves around and clicks, we created a phone application that does that same thing but instead of using a hand to control the mouse, we would use facial gestures and head movements to control the mouse.

We used Java and Android Studio to create the application and the [OpenCV](https://opencv.org/) libraries Android build to use the OpenCV camera allowing for tracking. We setup facial tracking to track head positioning and plotted the respective coordinates. We then used these coordinates to directly control and move an on screen mouse.

To utilize the mouse to control the phone, we setup a system that tracked when a head position stopped moving, and if the head stayed still for five seconds, it would perform a `click` action. For additional functionality, we included instruction for users to setup Android's built in disability mode which allowed for an on screen control for `hard buttons`.

> Hard buttons are the buttons the phone that such as volume control buttons, lock buttons, and the home button

The application fully tracks head movements and simulates a computer mouse on screen with full clicking functionality.

# Technologies

- Java
- Android Studio
- OpenCV
