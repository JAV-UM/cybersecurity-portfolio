---
layout: home
title: Home
---

# Josh Abad Valentini - Cybersecurity Portfolio

> Postgraduate student in cybersecurity at Universiti Malaya. This portfolio
> gathers my hands-on projects, skills and learning for the course WQE7001 Cyber Security.

- [About me](#1-about-me)
- [Technical skills](#2-technical-skills)
- [Certifications and training](#3-certifications-and-training)
- [Projects](#4-projects)
- [Learning journey](#5-learning-journey)
- [Career objective](#6-career-objective)
- [Contact information](#7-contact-information)

---

## 1. About me

I am Josh Abad Valentini, a postgraduate student at Universiti Malaya, currently
taking **WQE7001 Cyber Security**. I came into security from a broader computing
and project background, and what keeps me here is simple: I like understanding how
systems really work, and then how they break. Reading about an attack is never
enough for me - I want to reproduce it safely in a lab, see the packets, and
understand the defender's side as much as the attacker's.

During this course I have been building a small home lab, learning network
reconnaissance and traffic analysis, and studying the defensive frameworks that
put those techniques in context, such as the Cyber Kill Chain. I care about doing
this ethically: everything in this portfolio was done on my own lab or on legal
practice platforms. My goal is to grow into a hands-on blue-team / security
analyst role, with a solid grasp of both offensive technique and defensive design.

---

## 2. Technical skills

Honest self-assessment. Where a skill maps to a project here, it is linked.

| Skill | Level | Evidence |
|---|---|---|
| Linux command line | Working knowledge | [Virtual Lab Setup](projects/virtual-lab-setup/) |
| Virtualisation / home lab (VirtualBox, VMs) | Working knowledge | [Virtual Lab Setup](projects/virtual-lab-setup/) |
| Network reconnaissance (Nmap) | Working knowledge | [Nmap Service Scan](projects/nmap-service-scan/) |
| Packet / traffic analysis (Wireshark) | Beginner | *in progress - Wireshark lab* |
| Threat models (Cyber Kill Chain) | Working knowledge | TryHackMe: Cyber Kill Chain |
| Access control & security management concepts | Confident | coursework (WIX3003) |
| Git & GitHub (version control) | Working knowledge | this repository |
| Python scripting | Beginner | - |

---

## 3. Certifications and training

Only things I have actually done or am currently taking.

- **TryHackMe - Cyber Kill Chain** room, including the introductory Offensive Security and Defensive Security lessons. *(Completed - WQE7001 activity.)*
- **Cisco Networking Academy** - the networking and security modules of this course (WQE7001). *(In progress.)*

## 4. Projects

At least two hands-on projects, each in its own folder with a full write-up and
sanitised evidence.

### Virtual Lab Setup
Building an isolated, host-only virtual lab (attacker + target VMs) so I can
practise safely and legally. → **[Read the write-up](projects/virtual-lab-setup/)**

### Nmap Service Scan
Host discovery and service/version enumeration against my own lab target, then
turning the output into defensive observations. → **[Read the write-up](projects/nmap-service-scan/)**

---

## 5. Learning journey

When this course started, I understood cybersecurity mostly as theory: firewalls, attacks, "good practice". What really changed this semester is that I now work through problems with my own hands in a lab, and that shift is the main thing I take away.

The first thing that marked me was **building and using my own virtual lab**. I set up an isolated host-only network with Kali Linux as the attacker and Metasploitable 2 as the target, and kept a clean `fresh-install` snapshot of each machine. Doing this made abstract ideas concrete: I finally understood why a VM is the natural home for a test. Isolation means an exploit stays inside the lab and never touches my real host; reproducibility means I can snapshot, try an attack, and roll back to a clean state; and I can stand up a whole attacker-and-target network on one laptop. Keeping everything host-only was not just convenient, it was the safety rule that kept the work ethical and legal.

The second was **reconnaissance with Nmap**. After connecting the two VMs and checking they could reach each other, I did host discovery to find the live target, then scanned it and used `nmap -sV` to read the service versions behind each open port. Writing the results into a table (target IP, open ports, service, version, "looks risky?") turned the idea of an attack surface into something I could see. It also taught me the discipline of "look before you touch": observe and record first, and only ever scan a machine I own and am authorised to test, never the internet or the campus network. The Cisco modules on protocols and network devices gave me the vocabulary to actually understand what I was scanning.

One thing that **went wrong**: at first my two VMs could not see each other. Instead of assuming the tools were broken, I diagnosed it step by step, checking the network mode, then the IP addresses, then a simple `ping`, and found they were not both on the host-only adapter. Putting them on the same host-only network fixed it. The lesson was to debug from the bottom of the stack upward instead of guessing, and that most "it does not work" problems are configuration rather than magic.

One thing I **still find hard** is packet analysis in Wireshark. I can follow a TCP three-way handshake when it is pointed out, but reading a busy capture on my own, and knowing which filters matter, is not yet natural.

My **improvement goal**: finish the Wireshark TCP lab and at least three more practice captures by **31 January 2027**, and measure success by being able to summarise an unseen capture correctly without looking up every filter.

## 6. Career objective

In the short term I want to move into a hands-on **security analyst / blue-team**
role, where I can combine detection, traffic analysis and incident response with a
real understanding of how attacks are built. In the longer term I would like to
specialise in defensive security engineering - designing and hardening the systems
I currently learn to probe.

My next steps are concrete: (1) continue the Cisco Networking Academy track and work toward an
entry-level security certification; (2) complete a structured set of TryHackMe / lab paths to build a
visible track record of practical work; and (3) keep expanding this portfolio with
one new documented project per month so my progress is always demonstrable.

---

## 7. Contact information

- **GitHub:** [@JAV-UM](https://github.com/JAV-UM)
- **LinkedIn:** *Not published yet* - approved alternative in use (professional email + GitHub above). LinkedIn to be added and linked to this portfolio.
- **Professional email:** 25126410@siswa.um.edu.my

*(No phone number or home address is published, by design.)*

