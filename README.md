# tap-tap

**tap-tap** is my plan for a secure access system for condos (300–400 units).  

The idea is to replace buzzer systems with **temporary visitor passes** that work through a cryptographic challenge–response handshake.  
Name: "tap-tap" because the resident or visitor only needs to tap once at the door or tap once on a link.

⚠️ **Note:** This repo is only for planning and design.  
I have not started building or coding yet.

---

## Repo Contents
- **docs/** → design notes: architecture, protocol handshake, threat model, operations.  
- **services/** → placeholders for Edge Controller, Door Unit, and Visitor page.  
- **hardware/** → bill of materials, wiring notes, OSDP provisioning.  
- **deploy/** → docker/dev setup (future), infrastructure code (future).  
- **scripts/** → small tools and simulators.  

---

## Vision
- **Visitor passes instead of buzzers** → residents issue time-limited passes.  
- **Handshake model** → every unlock requires proof of possession (ephemeral key) and freshness (nonce).  
- **Building scale** → single building, 10–20 controlled doors, 300–400 units, thousands of events/day.  
- **Offline mode (later)** → fallback codes if network is down.  

---

## Current Status
- Architecture drafted  
- Protocol sequence outlined (Edge Controller ↔ Door Unit ↔ Visitor)  
- Hardware standards chosen (OSDP Secure Channel, mTLS, PoP tokens)  
- Not started: implementation, hardware prototypes  

---

## Roadmap
See [`ROADMAP.md`](./ROADMAP.md).  
High level:  
0. Planning (current stage) — write docs, design protocol, list hardware options  
1. Core handshake in simulation  
2. Single-door hardware MVP  
3. Building-wide features (amenities, deliveries, elevators)  
4. Security hardening and offline fallback  

---

## License
MIT. This is a personal planning repo.

