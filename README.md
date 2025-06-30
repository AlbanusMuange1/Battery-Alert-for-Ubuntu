
---

````markdown
# 🔋 Battery Alert for Ubuntu

**Battery Alert** is a lightweight desktop utility written in Python to notify you when:

- Your battery is **above a certain threshold** (e.g., 80%) — reminder to unplug the charger.
- Your battery is **below a certain threshold** (e.g., 30%) — reminder to plug in the charger.

It plays customizable alert sounds and shows desktop notifications using Zenity.

---

## ✅ Features

- Customizable battery charge thresholds
- GUI popup alerts using Zenity
- Different audio alerts for high and low battery warnings
- Runs in the background with minimal resource usage
- Starts automatically on system boot
- Packaged as a `.deb` installer for Ubuntu

---

## 📦 Installation

Download and install the `.deb` package:

```bash
sudo dpkg -i battery-alert.deb
````

To fix any missing dependencies:

```bash
sudo apt --fix-broken install
```

---

## 🛠️ Usage

Run the application:

```bash
battery-alert --threshold 85 --low
```

**Options:**

| Flag          | Description                        | Default  |
| ------------- | ---------------------------------- | -------- |
| `--threshold` | Battery % to alert when too high   | 80       |
| `--low`       | Also alert if battery is below 30% | Disabled |

---

## 🎵 Sound Alerts

* High battery sound: `~/Sounds/button-1.wav`
* Low battery sound: `~/Sounds/battery_alert.wav`

You can replace these files with your preferred `.wav` audio clips.

---

## 🔁 Autostart on Boot

After installation, the app adds itself to startup using a `.desktop` entry in:

```
~/.config/autostart/battery_alert.desktop
```

If needed, you can edit this file to change threshold values or sound locations.

---

## 🧱 Dependencies

* Python 3
* `psutil`
* `zenity`
* `paplay` (PulseAudio utility)

Install them manually if not bundled:

```bash
sudo apt install python3 python3-psutil zenity pulseaudio-utils
```

---

## 🐛 Testing

Simulate a high battery warning:

```bash
battery-alert --threshold 1
```

Simulate a low battery warning:

```bash
battery-alert --threshold 100 --low
```

---

## 📜 License

MIT License
© 2025 \[Albanus Muange Mutunga]

---

## 🤝 Contributions

Feel free to fork this repo, suggest improvements, or submit pull requests. Contributions are welcome!

```

---

Let me know if you’d like to include screenshots, badges, or GitHub Actions CI/CD instructions later.
```
