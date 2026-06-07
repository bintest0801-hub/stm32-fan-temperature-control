# STM32 Fan Temperature Control 🌡️

An automatic fan speed control system using STM32F1, 
monitoring temperature via DHT11 sensor and adjusting 
fan speed through PWM. Supports both manual button 
control and UART remote control.

## ⚙️ Features

- **Auto mode:** Fan speed adjusts automatically based on temperature threshold
- **Manual mode:** 4 speed levels via push buttons (0% / 40% / 60% / 100%)
- **UART control:** Remote speed control via serial commands (1/2/3/4/5)
- **LCD display:** Real-time temperature, humidity and fan speed on LCD 16x2 I2C
- **LED indicators:** 3 LEDs showing temperature range (low / medium / high)
- **Interrupt-driven:** Button inputs handled via EXTI interrupts

## 🛠️ Hardware

| Component | Details |
|---|---|
| MCU | STM32F1xx |
| Sensor | DHT11 (Temperature & Humidity) |
| Display | LCD 16x2 (I2C - STM32 HAL) |
| Fan | DC Fan via PWM (TIM2 CH2) |
| Control | 4x Push buttons (EXTI interrupt) |
| Communication | UART / Bluetooth |

## 🔧 PWM Speed Levels

| Button | Speed |
|---|---|
| Button 1 | 0% (Stop) |
| Button 2 | 40% |
| Button 3 | 60% |
| Button 4 | 100% |
| Button 5 | Auto (DHT11 controlled) |

## 📁 Project Structure
```
stm32-fan-temperature-control/
├── src/
│   ├── main.c              # Main firmware
│   ├── stm32f1xx_it.c      # Interrupt handlers (EXTI)
│   └── N6_LCD.c            # LCD I2C driver
└── README.md
```
## 🎓 Academic Info

- **Project type:** Major Course Project
- **University:** Hanoi University of Industry (HAUI)
- **Major:** Electronics & Telecommunications
- **Year:** 2025
