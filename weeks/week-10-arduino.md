# TUI | Lab 1: LED Blinking — Light Painting with 3 Pixels

<img width="720" height="414" alt="1_LmV0mAGZ6c_rSPCJOFd94g" src="https://github.com/user-attachments/assets/11d8e9b9-ab31-4fec-9197-52a56c2f1ab7" />

## Setup
- Red LED * 1, Green LED * 1, Blue LED * 1
- 220 Ohms-resistors * 3
- Breadboard
- Wires
- USB-C Connector
## Description
For our first Tangible UI lab, the goal was to take the foundational Arduino “Blink” example and transform it into a controllable, expressive light pattern.

<img width="720" height="494" alt="1__DaZ8BWSgT5LIC0IhRAgrg" width="30%" src="https://github.com/user-attachments/assets/3e5c5dd0-b46b-4bae-8c38-7fa4190c3302" />

Building on this foundation, I introduced a playful physical interaction: long-exposure light painting — much like capturing car light trails at night or spelling words in the air with sparklers on New Year’s Eve.

With game day around the corner, I decided to paint a digital cheer for the football team: “**CAL**”.

I lined up the three LEDs vertically on a breadboard: Red, Green, Blue from bottom to top. I encoded the letters using a simple binary matrix, where 1 = ON and 0 = OFF.

<img width="607" height="247" alt="1_rrutpquqniYd2xZaNYMlbw" src="https://github.com/user-attachments/assets/e45d0a12-9ee0-4769-96f2-cc651592370e" />

With the camera set to long-exposure mode, I pushed the breadboard horizontally from left to right. As it moved, the LEDs blinked through the sequence column by column. For instance, the letter “C” was coded into three sequential steps:

- Step 1: (R=1, G=1, B=1)
- Step 2: (R=1, G=0, B=1)
- Step 3: (R=1, G=0, B=1)
Using this same logic, “A” and “L” followed right after, turning the blinking lights into readable glowing letters. Go Bears!

## Behind the Scenes
It took a lot of trial and error to find the sweet spot between shutter speed, moving speed, and blinking frequency. To eliminate ambient light reflections, I ended up hiding inside my walk-in closet in near-total darkness to shoot the final exposures!

### Calibration & Setup Details:
- Exposure Time: 8.0 seconds
- ISO: 50 (kept at minimum to eliminate grain and prevent light-trail glare)
- Travel Distance: ~45 cm (manually sweeping the breadboard horizontally)

Press enter or click to view image in full size

<details>
<summary>Arduino Code</summary>

```cpp
const int pinRed = 11;
const int pinGreen = 12;
const int pinBlue = 13;

const int stepDelay = 300; 
const int charSpacing = 1000;

void setLEDs(bool r, bool g, bool b) {
  digitalWrite(pinRed, r ? HIGH : LOW);
  digitalWrite(pinGreen, g ? HIGH : LOW);
  digitalWrite(pinBlue, b ? HIGH : LOW);
  delay(stepDelay);
  clearLEDs(); delay(stepDelay);
}

void clearLEDs() {
  digitalWrite(pinRed, LOW);
  digitalWrite(pinGreen, LOW);
  digitalWrite(pinBlue, LOW);
}

void setup() {
  pinMode(pinRed, OUTPUT);
  pinMode(pinGreen, OUTPUT);
  pinMode(pinBlue, OUTPUT);
}

void loop() {
  clearLEDs();

  // letter "C"
  setLEDs(1, 1, 1);
  setLEDs(1, 0, 1);
  setLEDs(1, 0, 1);
  clearLEDs(); delay(charSpacing);

  // letter "A"
  setLEDs(1, 1, 0);
  setLEDs(0, 1, 1);
  setLEDs(1, 1, 0);
  clearLEDs(); delay(charSpacing);

  // letter "L"
  setLEDs(1, 1, 1);
  setLEDs(1, 0, 0);
  setLEDs(1, 0, 0);
  clearLEDs(); delay(charSpacing);
}
```

</details>
<p float="left">
  <img src="https://github.com/user-attachments/assets/cdab48e4-8f39-47e4-94cf-efdfd7ee018b" width="32%" />
  <img src="https://github.com/user-attachments/assets/b61f50f3-ac36-4e30-a9be-6ef90afb3061" width="32%" />
  <img src="https://github.com/user-attachments/assets/7e6462a7-de77-4f8e-baea-3405eb5ed3c6" width="32%" />
</p>
