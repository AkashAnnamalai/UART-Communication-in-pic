# 🚀 UART Communication using PIC16F877A

![PIC16F877A](https://img.shields.io/badge/Microcontroller-PIC16F877A-blue)
![XC8](https://img.shields.io/badge/Compiler-XC8-green)
![Protocol-UART-orange)
![Status-Working-success](https://img.shields.io/badge/Status-Working-success)

## 📌 Project Overview

This project demonstrates **UART (Universal Asynchronous Receiver Transmitter)** communication using **PIC16F877A**.

Using UART, the PIC can:

* 📤 Send data to Serial Monitor
* 📥 Receive data from Serial Monitor
* 💡 Control outputs (LED ON/OFF)
* 🔄 Perform full duplex communication

This project is useful for:

* Embedded Systems Beginners
* UART Protocol Learning
* PIC Microcontroller Practice
* Serial Communication Projects

---

## 🛠 Hardware Required

| Component                  | Quantity |
| -------------------------- | -------- |
| PIC16F877A                 | 1        |
| Crystal Oscillator (20MHz) | 1        |
| Capacitors (22pF)          | 2        |
| LED                        | 1        |
| Resistor (330Ω)            | 1        |
| USB to UART Converter      | 1        |
| Breadboard / PCB           | 1        |

---

## ⚙️ Configuration

### Microcontroller

```c
#define _XTAL_FREQ 20000000
```

### UART Settings

```text
Baud Rate : 9600
Data Bits : 8
Parity    : None
Stop Bits : 1
```

---

## 📂 Project Structure

```plaintext
UART-PIC16F877A/
│
├── main.c
├── uart.c
├── uart.h
├── README.md
└── images/
```

---

## 🔌 Circuit Connection

```plaintext
PIC16F877A              USB UART
--------------------------------
RC6 (TX)      ------->  RX
RC7 (RX)      <-------  TX
GND           -------   GND
```

---

## 💻 UART Initialization

```c
void UART_init()
{
    TRISCbits.TRISC6 = 1;
    TRISCbits.TRISC7 = 1;

    SPBRG = 129;      // 9600 Baud @20MHz

    TXSTA = 0x24;
    RCSTA = 0x90;
}
```

---

## 📤 UART Transmit Function

```c
void UART_write(char data)
{
    while(!TXSTAbits.TRMT);

    TXREG = data;
}
```

### Explanation

* Wait until previous transmission completes
* Load data into `TXREG`
* UART sends automatically

---

## 📥 UART Receive Function

```c
char UART_read()
{
    while(!PIR1bits.RCIF);

    return RCREG;
}
```

### Explanation

* Wait for incoming data
* Read received byte from `RCREG`

---

## ▶️ Example Output

### Send:

```text
ON
```

### Serial Monitor:

```text
LED ON
```

---

### Send:

```text
OFF
```

### Serial Monitor:

```text
LED OFF
```

---

## 🧠 UART Formula

```text
SPBRG = (Fosc / (64 × Baud)) − 1
```

Example:

```text
Fosc = 20MHz
Baud = 9600

SPBRG = 129
```

---

## 🚀 How to Run

1. Open project in MPLAB X IDE
2. Select XC8 Compiler
3. Build Project
4. Flash to PIC16F877A
5. Open Serial Monitor
6. Set Baud = **9600**
7. Send text

---

## 📷 Demo

Add project screenshot here:

```plaintext
images/output.png
```

---

## 📚 Concepts Covered

✔ UART Protocol
✔ Serial Communication
✔ TX/RX Registers
✔ Baud Rate Calculation
✔ PIC16F877A Programming
✔ Embedded C

---

## 🤝 Contributing

Pull requests are welcome.

If you found this project useful, give ⭐ to support.

---

## 👨‍💻 Author

**Akash R**

Made with ❤️ using PIC16F877A
