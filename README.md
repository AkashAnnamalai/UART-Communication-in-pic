<!-- HEADER -->

<h1 align="center">🚀 UART Communication using PIC16F877A</h1>

<p align="center">
Serial Communication • Embedded C • MPLAB X • XC8
</p>

<!-- WAVING HEADER -->

<p align="center">
<img width="100%"
src="https://capsule-render.vercel.app/api?type=waving&height=180&text=UART%20Communication&fontSize=40&fontAlignY=35&color=0:00C9FF,100:92FE9D"/>
</p>

---

<!-- BADGES -->

<p align="center">

<img src="https://img.shields.io/badge/Microcontroller-PIC16F877A-blue?style=for-the-badge">

<img src="https://img.shields.io/badge/Compiler-XC8-green?style=for-the-badge">

<img src="https://img.shields.io/badge/Protocol-UART-orange?style=for-the-badge">

<img src="https://img.shields.io/badge/Language-Embedded_C-red?style=for-the-badge">

<img src="https://img.shields.io/badge/Status-Working-success?style=for-the-badge">

</p>

---

<!-- VISITOR COUNTER -->

<p align="center">
<img src="https://komarev.com/ghpvc/?username=YOUR_USERNAME&label=Profile+Views&color=0e75b6">
</p>

---

## ✨ Features

* ⚡ UART Transmit
* 📥 UART Receive
* 💡 LED ON / OFF Control
* 🔄 Full Duplex Communication
* 🧠 Baud Rate Calculation
* 🛠 Embedded C

---

## 📂 Project Structure

```plaintext
UART-PIC16F877A
│
├── main.c
├── uart.c
├── uart.h
├── README.md
└── images
```

---

## 🔌 Circuit Connection

```plaintext
PIC16F877A              USB UART
--------------------------------
RC6 (TX)     ------->   RX
RC7 (RX)     <-------   TX
GND          -------    GND
```

---

## ⚙ UART Initialization

```c
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

## 📈 GitHub Stats

(Replace `YOUR_USERNAME`)

<p align="center">

<img height="170"
src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=tokyonight"/>

<br>

<img
src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=tokyonight"/>

</p>

---

## ⭐ Support

If this project helped you:

⭐ Star this repo
🍴 Fork it
🚀 Build more embedded projects

---

<p align="center">

Made with ❤️ using PIC16F877A

</p>

<p align="center">
<img width="100%"
src="https://capsule-render.vercel.app/api?type=waving&height=120&section=footer&color=0:00C9FF,100:92FE9D"/>
</p>
