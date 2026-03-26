# 🖐️ Air Gesture Mouse Controller

> Control your mouse cursor with just your hand — no hardware required.

[![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.8+-5C3EE8?style=flat-square&logo=opencv&logoColor=white)](https://opencv.org)
[![MediaPipe](https://img.shields.io/badge/MediaPipe-0.10.9-00BCD4?style=flat-square)](https://mediapipe.dev)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=flat-square&logo=windows&logoColor=white)](https://microsoft.com/windows)

---

## 📌 Project Overview

**Air Gesture Mouse Controller** is a computer vision project that lets you control your mouse cursor using hand gestures detected via your webcam — no physical mouse needed. Built with **Python**, **OpenCV**, **MediaPipe**, and **CVZone**.

It detects your hand in real-time and translates finger positions into mouse actions like moving, clicking, right-clicking, double-clicking, and scrolling.

---

## ✨ Features

- 🖱️ **Move cursor** with index finger
- 👆 **Left click** with two fingers
- 🖱️ **Right click** with three fingers
- ✊ **Double click** with closed fist
- 🖐️ **Scroll up** with open palm
- ⚡ Smooth cursor movement with interpolation
- 🎯 Real-time hand landmark detection

---

## 🖼️ Demo

```
┌─────────────────────────────────────────────┐
│                                             │
│   Gesture          →    Action              │
│   ─────────────────────────────────         │
│   ☝️  Index finger  →    Move cursor         │
│   ✌️  Two fingers   →    Left click          │
│   🤟 Three fingers  →    Right click         │
│   ✊  Fist          →    Double click        │
│   🖐️  Open palm     →    Scroll up           │
│                                             │
└─────────────────────────────────────────────┘
```

## 🛠️ Requirements

| Tool | Version |
|------|---------|
| Python | **3.11 only** (3.12+ not supported) |
| mediapipe | 0.10.9 |
| opencv-python | 4.8.0+ |
| cvzone | 1.6.1+ |
| pyautogui | 0.9.54+ |
| numpy | 1.24.0+ |
| Webcam | Any USB or built-in webcam |

> ⚠️ **Important:** MediaPipe only supports Python 3.11. Python 3.12 and 3.13 are NOT compatible.

---

## 🚀 Installation

### Step 1 — Clone the repository

```bash
git clone https://github.com/yourusername/air-gesture-mouse.git
cd air-gesture-mouse
```

### Step 2 — Make sure Python 3.11 is installed

Download from: https://www.python.org/downloads/release/python-3119/

✅ Check "Add Python to PATH" during installation.

### Step 3 — Install dependencies

```bash
py -3.11 -m pip install -r requirements.txt
```

### Step 4 — Run the program

```bash
py -3.11 air_mouse.py
```

---

## 🎮 How to Use

1. Run the program — your webcam will open
2. Place your hand **30–50 cm** in front of the camera
3. Use gestures from the table below:

| Gesture | Action |
|---------|--------|
| ☝️ Index finger only | Move cursor |
| ✌️ Index + Middle finger | Left click |
| 🤟 Index + Middle + Ring finger | Right click |
| ✊ All fingers closed (fist) | Double click |
| 🖐️ All fingers open | Scroll up |

4. Press **Q** on the camera window to quit

### Tips for best performance
- Use in a **well-lit room**
- Keep your hand **steady** for precise clicks
- Stay **30–50 cm** away from the webcam
- Use a **plain background** if detection is poor

---

## ⚙️ Configuration

You can tweak these values inside `air_mouse.py`:

```python
smooth = 7       # Cursor smoothness (higher = smoother but slower)
click_cooldown = 25  # Frames between clicks (higher = less accidental clicks)
detectionCon = 0.8   # Hand detection confidence (0.0 to 1.0)
```

---

## 🐛 Troubleshooting

| Problem | Solution |
|---------|----------|
| `AttributeError: module 'mediapipe' has no attribute 'solutions'` | Use Python 3.11 and `mediapipe==0.10.9` |
| Camera not opening | Change `cv2.VideoCapture(0)` to `cv2.VideoCapture(1)` |
| Cursor shaking too much | Increase `smooth` value (e.g., `smooth = 10`) |
| Accidental double clicks | Increase `click_cooldown` value |
| Hand not detected | Improve lighting or use a plain background |

---

## 📁 Project Structure

```
air-gesture-mouse/
│
├── air_mouse.py        # Main program
├── requirements.txt    # Python dependencies
├── LICENSE             # MIT License
├── .gitignore          # Git ignore rules
└── README.md           # Project documentation
```

---

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- [MediaPipe](https://mediapipe.dev) by Google — hand landmark detection
- [CVZone](https://github.com/cvzone/cvzone) by Murtaza Hassan — hand tracking module
- [OpenCV](https://opencv.org) — computer vision library
- [PyAutoGUI](https://pyautogui.readthedocs.io) — mouse and keyboard control

---

<div align="center">
  Made with ❤️ using Python & Computer Vision
</div>
