# Alfa AWUS036ACM WiFi Adapter Setup and Testing 🚀

Welcome to my blog!  
This page is fully dedicated to setting up and testing the **Alfa AWUS036ACM WiFi adapter** with Kali Linux and Raspberry Pi.

Here you'll find:

✅ How to install the drivers  
✅ How to enable monitor mode  
✅ Basic WiFi testing (packet injection test)  
✅ Small practical examples

---

## 🔥 Project Overview

The **Alfa AWUS036ACM** is a powerful WiFi adapter known for its excellent range, strong monitor mode support, and compatibility with penetration testing tools.

This guide will help you set it up and perform basic wireless security testing.

---

## 📖 Sections

- [1. About the Alfa AWUS036ACM Adapter](#1-about-the-alfa-awus036acm-adapter)
- [2. Installing the Driver on Kali Linux](#2-installing-the-driver-on-kali-linux)
- [3. Enabling Monitor Mode](#3-enabling-monitor-mode)
- [4. Basic Practical Tests](#4-basic-practical-tests)
- [5. Final Thoughts](#5-final-thoughts)

---

# 1. About the Alfa AWUS036ACM Adapter

- Dual-band support (2.4GHz and 5GHz WiFi)
- USB 3.0 for high-speed data transfer
- Chipset: **MediaTek MT7612U**
- Supports monitor mode and packet injection

This makes it perfect for learning WiFi security and ethical hacking.

---

# 2. Installing the Driver on Kali Linux

✅ Good news — as of the latest Kali Linux versions, the AWUS036ACM works **out of the box**!

But if you ever need to manually install drivers, you can:

```bash
sudo apt update
sudo apt install realtek-rtl88xxau-dkms
```

(You might need this if you ever switch to older kernels or custom systems.)

---

# 3. Enabling Monitor Mode

To enable monitor mode on the Alfa adapter:

```bash
sudo ip link set wlan1 down
sudo iwconfig wlan1 mode monitor
sudo ip link set wlan1 up
```

Check if monitor mode is enabled:

```bash
iwconfig
```

You should now see `Mode:Monitor` for `wlan1`.

---

# 4. Basic Practical Tests

✅ **Check available networks:**

```bash
sudo airodump-ng wlan1
```

✅ **Test packet injection:**

```bash
sudo aireplay-ng --test wlan1
```

✅ **Capture WiFi handshakes (for learning only):**

```bash
sudo airodump-ng wlan1
```

(Target an open network you control, or your own router for legal testing!)

---

# 5. Final Thoughts

The **Alfa AWUS036ACM** is an excellent choice for cybersecurity students, hobbyists, and wireless researchers.

With its plug-and-play support on Kali Linux, strong performance, and reliable packet injection, it's a tool worth mastering!

---

### Stay tuned for more WiFi security experiments soon! 🚀

