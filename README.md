# FunZone

FunZone is an open-source control platform for small animatronics, haunted houses, escape rooms, and interactive art.

It glues together cheap microcontrollers (like the Raspberry Pi Pico W, Arduino, ESP), sensors, servos, MP3 boards, and lights using MQTT and Node-RED so you can build weird, reactive, story-driven spaces without reinventing the whole stack every time.

FunZone is **open core**: the basics are free and open under Apache 2.0; advanced flows, kits, and tools are offered as optional paid add-ons to help fund development.

---

## ✨ What FunZone Does

- 🧠 **Node-based architecture**  
  Each “room” or prop gets a small FunZone node (Pico W or similar) handling:
  - sensors (PIR, buttons, beam breaks, etc.)
  - outputs (servos, relays, LEDs, MP3 triggers)
  - a simple state machine

- 📡 **MQTT messaging layer**  
  Nodes talk over MQTT so you can:
  - coordinate multiple rooms
  - trigger sequences from a central “director”
  - monitor health / status

- 🧩 **Node-RED orchestration**  
  Node-RED flows define:
  - scene logic
  - scare sequences
  - idle loops
  - show start/stop
  - panic / safe modes

- 🧪 **Simple, hackable firmware**  
  Firmware is written with clarity in mind, not cleverness, so artists and tinkerers can:
  - change pins
  - add sensors
  - tweak timings
  - log what’s happening

---

## 🧰 Current Status (v0.x – Early)

FunZone is **early-stage** and evolving. Right now you can:

- run a basic FunZone node on a Pico/Pico W
- react to a PIR or button and drive an LED or relay
- send/receive MQTT events
- use sample Node-RED flows for simple room logic

Planned for v0.1–v1.0:

- standardized node config format (YAML/JSON)
- cleaner topic conventions
- “room profile” examples for common setups
- test harness flows for bench testing nodes
- documentation + diagrams
- starter kits and flow packs

---

## 🚀 Getting Started

1. **Set up MQTT**  
   Install and run Mosquitto (or any MQTT broker).

2. **Install Node-RED**  
   Install Node-RED and import the `flows/` examples.

3. **Flash a FunZone node**  
   - Grab the firmware from `firmware/`
   - Flash to a Raspberry Pi Pico W (or similar)
   - Set your Wi-Fi + MQTT settings

4. **Wire up a test rig**  
   - 1x PIR or button
   - 1x LED or relay + test load
   - Optional: MP3 trigger or simple sound module

5. **Run the demo flow**  
   Use the example Node-RED flow to:
   - log events
   - trigger your output
   - confirm the node is alive

---

## 📁 Directory Layout

    /firmware      - Pico/Pico W firmware (MicroPython or C)
    /flows         - Node-RED flows (JSON)
    /docs          - Diagrams, guides, quickstarts
    /hardware      - Wiring examples, schematics, reference designs
    /tools         - Helper scripts and utilities
    LICENSE
    NOTICE
    README.md
    CONTRIBUTING.md
    ROADMAP.md

---

## 📜 License

Core FunZone software is licensed under the Apache License 2.0.  
See `LICENSE` for the full text.

Documentation may be licensed under Creative Commons CC BY 4.0.  
Premium flows, advanced tools, and hardware kits may be offered under separate commercial terms.

---

## 💬 Contributing

Contributions are welcome!

Ways to help:
- add new node firmware modules
- create Node-RED flows
- improve documentation or diagrams
- propose naming conventions
- share example installations

How to contribute:
1. Open an Issue  
2. Fork the repo  
3. Submit a PR  
4. We’ll review and merge

By contributing, you agree your contributions are licensed under Apache 2.0.

---

## ❤️ Support & Early Access

You can support FunZone by:
- buying early-access digital packs
- joining Patreon for dev notes and early builds
- sharing your projects
- submitting feedback and ideas

FunZone exists so small, weird projects can have big, weird control systems without theme-park budgets.
