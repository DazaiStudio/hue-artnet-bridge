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
```

If requirements.txt is missing, install manually:
```bash
pip install hue-entertainment-pykit
```

---

## 🚀 Usage

- Edit the script to set your Hue Bridge IP, username, and clientkey.These can be generated via the Hue Developer API or using the Hue app.
- Run the script:
```bash
python hue_artnet_bridge.py
```
- Start sending Art-Net from your lighting console or software. Hue lights in the configured Entertainment area will update in real time.

---

## ⚠️ Notes

- The Hue Bridge uses self-signed HTTPS certificates. This script disables InsecureRequestWarning for convenience. If you prefer full verification, install the Hue Bridge certificate and enable TLS checks.

- Default is 11 fixtures, each mapped to 4 DMX channels (Dimmer + R + G + B). Adjust the last_rgbs array and mapping logic if needed.

- Art-Net input is set to Universe 1, Port 6454 by default.

---

## 📜 License

MIT License.
Feel free to use and modify this project for your own setups.
