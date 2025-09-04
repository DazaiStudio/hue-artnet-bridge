# Hue Art-Net Bridge

A Python bridge that listens for **Art-Net (DMX over IP)** packets and maps them to **Philips Hue Entertainment** lights in real time.  
This allows you to control Hue lights with lighting desks, media servers, or any Art-Net capable software.

---

## ✨ Features
- Parses Art-Net **ArtDMX** packets on a specified universe.
- Extracts RGB values with **dimmer channel support**.
- Streams real-time RGB data to Hue lights via the **Hue Entertainment API v2**.
- Supports multiple fixtures (default: 11).

---

## 📦 Requirements
- **Python 3.9+**
- [hue-entertainment-pykit](https://pypi.org/project/hue-entertainment-pykit/)
- Local **Philips Hue Bridge** (with Entertainment area configured)
- Local network connection to the Hue Bridge

---

## 🔧 Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/yourusername/hue-artnet-bridge.git
cd hue-artnet-bridge
pip install -r requirements.txt


