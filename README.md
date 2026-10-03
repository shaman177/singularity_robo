# 🤖 Department Inauguration Robot

A remotely controlled humanoid robot designed and developed for department inauguration and college events.

The robot combines **embedded systems, robotics, automation, human-machine interaction, and AI-powered voice generation** into a compact 4-foot platform.

---

## 📌 Project Overview

The Department Inauguration Robot is a ~120 cm humanoid-style robot capable of:

- Remote-controlled movement
- Forward, reverse, left and right movement
- In-place rotation using differential drive
- Two-hand **Namaste** gesture
- Animated face display
- Voice-based welcome messages
- Carrying a tray for inauguration activities
- Assisting in ribbon-cutting ceremonies
- Optional AI-generated speech using an external API

The robot is controlled using a **Raspberry Pi 3B+** as the main computing unit.

---

## 🎯 Objectives

The main objective of the project is to build a functional humanoid robot capable of participating in a real-world college inauguration ceremony.

### Primary Goals

1. Build a stable mobile robotic platform.
2. Implement reliable wireless remote control.
3. Create a mechanical two-hand Namaste mechanism.
4. Add an animated face display.
5. Implement voice-based interaction.
6. Integrate all subsystems into a single robotic platform.
7. Maintain a lightweight and low-cost design.

---

## 🧠 System Architecture

```text
                    ┌─────────────────────┐
                    │   RC Transmitter    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    RC Receiver      │
                    └──────────┬──────────┘
                               │
                               ▼
┌───────────────────────────────────────────────────┐
│                Raspberry Pi 3B+                   │
│                                                   │
│  ┌────────────┐  ┌────────────┐  ┌────────────┐ │
│  │ Motor Ctrl │  │ Servo Ctrl │  │ Face/Voice │ │
│  └─────┬──────┘  └─────┬──────┘  └─────┬──────┘ │
└────────┼────────────────┼────────────────┼────────┘
         │                │                │
         ▼                ▼                ▼
   Motor Driver       PCA9685         Display /
         │                │            Speaker
         ▼                ▼
    DC Motors         MG946R
         │             Servo
         ▼                │
      Wheels             ▼
                    Namaste Arms
