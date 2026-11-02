# SmartKey Gait Analysis — Ecosystem & Android Mobile Client

> A biometric IoT access key ecosystem combining microcontroller firmware with a cross-platform Android mobile application built with **React 18**, **TypeScript**, and **Capacitor 8**.

---

## 📌 Project Overview

**SmartKey Gait Analysis** is an intelligent security and access system designed to authenticate users based on gait biometrics captured via wearable sensor hardware, paired seamlessly with a dedicated Android companion application for real-time telemetry, bypass management, and device configuration.

* **Repository:** [reinh20/SmartKey-App](https://github.com/reinh20/SmartKey-App)
* **Author / Developer:** Reinbrandt Malikiyano Cahyono ([@reinh20](https://github.com/reinh20))

---

## 👨‍💻 My Role & Contribution Scope

> **Role: Mobile Client Application & UI Interaction Engineer**

* **Frontend & Mobile Architecture:** Architected and implemented the cross-platform Android mobile application using **React 18**, **TypeScript**, **Vite**, and **Capacitor 8**.
* **UI/UX & Interactive Design:** Designed modern, responsive user control interfaces, telemetry status indicators, touch-optimized button flows, modals, and charts using **TailwindCSS**, **Radix UI / Shadcn UI**, and **Recharts**.
* **Hardware Connectivity (BLE):** Integrated Bluetooth Low Energy (BLE) peripheral discovery, connection handling, and message parsing via `@capacitor-community/bluetooth-le`.
* **Local Data Persistence:** Implemented offline-first local storage and history caching utilizing SQLite via `@capacitor-community/sqlite`.

*(Note: The embedded gait machine learning classifier and biomechanical feature extraction algorithms on the microcontroller were developed by the hardware/AI research team).*

---

## 🏗️ Repository Architecture

```text
SmartKeyGaitAnalysis/
├── Mobile-app/                     # Android mobile companion application
│   ├── android/                    # Native Android wrapper (Capacitor bridge)
│   ├── src/
│   │   ├── app/
│   │   │   ├── components/         # Modular UI components (AuthScan, Radar, Modals, Logs)
│   │   │   ├── context/            # Global state (BLEContext, device connectivity)
│   │   │   └── services/           # SQLite database services & storage management
│   │   ├── styles/                 # TailwindCSS and custom themes
│   │   └── main.tsx                # Application root entry point
│   ├── capacitor.config.json       # Native Capacitor configuration
│   ├── package.json                # Dependencies and build scripts
│   └── vite.config.ts              # Vite bundler configuration
│
├── Firmware-ESP32/                 # ESP32 wireless Bluetooth communication firmware
│   ├── src/
│   │   └── main.cpp                # ESP32 BLE peripheral handlers
│   └── platformio.ini              # PlatformIO build configuration
│
└── Filmware/                       # Arduino Nano RP2040 embedded sensor firmware
    ├── src/nano/                   # IMU sensor acquisition & gait analysis pipeline
    └── platformio.ini              # PlatformIO configuration
```

---

## 🛠️ Tech Stack

### Mobile Application
* **Framework:** React 18, TypeScript, Vite
* **Native Mobile Bridge:** Capacitor 8 (Android Platform)
* **Styling & UI:** TailwindCSS, Radix UI / Shadcn UI, Lucide Icons, Emotion
* **Data Visualization:** Recharts, Canvas Confetti
* **Hardware & Storage:** `@capacitor-community/bluetooth-le`, `@capacitor-community/sqlite`, `@capacitor/filesystem`

### Embedded Firmware
* **Microcontrollers:** ESP32, Arduino Nano RP2040
* **Languages:** C / C++
* **Development Environment:** PlatformIO, Arduino Framework

---

## 📱 Mobile App Features

1. **BLE Device Discovery & Pairing:** Fast wireless scan and pairing with the SmartKey wearable hardware.
2. **Real-Time Authentication Panel (`AuthScanPanel`):** Visual indicators providing instant feedback on biometric verification and access state.
3. **Emergency Bypass Modal (`EmergencyBypassModal`):** Secure fallback access verification using PIN authentication and audit logging.
4. **Interactive Telemetry & Radar (`RadarDisplay`):** Real-time spatial tracking and sensor status rendering.
5. **Local Logging & History (`LogSheet`):** SQLite-backed activity logging for offline auditing and session export.

---

## 🚀 Getting Started

### Running the Mobile Application
1. **Prerequisites:** Node.js (v18+) and pnpm/npm installed. Android Studio for APK builds.
2. **Navigate to the app directory:**
   ```bash
   cd Mobile-app
   ```
3. **Install dependencies:**
   ```bash
   npm install
   ```
4. **Start Vite development server:**
   ```bash
   npm run dev
   ```
5. **Sync with Android Studio (Capacitor):**
   ```bash
   npx cap sync android
   npx cap open android
   ```

---

## 📜 License & Acknowledgments

Developed by **Reinbrandt Malikiyano Cahyono** and project collaborators for the SmartKey Gait Analysis initiative.
