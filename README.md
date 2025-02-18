# Button-Controlled LED with Arduino

This project is part of my ongoing **Arduino learning series**, focusing on microcontrollers and embedded systems. It demonstrates how to control an LED using a push-button with a pull-down resistor.

## 🛠 Components Used:
- **Arduino Uno**
- **LED**
- **Push Button**
- **10KΩ Resistor (Pull-Down)**
- **330Ω Resistor (LED Protection)**
- **Jumper Wires**
- **Breadboard**

## 📜 How It Works:
- The **button** acts as a digital input.
- When **pressed**, the LED turns **ON**.
- When **released**, the LED turns **OFF**.
- The **pull-down resistor** ensures stable LOW input when the button is not pressed.

## 🚀 Next Steps:
- Modify the code to **toggle** the LED instead of holding the button.
- Add a **buzzer** to play sounds when pressed.
- Expand to an **LCD display** showing button press counts.


## 📂 Code:
```cpp
const int LEDpin = 13;
const int buttonPin = 12;
int buttonState = 0;

void setup() {
    pinMode(buttonPin, INPUT);
    pinMode(LEDpin, OUTPUT);
}

void loop() {
    buttonState = digitalRead(buttonPin);
    if (buttonState == HIGH) {
        digitalWrite(LEDpin, HIGH);
    } else {
        digitalWrite(LEDpin, LOW);
    }
}
