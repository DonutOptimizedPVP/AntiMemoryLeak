# 🛡️ AntiMemoryLeak (Minecraft 1.21.x)

![Minecraft Version](https://img.shields.io/badge/Minecraft-1.21.x-brightgreen.svg)
![Loader](https://img.shields.io/badge/Loader-Fabric-blue.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

**AntiMemoryLeak** is a high-performance, lightweight optimization mod for Minecraft Fabric 1.21.x. It serves as a modern successor to legacy memory leak fixes, specifically engineered to eliminate FPS drops, stuttering, and excessive RAM consumption during long play sessions.

Developed under the **DonutOptimizedPVP** organization, this mod focuses on core system efficiency for both Competitive PVP and General Survival.

---

## 🚀 Key Features

### 1. 🧠 Intelligent Memory Management
* **Forced Garbage Collection:** Smartly triggers `System.gc()` based on configurable thresholds (Player disconnect, World unload, or RAM usage > 90%).
* **Leak Stripper:** Actively nullifies references to unused objects that Java's GC often misses.

### 2. 🗺️ Chunk & Entity Optimization
* **Unused Chunk Purge:** Immediately unloads chunk data and lighting caches once they move out of render distance.
* **Dead Entity Cleanup:** Clears entity lists and prevents "ghost entities" from occupying memory.

### 3. 🖼️ Graphics & Shader Fixes
* **GPU Buffer Release:** Forces OpenGL to release vertex buffers and shader uniforms when switching worlds or reloading shaders.
* **Texture Atlas Defragmentation:** Frees up temporary RAM used during resource pack stitching.

### 4. ⚡ System & UI Optimization
* **DFU Stripper:** Discards the massive DataFixerUpper (DFU) cache after the game initializes, saving **200MB - 500MB** of RAM instantly.
* **GUI Screen Leak Fix:** Ensures previous screen references (Chests, Inventory, Menus) are cleared to prevent UI memory bloat.

### 5. 📊 Developer & Power User Tools
* **Live HUD:** Real-time RAM usage and GC statistics (Toggleable).
* **Debug Commands:** Use `/aml clean` for manual sweep or `/aml info` for heap analysis.

---

## 🛠️ Technical Details

* **Package ID:** `pvp.vnnhattruongneee.antimemoryleak`
* **Language:** Java 21
* **Compatibility:** Works seamlessly with **Sodium**, **Iris**, and other performance mods.
* **Environment:** Supported on both **Client** and **Server**.

---

## 📦 Installation

1.  Make sure you have **Fabric Loader** installed.
2.  Download the latest `.jar` from the [Releases](https://github.com/DonutOptimizedPVP/AntiMemoryLeak/releases) page.
3.  Place the file into your `.minecraft/mods` folder.
4.  Launch the game and look for `[AntiMemoryLeak] Initialized successfully!` in the console.

---

## 🤝 Contributing

Contributions are welcome! If you find a leak or have a suggestion:
1. Fork the Project.
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`).
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the Branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

---

## 📝 Credits & License

* **Developer:** VNNhatTruongneee
* **Organization:** DonutOptimizedPVP
* **License:** Distributed under the MIT License. See `LICENSE` for more information.

---
*Developed with ❤️ for the Minecraft PVP Community.*
