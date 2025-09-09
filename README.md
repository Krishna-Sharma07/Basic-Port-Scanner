<div align="center">
  <h1 align="center">🔎 Basic Port Scanner – Python Socket Tool</h1>
  <p align="center">
    A minimal <b>port scanning script</b> using Python's built-in <code>socket</code> library to detect open ports on a specified target.
  </p>
  <br />
  <img src="https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Socket_Library-Standard_Library-informational?style=for-the-badge" alt="Socket Library" />
</div>

---

## 📋 Table of Contents

* [🌟 Features](#features)
* [⚙️ Tech Stack](#tech-stack)
* [🚀 Getting Started](#getting-started)
* [📚 Project Structure](#project-structure)
* [🔄 How It Works](#how-it-works)
* [🚢 Deployment](#deployment)
* [🤝 Contributing](#contributing)

---

<a name="features"></a>

## 🌟 Features

### 🎯 Targeted Port Scan

* Scans well-known ports in range `1–99`
* Target is hardcoded as `apple.com`
* Uses TCP connect-ex method

### ⚡ Lightweight & Fast

* Minimal code (under 10 lines)
* Uses socket with 0.5s timeout for speed
* No external libraries

### 🧪 Great for Learning

* Understand basic network connections
* Easy to modify and extend

---

<a name="tech-stack"></a>

## ⚙️ Tech Stack

* **Language**: Python 3.10+
* **Library**: `socket` (built-in)

---

<a name="getting-started"></a>

## 🚀 Getting Started

### **Prerequisites**

* Python installed (version 3.10 or higher)
* Terminal or Command Prompt access

### **Clone the Repository**

```bash
git clone https://github.com/Krishna-Sharma07/basic-port-scanner.git
cd basic-port-scanner
```

### **Run the Script**

```bash
python scanner.py
```

---

<a name="project-structure"></a>

## 📚 Project Structure

```
basic-port-scanner/
│
├── scanner.py       # Main script with scanning logic
├── README.md        # Project documentation
└── LICENSE          # MIT License
```

---

<a name="how-it-works"></a>

## 🔄 How It Works

Here’s the core logic used in the scanner:

```python
import socket

target = "apple.com"
for port in range(1, 100):
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    s.settimeout(0.5)
    result = s.connect_ex((target, port))
    if result == 0:
        print(f"Port {port} is open")
    s.close()
```

### 🧠 What It Does:

1. Sets the target to `apple.com`
2. Iterates over ports 1 to 99
3. Attempts to connect using TCP
4. If a port is open (`connect_ex` returns 0), it prints the result
5. Each socket is closed after the attempt

---

<a name="deployment"></a>

## 🚢 Deployment

This is a terminal-based tool. No deployment needed.

Just run it with Python:

```bash
python scanner.py
```

---

<a name="contributing"></a>

## 🤝 Contributing

Want to improve the scanner?

1. Fork the repo
2. Create a branch

   ```bash
   git checkout -b add-argparse-support
   ```
3. Make your changes
4. Commit and push
5. Open a PR 🚀

---

<div align="center">
  🛠️ Built with <strong>Python & Sockets</strong> — by <strong>Krishna Sharma</strong>.
</div>

---
