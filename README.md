# Railway Chaiwala (रेलवे चाय वाला)

An Android APK and WebAssembly adaptation of **Railway Chai Wala** by [drcocktailgames](https://drcocktailgames.itch.io/railway-chai-wala).

- 📱 **Download Android APK (Direct Link):** [release/RailwayChaiWala-v1.0.apk](https://github.com/payalktr80-web/Railway-Chaiwala/raw/main/release/RailwayChaiWala-v1.0.apk)
- 🚀 **GitHub Releases (APK Artifact):** [Releases](https://github.com/payalktr80-web/Railway-Chaiwala/releases)
- 🌐 **Play Online on GitHub Pages:** [https://payalktr80-web.github.io/Railway-Chaiwala/](https://payalktr80-web.github.io/Railway-Chaiwala/)

---

## 🕹️ Mobile Touch Controls (Android APK & Touchscreens)

The Android APK is specifically tuned for mobile play with responsive on-screen virtual arcade controls:

| Control | Type | Function |
|---|---|---|
| 🕹️ **Virtual Analog Joystick** | Touch (Left) | Smoothly moves Chaiwala Ramu horizontally across the refreshment stall and platform to approach interactive stations. |
| 🤝 **SPACE BAR Button** | Action (Right) | **Interact / Action**: Lights burner, pours brewed tea, starts coffee machine, cuts noodles, packs trays, talks to customers, or advances dialogue. |
| ❌ **Q Button** | Cancel (Right) | **Drop / Cancel / Back**: Drops the item in hand, turns off the stove burner, clears packaging tray, or cancels/skips dialogues. |

---

## 📖 Story & Premise
Step into the shoes of **Ramu**, a hardworking tea vendor (*chaiwala*) running the refreshment stall at **Fakripur Junction** (*फ़कीरपुर जंक्शन*). 

Brew authentic Indian Kadak Chai, serve crispy Samosas, Vadapavs, chilled Kokila Kola, and 2-minute Fuggi noodles to impatient travelers before their express trains depart. But as the clock ticks past midnight and cold fog rolls across Platform 2, strange paranormal events and long-buried station secrets begin to unfold.

---

## 🎮 Key Features
- **Mobile Optimized Android App**: Native fullscreen immersive mode with hardware acceleration and 0 external dependencies for instant load times.
- **Authentic Chai Brewing**: Control gas burner flames, boil water and milk, add tea leaves (*chai patti*), crushed ginger (*adrak*), cardamom (*elaichi*), and sugar, and pour into traditional clay *kulhads*.
- **Railway Coffee Machine**: Insert cups, engage steam valves, and brew hot railway coffee.
- **Fuggi 2-Minute Noodles**: Slice open noodle packets with the station knife and cook on the burner.
- **Order Assembly & Billing**: Assemble trays for customers (Kashif, Preet, Saumya) and print itemized thermal receipts.
- **Full Psychological Thriller Story**: Experience all 6 shifts from morning dawn to the midnight confrontation on Track 2 with multiple branching endings.
- **Bilingual Interface**: Full English and Hindi subtitles and dialogues.
- **Zero-Dependency Web Audio**: Dynamic synthesizers for stove flames, boiling liquids, pouring streams, train whistles, bells, and horror drone music.

---

## ⌨️ Desktop Keyboard Controls
| Key | Action |
|---|---|
| **A / D** or **◀ / ▶** | Move Chaiwala left / right across stall |
| **Space** | Primary Interact / Action / Advance Dialogue |
| **Q** | Drop Held Item / Turn Off Burner / Cancel |
| **B** | Toggle Gas Burner on/off |
| **P** | Pour Hot Chai into Clay Kulhad |
| **C** | Brew Coffee in Coffee Machine |
| **N** | Place & Cut Fuggi Noodle Packet |
| **S** | Serve Assembled Tray to Customer |
| **Esc** | Skip Dialogue Line |

---

## 🛠️ Building the Android APK

### Locally with Gradle (PocketDev Environment)
```bash
timeout 15m gradle -Dorg.gradle.jvmargs= --no-daemon --max-workers=2 \
  --init-script /root/.gradle/init.d/pocketdev-android.gradle \
  -Pandroid.aapt2FromMavenOverride=/root/android-sdk/build-tools/35.0.0/aapt2 \
  assembleDebug --console=plain --stacktrace
```

The compiled APK will be output to `app/build/outputs/apk/debug/app-debug.apk`.

### Automated via GitHub Actions
Every push to `main` automatically triggers `.github/workflows/android-apk.yml`, compiling the APK and publishing it as a GitHub Actions build artifact and GitHub Release.
