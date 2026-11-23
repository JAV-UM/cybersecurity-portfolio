# Project: Nmap Service Scan

## Objective
Discover which hosts are alive on my lab subnet and enumerate the services and
versions exposed by my own target VM, then turn that reconnaissance into defensive
observations. Scanning was done **only** against a machine I own in my isolated lab.

## Environment and tools
- Attacker: Kali Linux VM
- Target: my lab target VM (see [Virtual Lab Setup](../virtual-lab-setup/))
- Tool: Nmap
- Network: VirtualBox host-only subnet

## Method (step by step)
1. **Host discovery** - swept the lab subnet to find live hosts:
   `nmap -sn 192.168.56.0/24`
2. **Port scan** - listed open TCP ports on the target:
   `nmap <target-ip>`
3. **Service / version detection** - identified what is actually running:
   `nmap -sV <target-ip>`
4. (Optional) default scripts for more detail:
   `nmap -sC -sV <target-ip>`
5. Saved the output and reviewed each open service.

## Results
- Host discovery found the target alive on the host-only subnet.
- The port scan revealed the open services (for example SSH, HTTP, etc.).
- Version detection named the service versions, which is exactly the information an
  attacker uses to look for known vulnerabilities.

*Evidence:* see `evidence/` (sanitised screenshots of the Nmap output).

## Defensive takeaway / what I would do differently
- Every open service is attack surface: close or firewall anything not needed.
- Keep exposed services patched, since version banners reveal exploitable builds.
- From the defender's side, this kind of scan is noisy and would be visible to an
  IDS - a good reason to monitor for sweeps and port scans.
- Next time I would also compare an unauthenticated scan with an authenticated one
  to see how much more detail credentials expose.
