# 🕰️ HistoricOverlay – AR Time Travel Through NYC

HistoricOverlay is a mobile AR app built with **Expo** and **Moondream**, designed to let users explore the past by simply pointing their phone at a building. With lightweight on-device inference and NYC historical image matching, the app overlays 1940s photos on top of live camera views in real time.

---

## 🚀 Getting Started

### 📦 Install dependencies

```bash
npm install
```

### ▶️ Start the development server

```bash
npx expo start
```

You’ll see options to:
- Open the app in **Expo Go** (for quick testing)
- Launch an **Android emulator** or **iOS simulator**
- Use a **development build** with native AR support

> **Note**: For AR features like camera + image overlay, use a physical device or development build with ARCore/ARKit enabled.

---

## 🛠️ Project Structure

- `/app`: Main application code (camera, UI, screens)
- `/assets`: Icons, images, and sample data
- `/lib`: Utility functions for geolocation, embedding, matching
- `/models`: Moondream embedding logic (ONNX/TFLite)
- `/data`: Historic image metadata + SQLite DB setup

---

## 📍 Features

- Camera preview using Expo Camera
- GPS + compass-based location filtering
- Moondream image embedding (on-device inference)
- Vector similarity matching to 1940s images
- AR overlay of matched photo with transparency slider
- Simple tap-to-trigger interaction for performance

---

## 🧰 Technologies Used

| Purpose               | Tool / Library                            |
|-----------------------|-------------------------------------------|
| Mobile Framework      | Expo (React Native)                       |
| Vision Model          | Moondream (converted to ONNX)             |
| Embedding Matching    | Cosine similarity (JS)                    |
| Location & Compass    | Expo Location, Expo Sensors               |
| UI & Navigation       | Expo Router, React Native components      |
| AR & Camera           | Expo Camera (ARCore support WIP)          |
| Data Storage          | SQLite (1940s NYC image dataset)          |
| OCR                   | Google Cloud Vision API                   |

---

## 🗺️ Data Sources

- [1940s.nyc](https://1940s.nyc)
- [80s.nyc](https://80s.nyc)
- [NYC ArcGIS Land Use](https://experience.arcgis.com/experience/d826b115c87841d491c2b41fcb175305)

---

## 🔐 API Keys & Environment Variables

Create a `.env` file in your project root:

```env
GOOGLE_VISION_API_KEY=your_key_here
MOONDREAM_API_KEY=your_key_here (if using server fallback)
```

---

## ♻️ Reset Project

To reset and start from a clean slate:

```bash
npm run reset-project
```

This will move starter code to `/app-example` and create a fresh `/app` directory.

---

## 📚 Learn More

- [📖 Expo Documentation](https://docs.expo.dev)
- [🧠 Moondream on GitHub](https://github.com/ashkamath/moondream)
- [📷 Google Cloud Vision Docs](https://cloud.google.com/vision)

---

## 🤝 Contributing

We welcome contributions! To contribute:
1. Fork the repo
2. Create a feature branch
3. Submit a pull request with your feature or fix

---
