# Smart Factory IoT Network (Cisco Packet Tracer)

A smart factory simulation built in Cisco Packet Tracer that combines a wired and wireless network with a wide range of IoT devices: access control, fire safety, lighting, ventilation, vehicle monitoring, weather sensing, and a renewable power source. All devices are registered on a central IoT server and can be monitored and controlled from a smartphone.

---

##  Overview

The project models an automated factory where sensors and actuators work together to provide security, safety, comfort, and energy management. Devices are grouped into zones, connected through a wireless router and microcontroller boards (MCUs), and managed from one web dashboard. It demonstrates networking, IoT integration, and automation logic.

##  Key Features

- **Centralized monitoring:** every device appears in the IoT Server dashboard with its live status.
- **Remote control:** devices can be monitored and controlled from a smartphone through a web browser.
- **Automation rules:** conditions can be defined so devices react automatically to sensor events.
- **Access control:** RFID cards and reader control the factory door.
- **Fire safety:** smoke and fire detection with siren and sprinkler response.
- **Renewable energy:** solar panel charging a battery.
- **Smart lighting and ventilation:** lights and fans respond to motion.

##  Network Architecture

| Device | Role |
|---|---|
| Factory-Server (Server-PT) | Factory server |
| Factory-Switch (2960-24TT) | Connects the server, PC, router, and wireless router |
| PC0 | Administration workstation |
| Router0 / Router1 (2911) | Routing between the factory network and the external network |
| Cable Modem0 and Cloud0 | Simulated internet / service provider connection |
| Access Point0 | Wireless access for external smartphones |
| Wireless Router (WRT300N) | Wireless gateway connecting all IoT devices |
| Smartphone0 / Smartphone2 | Monitoring and control from mobile devices |

##  IoT Zones and Devices

| Zone | Devices | Purpose |
|---|---|---|
|  Access & Power | RFID Card 1, RFID Card 2, RFID Reader, Door, Solar Panel, Battery | Secure entry and solar energy storage |
|  Lighting | LED IoT3, LED IoT5, LED IoT7 | Indicator and area lighting |
|  Comfort & Security | Window, Motion Detector, Fan, Fan2, Light, MCU2 | Motion-based light and fan control |
|  Fire Safety | Smoke Detector, Fire Monitor, Fire Sprinkler, Siren, Heating Element, MCU0 | Fire detection and response |
|  Vehicle & Street | Street Lamp, Old Car, Motion Detector, Garage Door | Parking and outdoor lighting |
|  Weather | Wind Sensor, LED, MCU1 | Wind monitoring with indicator |
|  Perimeter | Trip Sensor | Detects crossing of a protected line |

##  IoT Server Dashboard

The smartphone connects to the wireless network and opens the IoT server page:

```
http://192.168.10.10/home.html
```

The dashboard lists every registered device (smoke sensor, street lamp, garage door, trip sensor, lights, siren, battery, door, RFID reader, window, motion detector, fans, fire sensor, wind sensor, LEDs, and the MCUs) with a status indicator. From it you can:

- **Home:** view and control all devices.
- **Conditions:** create if-then rules between devices.
- **Editor:** edit device settings.


##  Example Automation Scenarios

> [Verify and edit these to match the conditions you created]

| Trigger | Action |
|---|---|
| Smoke or fire detected | Siren turns on and sprinkler activates |
| Motion detected in the room | Light and fan turn on |
| Valid RFID card at the reader | Door opens |
| Motion detected at the garage | Garage door opens |
| Wind sensor above threshold | Indicator LED changes state |
| Trip sensor beam interrupted | Alert is triggered |

##  How to Run

1. Install **Cisco Packet Tracer** [version].
2. Download the project file `Smart-Factory.pkt` from this repository.
3. Open it in Packet Tracer.
4. Wait until the links turn green (the simulation converges).
5. Click **Smartphone0**, then **Desktop**, then **Web Browser**.
6. Open `http://192.168.10.10/home.html` and sign in [username / password].
7. Control the devices or trigger events (for example, move a motion detector's target) and watch the reactions.

##  Repository Structure

```
├── Smart-Factory.pkt            # Packet Tracer project file
├── Images/
│   ├── All_devices_of_factor.png    # Full network topology
│   └── Monitoring.png               # IoT dashboard
└── README.md
```

##  Skills Demonstrated

- Network design and configuration (switching, routing, wireless)
- IoT system integration and device registration
- Microcontroller (MCU) based automation
- Conditional logic and event-driven control
- Remote monitoring through a web interface

