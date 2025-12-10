# 🚗 AutoPulse - Car Health Companion

Your complete automotive diagnostics and turbo boost control system with real-time OBD-II integration.

![AutoPulse](https://img.shields.io/badge/Version-1.0-orange) ![License](https://img.shields.io/badge/License-MIT-blue) ![Platform](https://img.shields.io/badge/Platform-Web-green)

---

## 🌟 Features

### Core Features
- ✅ **Real-Time OBD-II Diagnostics** - Live data from your vehicle's computer
- ✅ **Predictive Maintenance AI** - Smart alerts before problems occur
- ✅ **Health Score Calculator** - Overall vehicle condition rating
- ✅ **Smart Notifications** - Context-aware alerts and reminders
- ✅ **Trip Analytics** - Track mileage, MPG, and driving patterns
- ✅ **Cost Tracker** - Monitor all vehicle expenses

### Advanced Features
- 🚀 **Turbo Boost Control** - Monitor and adjust boost pressure (turbocharged vehicles)
- 📊 **Live Data Streaming** - Real-time sensor readings (RPM, speed, temps, boost)
- 🔧 **DTC Code Reader** - Read and clear diagnostic trouble codes
- 💾 **Data Export** - Export vehicle data as CSV/JSON
- 📈 **Performance Metrics** - Track max boost, boost events, efficiency

---

## 🚀 Quick Start (3 Steps)

### 1️⃣ Choose Your Launch Method

#### **Option A: Double-Click Launch (Easiest)**
```bash
# Windows users:
Double-click: launch.bat

# Mac/Linux users:
Double-click: launch.sh
(or run: ./launch.sh)
```

#### **Option B: Manual Python Server**
```bash
# Navigate to the folder containing the HTML file
cd /path/to/autopulse

# Start server
python3 -m http.server 8080

# Open in browser:
http://localhost:8080/car-health-companion-obd2.html
```

#### **Option C: Direct File Open**
```bash
# Simply double-click:
car-health-companion-obd2.html

# Opens directly in your default browser
```

### 2️⃣ Get an OBD-II Bluetooth Adapter

**Recommended Models:**

| Adapter | Price | Best For | Buy Link |
|---------|-------|----------|----------|
| Veepeak OBDCheck BLE+ | $29.99 | Most users | [Amazon](https://amazon.com) |
| BlueDriver Bluetooth Pro | $99.95 | Professionals | [Amazon](https://amazon.com) |
| Generic ELM327 | $10-20 | Budget option | [eBay](https://ebay.com) |

**Where to Buy:**
- Amazon (fastest delivery)
- AutoZone / O'Reilly (in-store pickup)
- eBay (cheapest prices)

### 3️⃣ Connect to Your Vehicle

1. **Locate OBD-II port** (under dashboard, driver's side)
2. **Plug in adapter** (LED should light up)
3. **Turn ignition ON** (don't start engine)
4. **Open AutoPulse app** in Chrome browser
5. **Click "Connect OBD-II"** button
6. **Select your adapter** from the list
7. **Done!** Live data starts flowing

---

## 📱 Mobile Access

### Connect from Your Phone:

1. **Make sure phone and computer are on same WiFi**
2. **Run the launch script** on your computer
3. **Note the IP address** shown (e.g., 192.168.1.100)
4. **Open Chrome on your Android phone**
5. **Visit:** `http://[IP-ADDRESS]:8080/car-health-companion-obd2.html`
6. **Bookmark it** for easy access

### Example:
```
http://192.168.1.100:8080/car-health-companion-obd2.html
```

---

## 🌐 Deploy Online (Permanent Access)

### Netlify (Recommended - Free)

1. Go to [netlify.com](https://netlify.com)
2. Sign up for free account
3. Drag and drop `car-health-companion-obd2.html`
4. Get instant URL: `https://[your-site].netlify.app`
5. Access from anywhere!

### GitHub Pages (Free)

1. Create GitHub account
2. Create new repository called "autopulse"
3. Upload HTML file (rename to `index.html`)
4. Enable GitHub Pages in Settings
5. Access at: `https://[username].github.io/autopulse`

### Vercel (Free)

1. Go to [vercel.com](https://vercel.com)
2. Sign up with GitHub
3. Import your repository
4. Automatic deployment
5. Fast global CDN

---

## 🔧 Browser Requirements

### Supported Browsers:
- ✅ **Chrome** (Desktop & Android) - Recommended
- ✅ **Edge** (Desktop)
- ✅ **Opera** (Desktop)

### NOT Supported:
- ❌ Safari (iOS/Mac) - No Web Bluetooth API
- ❌ Firefox - Web Bluetooth disabled by default
- ❌ Internet Explorer - Outdated

**Solution:** Use Chrome on Android or Desktop for full functionality.

---

## 🚀 Turbo Boost Control Setup

### For Turbocharged Vehicles

#### Monitor Boost (Works Immediately):
- Connect OBD-II adapter
- Click "Turbo Boost Control" in Quick Actions
- Live boost pressure displays automatically

#### Control Boost (Requires Hardware):
To actually adjust boost pressure, you need:

**Electronic Boost Controller Options:**
- Turbosmart e-Boost2 (~$400)
- AEM Tru-Boost Controller (~$300)
- Greddy Profec B Spec II (~$500)

**Installation:**
1. Install boost controller on turbo system
2. Wire to vehicle's wastegate
3. Connect to CAN bus or serial port
4. Configure communication protocol
5. Use AutoPulse presets to send commands

**⚠️ Important:** Current app shows boost control UI. To actually control boost, you'll need to add serial/CAN communication code specific to your boost controller model. See `DEPLOYMENT_GUIDE.md` for details.

---

## 📊 Supported OBD-II Data

### Real-Time Metrics:
- Engine RPM
- Vehicle Speed
- Engine Coolant Temperature
- Intake Air Temperature
- Throttle Position
- Fuel Level
- O2 Sensor Voltage
- Mass Air Flow Rate
- Timing Advance
- **Boost Pressure** (turbocharged vehicles)

### Calculated Metrics:
- Health Score
- Fuel Efficiency
- Driving Score
- Turbo Temperature (estimated)
- Max Boost Today

---

## 🛠️ Troubleshooting

### Can't Connect to OBD-II?

**Check:**
- ✓ Car ignition is ON
- ✓ Adapter LED is lit/blinking
- ✓ Using Chrome browser
- ✓ Adapter is in pairing mode
- ✓ Bluetooth enabled on device

**Try:**
- Restart adapter (unplug/replug)
- Clear browser cache
- Use Incognito mode
- Try different USB port (if WiFi adapter)

### No Data Showing?

**Solutions:**
- Wait 15-20 seconds after connection
- Start the engine (some cars require this)
- Check adapter compatibility with your vehicle
- Try a different OBD-II adapter
- Verify adapter supports your car's protocol

### Bluetooth Not Supported?

**Fix:**
- Update Chrome to latest version
- Use Chrome on Android (not iOS)
- Try Chrome on Desktop
- Verify Web Bluetooth API is enabled:
  - Visit: `chrome://flags`
  - Search: "Web Bluetooth"
  - Enable if disabled

### Turbo Panel Not Appearing?

**Enable:**
- Click "Turbo Boost Control" in Quick Actions panel
- Panel appears even without OBD-II connection
- Live data requires manifold pressure sensor (MAP)
- Some non-turbo cars show vacuum instead of boost

---

## 💡 Pro Tips

### For Best Experience:
1. 📱 **Mount phone** on dashboard for easy viewing
2. 🔌 **Keep phone charging** - Bluetooth drains battery
3. 🔖 **Bookmark the URL** for quick access
4. 📊 **Export data monthly** for maintenance tracking
5. 🚗 **Start with Stock preset** before increasing boost
6. 📐 **Use landscape mode** on mobile for better layout
7. 🔄 **Clear codes after repairs** to reset check engine light

### Safety Tips:
- ⚠️ Never adjust boost while driving
- ⚠️ Monitor engine temps at high boost
- ⚠️ Get professional tune before big boost increases
- ⚠️ Ensure proper supporting modifications
- ⚠️ Use dyno for safe AFR verification

---

## 📁 File Structure

```
autopulse/
├── car-health-companion-obd2.html    # Main application file
├── launch.sh                          # Mac/Linux launcher
├── launch.bat                         # Windows launcher
├── DEPLOYMENT_GUIDE.md               # Detailed setup guide
└── README.md                         # This file
```

---

## 🎯 Roadmap

### Coming Soon:
- [ ] iOS Support (when Safari adds Web Bluetooth)
- [ ] CAN bus direct integration
- [ ] Custom gauge builder
- [ ] Data visualization charts
- [ ] Cloud sync (optional)
- [ ] Multiple vehicle profiles
- [ ] Maintenance scheduler
- [ ] Parts recommendations
- [ ] Mechanic finder integration
- [ ] AR engine overlay

---

## 🤝 Contributing

Found a bug? Have a feature request? Contributions welcome!

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

---

## 📜 License

MIT License - Feel free to use, modify, and distribute.

---

## ⚠️ Disclaimer

This application is for educational and monitoring purposes. Modifying engine parameters can:
- Void warranties
- Damage engines
- Violate emissions laws
- Affect insurance

**Always consult professional tuners. Use at your own risk.**

---

## 🆘 Support

### Need Help?

**Documentation:**
- 📖 Read `DEPLOYMENT_GUIDE.md` for detailed setup
- 🔧 Check Troubleshooting section above
- 💬 Open an Issue on GitHub

**Learning Resources:**
- [OBD-II PIDs Wiki](https://en.wikipedia.org/wiki/OBD-II_PIDs)
- [ELM327 Documentation](https://www.elmelectronics.com/)
- [Turbo Basics](https://www.youtube.com/results?search_query=how+turbo+works)

**Communities:**
- Reddit: r/Cartalk, r/MechanicAdvice
- Forums: NASIOC, VWVortex, FT86Club
- Facebook: OBD-II Groups, Car Tuning Groups

---

## 🏁 Quick Launch Commands

```bash
# Mac/Linux
./launch.sh

# Windows
launch.bat

# Manual Python
python3 -m http.server 8080

# Then visit:
http://localhost:8080/car-health-companion-obd2.html
```

---

**Made with ❤️ for car enthusiasts**

**Happy tuning! 🏎️💨**
