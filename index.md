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

> **>> À VÉRIFIER** : ajuste l'intro à ta vraie histoire (parcours, pourquoi la cyber). 100-200 mots.

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

> **>> À VÉRIFIER** : enlève/ajoute des lignes pour refléter ton vrai niveau. Reste honnête (c'est noté là-dessus).

---

## 3. Certifications and training

Only things actually done or clearly in progress (with a target date).

- **TryHackMe - Cyber Kill Chain** room, plus the introductory Offensive Security
  and Defensive Security lessons. *(Completed - WQE7001 activity.)*
- **Cisco Networking Academy** modules - *>> À VÉRIFIER si tu en as suivi.*
- **ISC2 Certified in Cybersecurity (CC)** - *in progress, target: March 2027.*

> **>> À VÉRIFIER** : ne liste QUE ce que tu as vraiment fait. Mets un lien Credly si tu as un badge. Supprime les lignes non applicables.

---

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

*(Reflection on my progress in WQE7001 - 400 to 600 words.)*

When this course started, I understood security mostly as a set of concepts -
firewalls, attacks, "good practice". What changed is that I now work through
problems with my own hands, in a lab, and that shift is the real result of the
semester.

**Two topics that marked me.** The first is the **Cyber Kill Chain**. Doing the
TryHackMe room forced me to stop seeing an attack as a single event and instead
as a sequence - reconnaissance, weaponisation, delivery, exploitation,
installation, command and control, and actions on objectives. The useful part for
a defender is that every stage is also an opportunity to detect and break the
chain; I now read incidents by asking "which stage is this, and where could we
have cut it?". The second is **network reconnaissance with Nmap**. Running scans
against my own lab taught me the difference between a host sweep, a port scan and
service/version detection, and why an attacker's first move is almost always to
map what is listening. Seeing my target's open services listed in front of me made
the idea of "attack surface" concrete rather than abstract.

**Something that went wrong.** Setting up the lab, my attacker and target VMs could
not see each other. I assumed the tools were broken, but by checking step by step -
VM network mode, then IP addresses, then a simple `ping` - I found the VMs were on
NAT instead of a host-only network, so they were isolated from one another.
Switching both to the same host-only adapter fixed it. The lesson was to diagnose
from the bottom of the stack upward instead of guessing, and that most "it doesn't
work" problems are configuration, not magic.

**Something I still find hard.** Packet analysis in **Wireshark** is still
challenging for me. I can follow a TCP three-way handshake when it is pointed out,
but reading a busy capture on my own and separating signal from noise - knowing
which filters to apply and what "normal" looks like - is not yet natural. I plan to
keep practising on captured traffic until the common patterns are obvious to me.

**An improvement goal.** By the end of the next two months I want to be comfortable
analysing a packet capture unaided. Concretely, my target is to complete the
Wireshark TCP lab and at least three additional practice captures, and to be able
to write a short, correct summary of what happened in a capture I have never seen
before. I will measure success by whether I can do that without looking up every
filter. Target date: **31 January 2027**.

> **>> À VÉRIFIER / PERSONNALISER** : c'est le cœur de la note. Remplace par TES vrais souvenirs
> (au moins 2 sujets/labs, 1 problème que tu as résolu, 1 sujet encore difficile, 1 objectif daté et mesurable).
> Vise 400-600 mots.

---

## 6. Career objective

In the short term I want to move into a hands-on **security analyst / blue-team**
role, where I can combine detection, traffic analysis and incident response with a
real understanding of how attacks are built. In the longer term I would like to
specialise in defensive security engineering - designing and hardening the systems
I currently learn to probe.

My next steps are concrete: (1) finish the ISC2 Certified in Cybersecurity
certification; (2) complete a structured set of TryHackMe / lab paths to build a
visible track record of practical work; and (3) keep expanding this portfolio with
one new documented project per month so my progress is always demonstrable.

> **>> À VÉRIFIER** : adapte à TON vrai objectif (rôle visé + 2-3 prochaines étapes). 100-200 mots.

---

## 7. Contact information

- **GitHub:** [@JAV-UM](https://github.com/JAV-UM)
- **LinkedIn:** *Not published yet* - approved alternative in use (professional email + GitHub above). LinkedIn to be added and linked to this portfolio.
- **Professional email:** 25126410@siswa.um.edu.my

*(No phone number or home address is published, by design.)*

> **>> À VÉRIFIER** : ton LinkedIn doit pointer vers ce portfolio (exigence de l'énoncé). Mets un email pro.
