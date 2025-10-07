# 🎥 YouTube Scrollable Fullscreen (Fake Fullscreen Extension)

This Chrome extension replaces YouTube’s native fullscreen mode with a **custom "fake fullscreen"** that keeps the video large and immersive **while allowing you to scroll** to comments, descriptions, and other elements — all without exiting fullscreen.

---

## 🚀 Features

- ✅ Custom fullscreen button that replaces YouTube’s original one  
- ✅ Scroll through comments and related videos while in "fullscreen"  
- ✅ Automatically reinjects the custom button when YouTube updates the player UI  
- ✅ Handles `Escape`, `F11`, and `fullscreenchange` events gracefully  
- ✅ Toggle the feature ON/OFF from the extension popup  
- ✅ Saves your ON/OFF preference across page reloads and sessions  

---

## 🧠 How It Works

1. When you open a YouTube video, `content.js` injects a **custom fullscreen button** next to the theater mode button.
2. Clicking this button triggers **fake fullscreen mode**, which:
   - Hides YouTube’s header, sidebar, and footer.
   - Expands the video player to fill the viewport.
   - Keeps the rest of the page scrollable.
3. The original YouTube fullscreen button is hidden while the extension is active.
4. You can enable or disable the extension anytime from the popup switch.
5. Your preference is stored via `chrome.storage.sync` and persists across refreshes.

---

## 🧩 Files Overview

| File | Purpose |
|------|----------|
| `manifest.json` | Chrome extension manifest (declares scripts, popup, permissions). |
| `content.js` | Main logic injected into YouTube pages — handles button creation and fake fullscreen behavior. |
| `styles.css` | Applies layout and style adjustments during fake fullscreen. |
| `popup.html` | The popup UI with a simple enable/disable toggle. |
| `popup.js` | Handles user interactions in the popup and communicates state to the content script. |

---

## ⚙️ Installation

1. Download or clone this repository.
2. Open **Chrome** and go to `chrome://extensions/`.
3. Turn on **Developer mode** (top right).
4. Click **Load unpacked** and select this project folder.
5. Go to any YouTube video — you’ll see the new fullscreen button!
6. Use the extension popup to enable or disable the feature.

---

## 🛠️ Tech Details

- **Manifest Version:** 3  
- **Languages:** JavaScript, HTML, CSS  
- **APIs used:**  
  - `chrome.scripting`  
  - `chrome.runtime`  
  - `chrome.storage.sync`  

---

## 🧾 License

This project is open-source and free to use for personal customization of YouTube’s interface.

---

## 💡 Credits

Created with ❤️ to make YouTube fullscreen more practical for viewers who want to keep scrolling!

