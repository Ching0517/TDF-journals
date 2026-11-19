# TDF Journals

Welcome to my learning journal for **Tangible Design & Fabrication (TDF)**! This repository documents my weekly progress, fabrication experiments, technical explorations, and reflections throughout the course.

---

## 📌 First Half of the Semester (Weeks 1 – 9)

All ideation, sketching, and early documentation from the first half of the semester are hosted on FigJam:

👉 [**View Weeks 1–9 Documentation on FigJam**](https://figma.com/board/hXR1BTe4SbWHZ1LpmUD97Q/TDF-journal?t=edSIyHwZtvgwDc9v-0)

---

## 🛠️ Second Half of the Semester (Weeks 10+)

Starting from Week 10, weekly posts are divided into two dedicated tracks: **Arduino** (sensors, microcontrollers, and circuit prototyping) and **Laser Cutter** (2D CAD design, joinery, and material fabrication).

| Week | Arduino Journal | Laser Cutter Journal | Focus / Notes |
| :--- | :--- | :--- | :--- |
| **Week 10** | [Arduino Log](./weeks/week-10-arduino.md) | [Laser Cutter Log](./weeks/week-10-lasercutter.md) | Servo motor control & acrylic finger joint enclosure |
| **Week 11** | 🍂 [Nov 6](./weeks/week-11-12-thelastleaf/2026-11-06.md) · [Nov 7](./weeks/week-11-12-thelastleaf/2026-11-07.md) · [Nov 8](./weeks/week-11-12-thelastleaf/2026-11-08.md) | *Arduino and laser cutting are covered together in each daily entry* | **The Last Leaf** — concept, wave-machine tests, sector gear design |
| **Week 12** | 🍂 [Nov 9](./weeks/week-11-12-thelastleaf/2026-11-09.md) · [Nov 10](./weeks/week-11-12-thelastleaf/2026-11-10.md) · [Nov 11](./weeks/week-11-12-thelastleaf/2026-11-11.md) · [Nov 12](./weeks/week-11-12-thelastleaf/2026-11-12.md) | *Arduino and laser cutting are covered together in each daily entry* | **The Last Leaf** — servo + ultrasonic + p5.js link, laser-cut gear, leg clamps, living-hinge skirt |
| **Week 13** | [Arduino Log](./weeks/week-13-arduino.md) | [Laser Cutter Log](./weeks/week-13-lasercutter.md) | Troubleshooting & final chassis assembly |
| **Week 14** | [Arduino Log](./weeks/week-14-arduino.md) | [Laser Cutter Log](./weeks/week-14-lasercutter.md) | Final integration, demo, and reflections |

### 🍂 Project: The Last Leaf (Weeks 11–12)

A real leaf on a hinged branch breathes, drops when a visitor comes close (ultrasonic sensor), and is wound back up by a servo and sector gear as the visitor paints a leaf on screen (p5.js + ml5 hand tracking).

👉 [**Project index, diagrams and all daily entries**](./weeks/week-11-12-thelastleaf/README.md)

---

## 📁 Repository Structure

To keep everything clean and organized, here is the file structure:

```text
├── README.md                      # Landing page (this file)
├── weeks/                         # Markdown files for weekly logs
│   ├── week-10-arduino.md
│   ├── week-10-lasercutter.md
│   ├── week-11-12-thelastleaf/    # Project: The Last Leaf (daily entries)
│   │   ├── README.md              #   project index + diagrams
│   │   ├── 2026-11-06.md
│   │   ├── ...
│   │   └── 2026-11-12.md
│   └── ...
└── assets/                        # Photos, schematics, and vector cut files
    ├── images/
    │   └── thelastleaf/           # photos, sketches, CAD renders, diagrams
    └── cad-files/
        └── thelastleaf/           # laser-cut SVGs + diagram SVGs
```
