---
title: "Fixing Hyprland Atomic Modesetting"
date: 2026-08-31
tags: ["Linux"]
excerpt: "A general manual about fixing Hyprland atomic modesetting w/ Strix Point."
---

# Solution
To someone who suffered from the same problem -
Install `aquamarine-git` and `hyprland-git` from AUR.

# Intro

Suddenly want to write this in English......

This was a embarrassing thing to say......

So, first thing first, I bought a ASUS ROG Zephyrus G16 (2025, GA605KM) on 19th, July. After all things in Windows - mostly some video games are settled down, I started to think setting up the daily-drive workflow on it, which is `Arch Linux` + `illgical-impulse`.

# Symptom

After fresh installing Arch...... of course I didn't use `archinstall`. I install it totally from scratch. When I tried to launch Hyprland through `/usr/bin/start-hyprland`, the whole screen freezes on **GatherAsyncResources** and the log file didn't cover any error subject.

Okay, then I started googling for 3 hours just try to fix it, and found out the solution - which is add `AQ_NO_ATOMIC=1` to environment variable to force Hyprland launches as legacy DRM mode, which is *Highly unrecommended*. Dang it, at least it can let me get into GUI.

Then I connect my Samsung G8 w/ 4K@240Hz, and it shows beautiful purple artifacts on the screen. Nice.

I googled for the entire next day and the day after tomorrow, even tried to get some help from ChatGPT, Gemini and even Claude and Grok, after running out all my plan, I exhausted, because all the things are just telling me to turn off hardware cursor or just try to lower down the refresh rate - imperfect implementation on multi-GPU / DSC / DRM / NVIDIA support and all the info just try to blame them on @vaxerski and Jensen Huang.

Actually it is due to forceibly turning off atomic modesetting also turned off explicit sync.

I installed Plasma 6, no artifacts, also for Gnome 50. And my agents told me it is about dirty patch for specific hardware - or some bugs from `amdgpu` driver.

Okay, I guess it is just a minor bug caused by atomic modesetting with RDNA 3.5 driver implementation.

Anyway, it is being fixed and merged into `hyprwm/aquamarine`, but it is still not a major fix, so the `aquamarine` package in official repo will still result in this fault, but the software built from source code will work just fine with atomic modesetting on and without any artifacts on the external screen.

Funniest part - I installed `aquamarine` and `hyprland` using `cmake` at first, LOL.

I TOTALLY FORGET WHAT AUR IS FOR. DANG IT. I APOLOGIZE AS A ARCH LINUX USER.

It really brings me lot of pain...... I even decided to switch to `Niri` in the first place, but I soon discovered a PR which fixes this bug in GitHub Discussion in 31st, May. Thanks god, I love this guy, really.

For sure, a good laptop need a good OS, using Hyprland with 180+ PPI screen is amazing.

Try tiling WM with ricing guys, it just feels good and doesn't cost a lot. Maybe more power efficient than most of the DE, although Quickshell itself is kind of heavy though.