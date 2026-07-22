# Cyber Homelab - Attack, Detect, Segment

A hands-on lab built to answer one question: **can I make an attack happen, and
then can I detect it?**

Built in phases, each session with a goal. Every session is logged in
LOG.md.

## Phases

**1. The attack works**
Kali and Metasploitable on an isolated host-only network.
Enumerating services, then exploiting one. 

**2. The detection works**
Zeek sensor watching the same network. Re-running attack and finding it in the logs.

**3. The network is real**
Teltonika RUT200 as a dedicated lab gateway: lab segment isolated from the home
network by firewall rules, port mirroring feeding real traffic to the sensor.

**4. The dashboard**
FastAPI backend surfacing Zeek detections, displayed on a wall-mounted tablet.

## Repo layout

```
phase-1-attack/     Notes, commands, screenshots
phase-2-detect/     Zeek config, log excerpts, detection notes
phase-3-network/    Router config, firewall rules, segmentation tests
phase-4-dashboard/  FastAPI app + frontend
evidence/           Screenshots
LOG.md              Session log
```

## Environment

| Role     | Machine |
| Attacker | Kali Linux VM (VirtualBox)
| Target   | Metasploitable 2 VM (VirtualBox, isolated network only)
| Sensor   | Zeek
| Gateway  | Teltonika RUT200 (RutOS)


## Status

- [ ] Phase 1 — attack works
- [ ] Phase 2 — detection works
- [ ] Phase 3 — segmented network with mirrored traffic
- [ ] Phase 4 — dashboard
