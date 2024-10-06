# Asustor 5404T aka Tesseract

## Overview

I've always wanted to own a NAS, and in 2024, I finally bought one. It's been one of my biggest investments, but it's been solid since day one. I call it **Tesseract** because its shape reminds me of the Tesseract from the MCU (yes, I’m a big fan). *Fun fact: back in university (around 2014), I had a portable HDD that I also named Tesseract. So, this feels like a full-circle moment for me.*

My main goal for Tesseract is to serve as a media server, which is why I chose the Asustor 5404T—for its internal GPU that supports hardware-accelerated transcoding. Of course, it also functions as a standard NAS, handling network shares to free up storage on my other devices. 

## Specifications

| Model           | CPU                 | RAM       | Storage                  | Networking      |
|-----------------|---------------------|-----------|--------------------------|-----------------|
| Asustor AS5404T | Intel Celeron N5105 | 4 GB DDR4 | 4-bay HDD and 4x M.2 SSD | 2.5 Gb Ethernet |

The deal breakers for me:

* It is a hybrid NAS that supports both HDD and SSD (for caching/hot tier), I believe it's one of the first hybrid NAS devices on the market..
* 2.5 Gb Ethernet, but I don't think I’ll need that much bandwidth anytime soon.
* The internal GPU for media transcoding is a big plus. 
* I have a soft spot for Asus products. I use an Asus ROG Strix as my daily driver, along with an [Asus Azoth keyboard](https://rog.asus.com/us/keyboards/keyboards/aura-rgb/rog-azoth-model/).

## OS

AS5404T runs Asustor Data Master (ADM) OS. Since this is my first NAS, I decided to stick with the stock OS to get familiar with its features before trying a custom option.

## Services

ADM uses Docker containers but has an App Central front end that makes installing containers, as *applications*, very user-friendly. Most of the services I’ve deployed on Tesseract are through App Central. The exceptions are Watchtower and a few containers not officially supported by App Central, which I use mostly for testing.

| Service                                   | Usage                        |
|-------------------------------------------|------------------------------|
| [Portainer](../services/portainer.md)     | Container management tool    |
| [Jellyfin](../services/jellyfin.md)       | Open-source Media Server     |
| [Vaultwarden](../services/vaultwarden.md) | Open-source Password Manager |