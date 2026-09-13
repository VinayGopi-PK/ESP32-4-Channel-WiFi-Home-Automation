# ESP32 4-Channel Wi-Fi Home Automation

An **ESP32-based 4-channel Wi-Fi Home Automation Controller** designed for wireless control of electrical loads using four relay outputs.

The project includes a custom hardware design developed in **KiCad**, covering the schematic, PCB layout, power supply section, ESP32 programming interface, relay control circuitry, indicators, and PCB 3D visualization.

---

## Project Overview

This project is a compact **4-channel Wi-Fi Home Automation Controller** based on an ESP32 module.

The controller is designed to provide four independent relay-controlled outputs that can be operated through the ESP32's Wi-Fi connectivity.

The PCB integrates the ESP32 controller, isolated AC-to-DC power supply, 3.3 V regulation, USB programming interface, relay control circuitry, status indicators, and four relay outputs into a single custom PCB.

### Basic System Architecture

```text
                    AC INPUT
                       │
                       ▼
              ┌─────────────────┐
              │  Isolated AC-DC │
              │   Power Supply  │
              └────────┬────────┘
                       │
                       ▼
                  +5V DC Rail
                       │
             ┌─────────┴─────────┐
             │                   │
             ▼                   ▼
       3.3V Regulator       Relay Section
             │                   │
             ▼                   ▼
          ESP32 MCU        4 × Relays
             │                   │
             └─────────┬─────────┘
                       │
                 Wi-Fi Control
                       │
                       ▼
                 Home Appliances
```

---

## Main Features

* ESP32-based Wi-Fi controller
* 4 independent relay channels
* Custom PCB designed using KiCad
* Isolated AC-to-DC power supply section
* 5 V system power rail
* 3.3 V regulated supply for ESP32
* USB interface for programming and communication
* CP2102 USB-to-UART interface
* Auto-programming support
* BOOT and RESET controls
* Individual relay control circuitry
* Status indication LEDs
* Custom PCB layout
* Front and back copper routing
* 3D PCB visualization
* Manufacturing-oriented PCB design

---

## Hardware

| Component         | Function                                    |
| ----------------- | ------------------------------------------- |
| ESP32             | Main microcontroller and Wi-Fi connectivity |
| HLK-PM01          | Isolated AC-to-DC power supply              |
| AMS1117-3.3       | 3.3 V voltage regulation                    |
| CP2102            | USB-to-UART programming interface           |
| SANYOU SRD Relays | Switching of four output channels           |
| SS14              | Power protection / rectification section    |
| BOOT Button       | ESP32 boot-mode control                     |
| RESET Button      | ESP32 reset control                         |
| Status LEDs       | Power / system / channel indication         |
| Micro USB         | Power/programming interface                 |

---

## 4-Channel Relay Control

The PCB provides **four independent relay channels** for controlling external electrical loads.

```text
                    ESP32
                      │
          ┌───────────┼───────────┐───────────┐   
          │           │           │           │
          ▼           ▼           ▼           ▼
       Channel 1   Channel 2   Channel 3   Channel 4
          │           │           │           │
          ▼           ▼           ▼           ▼
       Relay 1     Relay 2     Relay 3     Relay 4
          │           │           │           │
          ▼           ▼           ▼           ▼
       LOAD 1      LOAD 2      LOAD 3      LOAD 4
```

Each relay channel is controlled independently by the ESP32.

---

## Power Supply

The PCB incorporates an **isolated AC-to-DC power supply section** to provide the required DC power for the controller.

The power architecture includes:

* AC input
* Isolated AC-to-DC conversion
* +5 V system rail
* 3.3 V regulation
* ESP32 power supply
* Relay power supply
* Power protection components

The design separates the low-voltage control circuitry from the incoming AC section through the isolated power supply.

---

## USB Programming Interface

The PCB includes a **CP2102 USB-to-UART interface** for programming and serial communication with the ESP32.

The programming section includes:

* Micro USB connector
* CP2102 USB-to-UART bridge
* ESP32 UART connection
* Auto-programming circuitry
* BOOT control
* RESET control

This allows the ESP32 firmware to be programmed without requiring a separate external USB-to-UART module.

---

## Indicators and Controls

The design includes dedicated user-interface components for operating and monitoring the controller.

### Controls

* BOOT button
* RESET button

### Indicators

* Power/system status indication
* Relay/channel status indication

The PCB uses compact SMD LEDs for status indication while retaining convenient physical controls for programming and reset operations.

---

## PCB Design

The complete PCB was designed using **KiCad**.

The design includes:

* Complete electrical schematic
* Component selection and footprint assignment
* PCB component placement
* Signal routing
* Power routing
* Ground plane
* Relay section
* AC input section
* USB programming section
* ESP32 section
* Front and back PCB layout
* 3D PCB visualization
* Manufacturing files

---

## PCB Design Preview

### Schematic

![ESP32 Home Automation Schematic](Images/ESP32%20Home%20Automation%20Schematic.JPG)

### PCB Front Layout

![ESP32 4-Channel Home Automation PCB Front Layout](Images/Front%20PCB%20Layout.JPG)

### PCB Back Layout

![ESP32 4-Channel Home Automation PCB Back Layout](Images/Back%20PCB%20Layout.JPG)

### 3D View

![ESP32 4-Channel Home Automation PCB 3D View](Images/ESP32%20Home%20Automation%20PCB%203D%20View.JPG)

---

## Design Considerations

The PCB design considers the separation between the **AC mains section and low-voltage electronics**.

Important design considerations include:

* Isolation between AC input and low-voltage circuitry
* Dedicated power distribution
* Ground-plane implementation
* Appropriate PCB clearances
* Relay switching section
* ESP32 signal routing
* USB programming interface
* Component placement
* Manufacturing requirements

> **Safety note:** This project involves mains-voltage circuitry. The PCB should only be assembled, tested, and operated by appropriately qualified personnel using suitable electrical safety practices and enclosure/isolation measures.

---

## Design Tools

* **KiCad** — Schematic and PCB design
* **ESP32** — Embedded Wi-Fi controller
* **CP2102** — USB-to-UART interface

---

## Technical Highlights

**Microcontroller:** ESP32
**Wireless Communication:** Wi-Fi
**Relay Channels:** 4
**AC-DC Power Supply:** HLK-PM01
**Logic Supply:** 3.3 V
**USB-UART:** CP2102
**Relay:** SANYOU SRD Series
**PCB Design Tool:** KiCad
**PCB Type:** Custom PCB

---

## Repository Contents

The repository contains the project design files, PCB manufacturing files, documentation, and project images.

### KiCad Project

Contains:

* KiCad schematic
* KiCad PCB layout
* KiCad project files
* Component and footprint configuration files

### Documentation

Contains project-related documentation and component information.

### Gerber Files

Contains the generated PCB manufacturing files.

### Images

Contains:

* Schematic
* PCB front layout
* PCB back layout
* PCB 3D view

---

## Project Objective

The objective of this project was to design a **compact 4-channel ESP32-based Wi-Fi Home Automation Controller** integrating wireless control, relay switching, isolated power conversion, USB programming, and custom PCB design into a single hardware platform.

The project demonstrates skills in:

* Embedded system hardware design
* ESP32-based systems
* Wi-Fi-enabled control systems
* Power supply design
* Relay control
* USB-to-UART programming
* Schematic design
* PCB layout
* Component selection
* PCB manufacturing file generation

---

## Project Type

**ESP32 Embedded System | Wi-Fi Home Automation | Relay Controller | PCB Design**

**Design Software:** KiCad
**Controller:** ESP32
