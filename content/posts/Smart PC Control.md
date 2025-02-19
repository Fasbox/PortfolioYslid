+++
date = '2025-02-18T22:41:17-05:00'
draft = false
title = 'Smart PC Control: Alexa + Remote Access'
description = "Ever wished you could turn on your PC with just your voice? I made Alexa do it—and set up secure remote access with RustDesk. Here’s how I pulled it off!"
image = "/ImagenesPosts/Thumbnail post1.1.svg"
imageBig = "/ImagenesPosts/Thumbnail post1.svg"
categories = ["IoT", "DIY Tech Hacks"]
authors = ["Yslid"]
avatar = "/images/avatar.webp"
videoEs = "-AdjRO3UgW0"
videoEn = "CvPtDd3B3PE"
+++

# The Problem: "Wait, Did I Leave My PC On?"

You ever left home, halfway to wherever you're going, and suddenly remembered you needed something from your computer? That was me. The worst part? My PC was off.

I needed a way to turn it on remotely and access it securely, no matter where I was. That's when I went down the rabbit hole of **Wake-on-LAN**, **RustDesk**, and **self-hosted setups**—with some inspiration from NetworkChuck, of course.

And let me tell you… It **did not** work on the first try.

## Step 1: Making Alexa Turn On the PC
To make this happen, I used **Wake-on-LAN via Alexa** along with a few tweaks. Here’s how I got it working:

1. **Enable Wake-on-LAN on Windows**
    - Go to BIOS and enable Wake-on-LAN (WOL).
    - In Windows, enable WOL in your network adapter settings.
      
2. **Set Up a Wake-on-LAN Alexa Skill**
    - I used [Alexa Wake-on-LAN](https://example.com) (or the one you used).
    - Linked it to my network and set up my PC's MAC address.
      
3. **Test It**
    - _This was the fun/frustrating part._
    - Alexa just wouldn’t recognize the command at first. I triple-checked everything, no luck.
    - Gave up, went to sleep, tried the next day, and boom—it worked. No idea why, but hey, I’m not complaining.

## Step 2: Remote Access with RustDesk (Self-Hosted, Of Course!)
Once I had Alexa waking up my PC, I needed a **reliable** and **secure** way to connect to it from my laptop (running Linux) to my Windows machine. My biggest challenge? Finding software that worked well across OSes.

I decided to **self-host RustDesk**, inspired by NetworkChuck's approach:

1. **Set Up a RustDesk Server**
    - Installed my own relay server to avoid third-party connections.
    - Configured my Windows machine as a host.
    - Installed RustDesk on my Linux laptop.

2. **Tested and Tweaked Security Settings**
    - Configured strong passwords.
    - Set up firewalls and network rules to lock things down.

3. **Now I Can Access My PC from Anywhere**
    - With just a voice command to Alexa and a RustDesk connection, I can remotely wake up and control my PC.

## **Final Thoughts: What Did I Learn?**
- **Persistence pays off.** Sometimes, tech just starts working for no reason.
- **Self-hosting is worth it.** RustDesk gives me control over my data.
- **Wake-on-LAN + Alexa = Super handy.**