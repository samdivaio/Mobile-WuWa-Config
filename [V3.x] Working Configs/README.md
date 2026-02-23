# Mobile Config Selector Guide for V3.x

This guide helps you choose the **correct config preset** based on your phone's **CPU/GPU tier**.
Using the right preset avoids crashes, overheating, and severe frame drops.

---

## Config Presets Explained

- **High-Visual Config**
  - Usually for high-end/flagship devices
  - Maximizes visuals and effects
  - Great to use when doing the Main Story Quest
  - Mid-end devices can also use this, but using the corresponding Mid-End DeviceProfiles.ini

- **Stable Configs**
  - For all devices
  - Balanced visuals and performance
  - Reflections are introduced here

- **Performance Configs**
  - For people who favor FPS over visual fidelity
  - For low-end devices
  - Prioritizes performance, expect lower visuals
  - Shadow, Reflections, and Grass are usually disabled here

---

## Device Compatibility Table

| Phone (Examples) | CPU / GPU | Config to Use |
|------------------|-----------|---------------|
| Galaxy S24 Ultra | Snapdragon 8 Gen 3 / Adreno 750 | Stable Config – A / (High Visuals) |
| Xiaomi 14 | Snapdragon 8 Gen 3 / Adreno 750 | Stable Config – A / (High Visuals) |
| OnePlus 12 | Snapdragon 8 Gen 3 / Adreno 750 | Stable Config – A / (High Visuals) |
| Vivo X100 | Dimensity 9300 / Mali-G720 | Stable Config – A / (High Visuals) |
| Galaxy S23 / S23+ | Snapdragon 8 Gen 2 / Adreno 740 | Stable Config – B |
| Galaxy S24 (Exynos) | Exynos 2400 / Mali-G715 | Stable Config – B |
| Poco X6 Pro | Dimensity 8300 / Mali-G615 | Stable Config – B |
| Galaxy A54 | Exynos 1380 / Mali-G68 | Stable Config – C |
| Galaxy A34 | Dimensity 1080 / Mali-G68 | Stable Config – C |
| Redmi Note 12 Pro | Dimensity 1080 / Mali-G68 | Stable Config – C |
| Poco X5 Pro | Snapdragon 778G / Adreno 642L | Stable Config – C |
| Infinix Zero 30 | Dimensity 8020 / Mali-G77 | Stable Config – C |
| Tecno Camon 20 Pro | Dimensity 8050 / Mali-G77 | Stable Config – C |
| Redmi 13C | Helio G85 / Mali-G52 | Potato Config |
| Galaxy A05 | Helio G85 / Mali-G52 | Potato Config |
| Realme C55 | Helio G88 / Mali-G52 | Potato Config |
| Infinix Smart 8 | Unisoc T606 / Mali-G57 MC1 | Potato Config |
| Tecno Spark Go | Unisoc T606 / Mali-G57 MC1 | Potato Config |

---

## Stable Config Selector

### Config A – High Visuals (Stable)
**Minimum recommended hardware:**
- Snapdragon **8 Gen 3**
- Dimensity **9000 series and above**

Target: maximum visuals while maintaining frame stability.

### Config B – Balanced (Stable)
**Up to:**
- Dimensity **8400**
- Snapdragon **7+ Gen 3** (equivalent class)

Target: strong visuals with controlled effects and consistent performance.

### Config C – Low (Stable)
**Lower-end devices below Config B minimum**

Target: playability and consistency over visual fidelity.

---

## Quick Rule of Thumb

- **Snapdragon 8 Gen 3 / Dimensity 9000+** → Stable Config A  
- **Snapdragon 8 Gen 2 → Snapdragon 7+ Gen 3 / Dimensity 6000–8000** → Stable Config B  
- **Snapdragon 7xx (non-Plus) / Mali-G68–G77** → Stable Config C  
- **Adreno 5xx / Mali-G52–G57 / Mali-G31** → Potato Config
---

## Notes

- If you experience overheating or instability, downgrade one tier.
- Shader recompilation after switching configs is recommended.

---

*Configs are continuously refined. Always use the latest version.*

Last Updated on: 2026-2-23