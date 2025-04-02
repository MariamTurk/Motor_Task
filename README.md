# 🔁 Arduino Motor Speed & Direction Control with Potentiometer + LCD

This Arduino project allows you to control the speed and direction of a DC motor using a potentiometer. The motor is driven by an L293D motor driver, and a 16x2 LCD displays live data such as speed, angle, and direction.

---

## 📦 Components Used

- Arduino UNO
- L293D Motor Driver
- DC Motor
- Potentiometer (10kΩ)
- 16x2 LCD Display
- Power Supply
- Jumper Wires
- Breadboard (optional)

---

## ⚙️ Pin Configuration

| Component         | Arduino Pin |
|------------------|-------------|
| Potentiometer     | A4          |
| L293D Enable A    | 11 (PWM)    |
| L293D IN1         | 9           |
| L293D IN2         | 10          |
| LCD RS            | 7           |
| LCD EN            | 6           |
| LCD D4            | 3           |
| LCD D5            | 4           |
| LCD D6            | 5           |
| LCD D7            | 2           |

---

## 🔧 How It Works

- The **potentiometer** determines both the speed and direction of the motor:
  - Values above 512 → Forward
  - Values below 512 → Reverse
  - Value ~512 → Stop
- The **motor speed** is controlled via PWM signal on the Enable pin.
- The **LCD** displays:
  - Current motor speed (0–255)
  - Mapped angle (0–180 degrees)
  - Direction (`FWD`, `REV`, or `STOP`)
- **Serial Monitor** output provides additional debugging info.

---

## 🖥️ Sample Output

### 📟 LCD Display

Speed: 180 Ang: 140 FWD

### 🛠 Serial Monitor

Pot Value: 800 | Speed: 144 | Angle: 105 | Direction: Forward


---

## 🏁 Getting Started

1. Wire the components as per the pin configuration above.
2. Upload the Arduino sketch (`main.ino`) to your board.
3. Open the Serial Monitor (9600 baud) for real-time logs.
4. Turn the potentiometer to control the motor.
5. Watch motor data update on the LCD.

---
