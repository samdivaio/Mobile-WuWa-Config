# ❓ WuWa Config – Frequently Asked Questions (FAQ)

Welcome to the **Ultimate FAQ Guide** for customizing your `Engine.ini` and `DeviceProfiles.ini`!

Whether you want **ultra-sharp visuals**, **maximum performance**, or a **balanced blend**, this guide gives you the power to tweak the config to suit your device and taste.


Please note that as of Feb. 22, 2026, I am refactoring this section to ensure accurate and updated codes to assist you. This will be completed by the end of this week.  (See you in March)
---

## 🎮 I want better graphics. How can I make the game look sharper?

### ✅ Solution:

* **Increase resolution scale**:

  ```
  Cvars=r.MobileContentScaleFactor=2.0
  ```

* **Improve texture quality**:

  ```
  r.Streaming.MipBias=-1   ; -1 = sharper, 0 = default, 1 = blurrier
  ```

* **Use higher density foliage and grass**:

  ```
  foliage.DensityScale=2.0  ; Default = 1.0, can go up to 4.0+
  ```

> 🔥 Warning: High values will impact performance on mid-range devices.

---

## 🚀 I want better performance. How can I make the game run faster?

### ✅ Solution:

* **Lower native render resolution**:

  ```
  Cvars=r.MobileContentScaleFactor=1.0
  ```

* **Reduce foliage and mesh density**:

  ```
  grass.DensityScale=0.5
  foliage.DensityScale=0.5
  ;or you can disable them completely
  foliage.cullAll=1
  ```

* **Disable expensive effects**:

  ```
  r.AmbientOcclusionLevels=0
  r.BloomQuality=0
  r.SSR.Quality=0
  ```

* **Force lower LODs** (simpler models):

  ```
  r.ViewDistanceScale=1
  r.SkeletalMeshLODBias=1
  ```

---

## 🌆 I don’t care about shadows. How do I disable them?

### ✅ Solution:

* **Disable dynamic and static shadows**:

  ```
  r.ShadowQuality=0
  r.Shadow.CSM.MaxCascades=0
  r.Shadow.RadiusThreshold=0.1
  r.Shadow.MaxResolution=16
  r.Mobile.Shadow.CSMShaderCullingMethod=0
  ```

> This will greatly improve performance on lower-end devices.

---

## 🧊 I want polygonal, low-poly look. Can I do that?

### ✅ Solution:

* **Lower resolution + no AA + high LOD bias**:

  ```
  r.ScreenPercentage=60
  r.TemporalAA.Upsampling=0
  r.MaterialQualityLevel=0
  r.SkeletalMeshLODBias=3
  ```

* **Disable post-processing**:

  ```
  r.Tonemapper.GrainQuantization=0
  r.SceneColorFringeQuality=0
  r.BloomQuality=0
  r.LensFlareQuality=0
  ```

---

## 🦾 I want MAX settings. Ultra-high. No limits. What to tweak?

### ✅ Solution:

* **Go full blast on everything** (WARNING: for flagship phones only):

  ```
  r.MobileContentScaleFactor=2.0
  r.ScreenPercentage=150
  r.Mobile.TonemapperFilm=1
  r.TemporalAA.Upsampling=1
  r.SSR.Quality=4
  r.AmbientOcclusionLevels=4
  r.BloomQuality=5
  r.LensFlareQuality=3
  r.MaterialQualityLevel=2
  foliage.DensityScale=4.0
  grass.DensityScale=4.0
  ```

* **Unlock full draw distances**:

  ```
  r.ViewDistanceScale=6
  r.SkeletalMeshLODRadiusScale=0.25
  ```

* **Enable Niagara GPU FX** (if supported):

  ```
  fx.NiagaraAllowGPUParticles=1
  ```

> ⚠️ Use at your own risk. Not all devices can handle this without overheating or crashing.

---

## 🚩 My game crashes or doesn’t load after changes. What now?

### ✅ Solution:

1. Delete these files from:

   ```
   Android/data/com.kurogame.wutheringwaves.global/files/UE4Game/Client/Client/Saved/Config/Android/
   ```

   * `Engine.ini`
   * `DeviceProfiles.ini`

2. Restart WuWa – the game will regenerate safe default configs.

---

## 💡 Bonus: How do I test changes quickly?

### ✅ Tip:

* Modify `Engine.ini` on PC
* Save and push via USB
* Force-stop the game on your phone and relaunch

Use tools like **ADB logcat** to debug crashes or GPU monitors (e.g., Adreno Profiler / PerfDog / Xiaomi Performance Monitor).

---

## 🤝 Need More Help?

Join our Discord community to ask, share configs, and get real-time support:  
[![Discord](https://img.shields.io/badge/Join-Discord-7289DA?logo=discord&logoColor=white)](https://discord.gg/renjxYBEZM)

---

*Made with ⚙️(ChatGPT) by Arglax – Tweak wisely and game smoothly!*
