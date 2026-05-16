---
layout: post
title: "I found my first ever bug???"
date: 2026-05-03
categories: bug exploit 
---
[Note] this bug has already been reported in the chromium issues tracker, but i have not found any writeup's or detailed explanation or a fix for this issues but i will still be writing a blog on this bug hoping to find a soultion or at the very least find the root cause of the bug :).
## ---------------------------------------------------------------------------------
I have my arrear exams in 3 days which scare the shit out of me.
I should be preparing for that but here i am, writing a blog for a bug which i am not sure is even a bug. 

## Context 

In my oneplus 12r, and even until 2ish years or so ago, oneplus mobile devices had something called a alert slider. They are non programmable and they have only three functions programmed into them: 
- **Ring**, 
- **Vibrate**, 
- **Silent**.

When the slider is in the bottom most position it puts the device in it is default state ie., **Ring** mode. From the bottom of the slider when you push the slider to the middle, it puts the device into **Vibration** mode, and again when you push the slider up, you put the mobile in **Silent** mode.

Why should the context matter???. I have no fucking idea, i am not a security reseacher and i dont know whats relevant and whats not relevant.

## So what's the bug??

The bug itself is not dangerous(i think). but what the bug/glitch is that when you are inside a wesbite and you are toggling the alert slider up and down, something weird happens. The find funcionality on the Chrome mobile apps pops up
