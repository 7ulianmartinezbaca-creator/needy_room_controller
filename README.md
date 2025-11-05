# needy_room_controller
First room controller thats needy like me 

## Overview
The Smart Room Controller is a home-automation system designed for users who prefer a customizable and automatically managed environment. Inspired by *Ned the Needy Room Controller*, this project implements both automatic and manual control modes to manage temperature and lighting conditions efficiently.

Built around the **Particle Photon 2**, the controller integrates with **Philips Hue lights**, **rotary encoders**, **push buttons**, and multiple sensors to regulate devices such as a **lamp** and **fan** based on real-time environmental data or user input.

## System Features
- **Dual Operation Modes:** Automatic and manual modes for flexible control.
- **Sensor Integration:**
  - **Photodiode** for ambient-light detection.
  - **BME sensor** for temperature measurement.
- **Device Control:**
  - Photon 2 controls a **lamp** and **fan** through connected relays.
  - Two **buttons** toggle the fan and lamp in manual mode.
  - A third **button** switches the system into automatic mode.
- **Rotary Encoders:**
  - One encoder adjusts **Hue-light brightness and color**.
  - The other sets the **desired room temperature**.
- **OLED Display:** Shows current temperature and user-defined target temperature.

## System Operation
### Automatic Mode
When automatic mode is enabled:
- The **BME sensor** continuously measures room temperature.
- If the current temperature exceeds the target temperature, the **fan** turns on.
- The **photodiode** measures ambient light; if sufficient light is detected, the **Hue lights** and **lamp** automatically turn off.
- While in automatic mode, manual inputs from buttons and encoders are disabled to prevent conflicting commands.

### Manual Mode
When manual mode is active:
- **Buttons** manually toggle the lamp and fan.
- **Encoders** adjust Hue-light settings and desired temperature.
- Pressing an encoder’s push button turns the lights off.
- Automatic features are suspended until re-enabled.

## Hardware Components
- **Particle Photon 2** microcontroller  
- **BME280** (temperature, humidity, and pressure sensor)  
- **Photodiode** for light detection  
- **OLED display** (0.96" I²C)  
- **Two rotary encoders** with push buttons  
- **Three push buttons** for mode and device control  
- **Relay modules** (for lamp and fan control)  
- **Philips Hue lights** (integrated via network API)  
- Power supply, resistors, and supporting components  

## Design Intent
The purpose of this system is to maintain comfortable room conditions automatically, minimizing the need for manual adjustments. By integrating environmental sensors, networked lighting, and flexible input options, the controller offers a blend of automation, energy efficiency, and user customization.

## Future Improvements
- Add humidity-based fan control.
- Integrate motion detection for occupancy-based automation.
- Expand support for additional smart-home ecosystems (e.g., Home Assistant, Alexa).

## License
This project is open source. You may use and modify it freely for personal or educational purposes.

---

*Developed using the Particle Photon 2 and inspired by Ned the Needy Room Controller.*
