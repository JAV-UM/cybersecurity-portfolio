# Project: Virtual Lab Setup

## Objective
Build an isolated virtual lab where I can practise offensive and defensive
techniques safely and legally, without touching any production or third-party
system. The lab had to let an "attacker" machine and a "target" machine talk to
each other while staying cut off from the internet and from my real network.

## Environment and tools
- Host: my personal laptop
- Hypervisor: Oracle VirtualBox
- Attacker VM: Kali Linux
- Target VM: a deliberately vulnerable/learning VM (e.g. Metasploitable or a basic Linux server)
- Networking: VirtualBox **host-only** adapter shared by both VMs

## Method (step by step)
1. Installed VirtualBox on the host.
2. Created the attacker VM (Kali) and the target VM, each with its own virtual disk.
3. Configured both VMs to use the **same host-only network** so they share a subnet
   but have no route to the internet.
4. Booted both VMs and recorded each one's IP address (`ip a`).
5. Verified connectivity from attacker to target with `ping`.
6. Took a baseline note of the target's hostname and reachable address.

## Results
- Both VMs came up on the same host-only subnet and could reach each other.
- The lab is isolated: no bridge to the physical LAN or the internet.
- This lab is the base used for the [Nmap Service Scan](../nmap-service-scan/) project.

*Evidence:* see `evidence/` (sanitised screenshots of the VM network settings and a
successful `ping` between the two VMs).

> **>> À FAIRE** : dépose tes vraies captures d'écran dans `evidence/` (config réseau + ping réussi).

## What I would do differently
- Snapshot each VM right after setup, so I can roll back to a clean state between exercises.
- Add a third VM running a simple IDS (for example Security Onion / Suricata) to see
  the same attacks from the defender's point of view.
