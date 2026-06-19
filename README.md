<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&height=300&color=0:0F2027,50:203A43,100:2C5364&text=UART%20using%20PIC16F877A&fontSize=42&fontColor=ffffff&animation=fadeIn"/>

# 🚀 UART Communication using PIC16F877A

### Serial Communication using Embedded C • MPLAB X • XC8

<img src="https://readme-typing-svg.demolab.com?font=Poppins&weight=700&size=24&pause=1000&color=36BCF7&center=true&vCenter=true&width=700&lines=Transmit+and+Receive+Data;UART+Protocol+Implementation;Embedded+Systems+Project;Built+with+PIC16F877A"/>

<br>

<img src="https://img.shields.io/badge/PIC16F877A-0096FF?style=for-the-badge&logo=microchip&logoColor=white">

<img src="https://img.shields.io/badge/XC8-13AA52?style=for-the-badge">

<img src="https://img.shields.io/badge/UART-FF7A00?style=for-the-badge">

<img src="https://img.shields.io/badge/Embedded_C-EF4444?style=for-the-badge">

<img src="https://img.shields.io/badge/Status-Working-success?style=for-the-badge">

</div>

---

## ✨ About Project

This project demonstrates **UART communication using PIC16F877A**.

Features:

⚡ Serial Transmission
📩 Serial Reception
💡 LED Control (ON / OFF)
🔄 Full Duplex Communication
🧠 Baud Rate Configuration

---

## 🧩 Architecture

```plaintext id="k9teiy"
PC Serial Monitor
        │
        │ UART
        ▼
+----------------+
| PIC16F877A     |
|                |
| RC6 → TX       |
| RC7 ← RX       |
+----------------+
        │
        ▼
      LED
```

---

## ⚙ UART Setup

```c id="snn6j7"
#define _XTAL_FREQ 20000000

void UART_init()
{
TRISCbits.TRISC6=1;
TRISCbits.TRISC7=1;

SPBRG=129;

TXSTA=0x24;
RCSTA=0x90;
}
```

---

## 📤 Example

```plaintext id="4h5u0f"
INPUT   → ON
OUTPUT  → LED ON

INPUT   → OFF
OUTPUT  → LED OFF
```

---

## 📂 Folder Structure

```plaintext id="1sscxm"
UART-PIC16F877A
├── main.c
├── uart.c
├── uart.h
├── README.md
└── Images
```

---

<div align="center">

### ⭐ Star this Repository if it helped

<img src="https://capsule-render.vercel.app/api?type=waving&height=160&section=footer&color=0:2C5364,100:0F2027"/>

</div>
