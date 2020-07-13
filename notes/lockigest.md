---
title: "Lockigest"
date: 2020-07-13T01:24:20+03:00
draft: false
toc: false
description: "Lockigest is a very primitive, manipulative security software that sets a trap instead of locking your device screen immediately to protect it from strangers."
tags: ["terminal"]
categories: ["Security", "GNU Linux"]
---

{{< figure src="/images/lockigest.jpg" class="no-shadow" title="to you / to strangers" >}}

:closed_lock_with_key:  Lockigest is a very primitive, manipulative security software that sets a trap instead of locking your device screen immediately to protect it from strangers.

### Here is how Lockigest works:  
1. Follow the cursor's movements. 
2. If the cursor is at the same location as before for a certain period of time (say 5 minutes), assume that the owner of the device is away and set a trap for unauthorized hands. At this stage, the device will still appear unlocked.
3. As soon as the cursor moves while the trap is active, start counting up to the specified number of seconds (e.g. 5 seconds) before locking the device.
4. If the user moves the cursor to the predefined area in 5 seconds, no need to lock the device as this user is the owner. Otherwise, lock the device so the attacker caught in the trap.

With this approach, you do not have to type your password -again and again- to unlock your device. It will always seem unlocked. After a period of inactivity, instead of getting locked, your device will wait for you to move the cursor to the predefined area in order to stop the protection mode and counting to lock. So you can unlock your pseudo-locked device just by moving your cursor to the predefined location. Easy.

{{< video src="/images/lockigest.mp4" title="Trying Lockigest" controls="1" controls="1" >}}

### Talk is cheap so let's see the code:
Lockigest is a very small software consisting of 90 lines code, including comment and blank lines. It can be very useful though.

***
The main idea behind this simple software is the "trap system". You can change the way your Lockigest deactivates the trap. For instance, you can use your keyboard strokes so if you type "a" and wait for three seconds and then type "can2", the trap can be deactivated. It's only limited to your imagination and the triggers you choose.

