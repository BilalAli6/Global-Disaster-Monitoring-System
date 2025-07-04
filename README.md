
# 🌍 Global Disaster Monitoring System

A real-time Python system that monitors **weather**, **earthquakes**, and **volcanic eruptions** worldwide using public APIs. It highlights **RARE or hazardous events** in the terminal using clean color-coded boxes and saves a full log in JSON format for future analysis.

> 🔁 Auto-refreshes every 2 minutes | 💾 All data saved to `disaster_monitor.json`

---

## 📦 Features

- 🌦 Weather hazard detection (storms, cyclones, floods)
- 🌐 Earthquake severity mapping (normal/moderate/rare)
- 🌋 Volcanic eruption monitoring (NASA EONET)
- 🎨 Terminal output with clean colored boxes using Colorama
- 💾 JSON logging of every event
- ⏰ Auto-refresh every 120 seconds (2 minutes)

---

## 🛰 APIs Used

| API | Description |
|-----|-------------|
| [🌤 WeatherAPI](https://www.weatherapi.com/) | Real-time weather data for selected cities |
| [🌍 USGS Earthquake Feed](https://earthquake.usgs.gov/earthquakes/feed/) | Global hourly earthquake updates |
| [🌋 NASA EONET](https://eonet.gsfc.nasa.gov/docs/v3) | Open volcano eruption event tracking |

---

## 🧠 Event Detection Logic

### 🌦 Weather

Rare weather is detected using keywords like:

- `storm`
- `thunder`
- `flood`
- `cyclone`
- `hurricane`

These are flagged as:

```json
"Rare Weather Event": "Yes"
````

Along with an explanation and a red 🔴 mark in the output.

---

### 🌐 Earthquakes

| Magnitude | Severity | Rare? |
| --------- | -------- | ----- |
| < 4.0     | Normal   | ❌     |
| 4.0–6.9   | Moderate | ❌     |
| ≥ 7.0     | Rare     | ✅     |

Major earthquakes are highlighted with 🔴 and explanation in the log.

---

### 🌋 Volcanic Eruptions

* All **active** volcano eruptions fetched from NASA EONET are flagged as **Rare**
* Displayed with red 🔴 marker and explanation

---

## 📁 Output Example

```json
{
    "Event Type": "Weather Update",
    "City": "Lahore",
    "Weather Condition": "Thunderstorm",
    "Rare Weather Event": "Yes",
    "Hazard Reason": "Hazard: Thunder detected",
    "Hazard Detail": "Severe thunderstorms may include lightning...",
    "Explanation": "Thunder detected in weather report..."
}
```

---

## 🚀 How to Run

### 🔗 [Click here to view the project online (preview output)](https://drive.google.com/drive/folders/1-1djffc1ZInWSucx6Pnc-ntlTprmV7Uo?usp=sharing)

### 📥 [Click here to download the full project as ZIP](https://drive.google.com/drive/folders/1-1djffc1ZInWSucx6Pnc-ntlTprmV7Uo?usp=sharing)

### 🛠 Manual Setup

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/Global-Disaster-Monitoring.git
   cd Global-Disaster-Monitoring
   ```

2. **Install dependencies:**

   ```bash
   pip install requests colorama
   ```

3. **Add your API key** in the `WEATHER_API_KEY` variable at the top of the script.

4. **Run the script:**

   ```bash
   python disaster_monitor.py
   ```

## 📸 Real-Time Running Video On Terminal

   
## 📸 Real-Time Screenshot Samples

<img width="692" alt="image" src="https://github.com/user-attachments/assets/179ccfbf-361a-422a-a343-9f079d64c0ad" />


<img width="904" alt="image" src="https://github.com/user-attachments/assets/fd782447-448c-4d61-a43e-2fa36e0c51cc" />

<img width="878" alt="image" src="https://github.com/user-attachments/assets/375c9137-0e7c-4abd-9f21-4b18bb51bef1" />

> 📁 These screenshots are captured from actual system output and highlight rare, moderate or hazardous events in real-time.

---

## 💡 Future Ideas

* 📩 SMS/Email alerts when rare events are detected
* 📊 Graphical visualizations with charts (e.g., using Matplotlib or Streamlit)
* 🧠 Historical trend analysis using databases (SQLite or MongoDB)
* 🌐 Web dashboard version for disaster command centers

---

## 📜 License

This project is open-source under the **MIT License**.
Feel free to fork, use, improve, and share it!

---

## 👤 Author

Built with ❤️ by **Awais Ali**

* 🔗 GitHub: [@Muhammad Bilal Ali Saif](https://github.com/bilalali6)
* 💼 LinkedIn: [@Muhammad Bilal Ali Saif](https://www.linkedin.com/in/muhammad-bilal-ali-saif)

---

## 🔖 Tags

`#Python` `#WeatherAPI` `#USGS` `#NASA-EONET` `#Disaster-Monitoring` `#Automation` `#OpenSource` `#ClimateTech`





