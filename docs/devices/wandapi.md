# Raspberry Pi 4B aka Wanda

## Overview

My journey into homelabs began with a Raspberry Pi. A few years ago, I owned a Raspberry Pi 3, which I used to learn Linux and run a few services. When I restarted my homelab journey a year ago, I naturally chose another Raspberry Pi (4B), which I named Wanda.

Initially, I used it to run a DNS ad-blocking server and some download clients. However, I have since moved those services to a GMKtec G2. Now, my Raspberry Pi serves as my Tailscale subnet router and runs monitoring software like Prometheus and Grafana. I also use it as my workstation to study Golang.

## Specifications

| Model                  | CPU           | RAM  | Storage    | Networking                       |
|------------------------|---------------|------|------------|----------------------------------|
| Raspberry Pi 4 Model B | BCM2711 ARM64 | 8 GB | 256 GB SSD | 1 Gb Ethernet & 2.4GHz/5GHz WiFi |

I use an [Argon ONE M.2 Case](https://argon40.com/products/argon-one-m-2-case-for-raspberry-pi-4) to house Wanda. This case is super aesthetic and equally functional. It features a built-in fan with automated control. You can set temperature thresholds to adjust the fan speed. Additionally, it supports an M.2 SATA SSD, allowing for faster and larger storage compared to the default SD card.

## OS

I’m currently using Raspberry Pi OS as my base operating system. I’ve tried other options like DietPi and Ubuntu, but Raspberry Pi OS has proven to be the most reliable.

I am running [CasaOS](https://casaos.zimaspace.com) on top of it to *simplify my personal cloud experience*, as their site claims. However, I will probably uninstall it soon. I haven't found it very useful, and I prefer the flexibility of managing my Docker containers manually.

## Services

I use Docker heavily and utilize Docker Compose to deploy my containers. For monitoring and managing these containers, I use Portainer.

| Service                                                 | Usage                                |
|---------------------------------------------------------|--------------------------------------|
| [Portainer](../services/portainer.md)                   | Docker Management tool               |
| [Dockge](../services/dockge.md)                         | Docker Compose Management tool       |
| [Tailscale](../services/tailscale.md)                   | VPN for secure access to my homelab  |
| [Grafana](../services/grafana.md)                       | Visualize metrics                    |
| [Prometheus](../services/prometheus.md)                 | Time series data storage for metrics |
| [Prometheus SNMP Exporter](../services/snmpexporter.md) | Collect SNMP device metrics          |
| [Prometheus Node Exporter](../services/nodeexporter.md) | Collect host system metrics          |
| [cAdvisor](../services/cadvisor.md)                     | Collect container metrics            |

