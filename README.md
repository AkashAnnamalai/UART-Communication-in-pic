<!-- HEADER -->

<h1 align="center">
🚀 UART Communication using PIC16F877A
</h1>

<p align="center">
Serial Communication using Embedded C • MPLAB X • XC8
</p>

<!-- Typing Animation -->

<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?font=Poppins&size=28&duration=3000&pause=1000&color=00D9FF&center=true&vCenter=true&width=800&lines=PIC16F877A+UART+Project;Embedded+Systems+Development;Serial+Communication+Protocol;Transmit+%26+Receive+Data;Built+using+MPLAB+X+%2B+XC8">
</p>

---

<!-- BADGES -->

<p align="center">

<img src="https://img.shields.io/badge/Microcontroller-PIC16F877A-blue?style=for-the-badge">

<img src="https://img.shields.io/badge/Compiler-XC8-success?style=for-the-badge">

<img src="https://img.shields.io/badge/Protocol-UART-orange?style=for-the-badge">

<img src="https://img.shields.io/badge/Language-Embedded_C-red?style=for-the-badge">

<img src="https://img.shields.io/badge/Status-Working-brightgreen?style=for-the-badge">

</p>

---

<!-- ANIMATED LINE -->

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00C9FF,100:92FE9D&height=120&section=header"/>

---

## ✨ Features

⚡ UART Transmission
📩 UART Reception
🔄 Full Duplex Communication
💡 LED ON / OFF Control
🧠 Baud Rate Calculation
🛠 Beginner Friendly

---

## 📷 Project Preview

<p align="center">

<img width="800"
src="https://media.giphy.com/media/f3iwJFOVOwuy7K6FFw/giphy.gif">

</p>

---

## 🔌 Circuit

```plaintext
PIC16F877A              USB UART
--------------------------------
RC6 (TX)       ----->   RX
RC7 (RX)       <-----   TX
GND            -----    GND
```

---

## ⚙ UART Configuration

```c
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

## 📊 Project Stats

<p align="center">

<img src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=tokyonight">

</p>

---

## 📈 Activity Graph

<p align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=YOUR_USERNAME&theme=react-dark">

</p>

---

## ⭐ Support

If you like this project:

🌟 Star the Repository
🍴 Fork the Project
🧠 Learn Embedded Systems

---

<p align="center">

Made with ❤️ using PIC16F877A

</p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00C9FF,100:92FE9D&height=120&section=footer"/>
