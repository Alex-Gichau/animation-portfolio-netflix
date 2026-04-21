# 🎬 Animation Portfolio: Netflix Edition

A cinematic, high-performance web application designed to showcase animation projects across multiple YouTube channels. This portfolio mimics the premium Netflix UI/UX, featuring persistent user history and real-time data integration.

---

## 🚀 Key Features

* **Multi-Channel Aggregation:** Automatically pulls and organizes content from different YouTube channels into a single interface.
* **Smart "Continue Watching":** Uses `localStorage` to cache user progress. If a viewer leaves and returns, your site remembers exactly where they stopped.
* **Dynamic Metadata:** Real-time fetching of **view counts** and **channel names** via the YouTube Data API v3.
* **Premium UX:**
    * Responsive horizontal sliders.
    * Hover-to-preview functionality.
    * Sleek Dark Mode aesthetic.

---

## 🛠️ Tech Stack

| Layer | Technology |
| :--- | :--- |
| **Frontend** | React.js / Next.js |
| **Styling** | Tailwind CSS |
| **Animations** | Framer Motion |
| **Data Fetching** | YouTube Data API v3 |
| **State/History** | Browser LocalStorage API |

---

## 📖 How It Works

### 1. User History (Persistence)
The site monitors the YouTube IFrame Player. When a user pauses or closes a video, the current timestamp is saved to the browser's cache:
```javascript
localStorage.setItem('watch_history', JSON.stringify({ videoId: 'XYZ', time: 120 }));
