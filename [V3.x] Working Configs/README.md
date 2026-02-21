# Mobile Config Selector Guide

This readme will be updated in the near future due to the refactoring being done this week.

This guide helps you choose the **correct config preset** based on your phone's **CPU/GPU tier**.
Using the right preset avoids crashes, overheating, and severe frame drops.

---

## Config Presets Explained

- **High-End Config**
  - For flagship and near-flagship devices
  - Maximizes visuals and effects

- **Stable Config**
  - For mid-range and upper low-end devices
  - Balanced visuals and performance

- **Potato Config**
  - For low-end devices
  - Prioritizes compatibility and FPS over visuals

---

## Device Compatibility Table

| Phone (Examples) | CPU / GPU | Config to Use |
|------------------|-----------|---------------|
| Galaxy S24 Ultra | Snapdragon 8 Gen 3 / Adreno 750 | High-End Config |
| Galaxy S23 / S23+ | Snapdragon 8 Gen 2 / Adreno 740 | High-End Config |
| Galaxy S24 (Exynos) | Exynos 2400 / Mali-G715 | High-End Config |
| Xiaomi 14 | Snapdragon 8 Gen 3 / Adreno 750 | High-End Config |
| OnePlus 12 | Snapdragon 8 Gen 3 / Adreno 750 | High-End Config |
| Vivo X100 | Dimensity 9300 / Mali-G720 | High-End Config |
| Poco X6 Pro | Dimensity 8300 / Mali-G615 | High-End Config |
| Galaxy A54 | Exynos 1380 / Mali-G68 | Stable Config |
| Galaxy A34 | Dimensity 1080 / Mali-G68 | Stable Config |
| Redmi Note 12 Pro | Dimensity 1080 / Mali-G68 | Stable Config |
| Poco X5 Pro | Snapdragon 778G / Adreno 642L | Stable Config |
| Infinix Zero 30 | Dimensity 8020 / Mali-G77 | Stable Config |
| Tecno Camon 20 Pro | Dimensity 8050 / Mali-G77 | Stable Config |
| Redmi 13C | Helio G85 / Mali-G52 | Potato Config |
| Galaxy A05 | Helio G85 / Mali-G52 | Potato Config |
| Realme C55 | Helio G88 / Mali-G52 | Potato Config |
| Infinix Smart 8 | Unisoc T606 / Mali-G57 MC1 | Potato Config |
| Tecno Spark Go | Unisoc T606 / Mali-G57 MC1 | Potato Config |

---

## Quick Rule of Thumb

- **Adreno 7xx / Mali G7xx** → High-End Config
- **Adreno 6xx / Mali G68–G77** → Stable Config
- **Adreno 5xx / Mali G52–G57 / Mali G31** → Potato Config

---

## Notes

- If you experience overheating or instability, downgrade one tier.
- Shader recompilation after switching configs is recommended.

---

*Configs are continuously refined. Always use the latest version.*
