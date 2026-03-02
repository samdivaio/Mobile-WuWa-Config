# Performance Config / Config_1
Last Updated: March 3, 2026  

## Table of Contents
1. [Overview](#a)  
2. [Important Notes](#b)  
3. [CVars You May Consider Tweaking](#c)   
      3.a. [DeviceProfiles CVars](#d)   
      3.b. [Engine.ini CVars](#e)   
4. [Final Notes](#f)   
  
---

## Overview

<a id="a"></a>
This is the README file for Performance Config/Config_1

First things first, this is the overview of the config as I have designed it:  

- **Config_1** is designed to be a high quality for the characters while keeping shadows, foliage and reflections minimal or zero. We're boosting detail and visuals while sacrificing three of the heaviest graphics load.(Staring at you, Lahai-roi)  

- **DeviceProfiles.ini** contains all the high-quality cvars that will affect the game. However, I intentionally did not push the values to their maximum limits. Additionally, I have set the `sg.ShadowQuality` and `sg.FoliageQuality` to zero.

- **Engine.ini** on the other hand contains all the optimizations for this config. You can basically mix and match your preferred `DeviceProfiles.ini` with this config's engine.

---

## Important Notes

<a id="b"></a>
Some information worth noting:

1. This is a config for testing and I'm still waiting for feedback.  
2. This config is tested using **Poco X6 Pro (MD8300/Mali G615)**. Therefore I do not have data yet how this performs for the actual flagship devices.  
3. `r.BloomQuality=0`, for some reasons, does not truly remove/disable the bloom in this config. *This could most possibly be a skill issue on my end though*  
4. The reason I included the `r.Color` lines was due to the washout and extreme light that Kuro is giving me when testing the config, which also made me put a low value of `r.TonemapperGamma=1.8` (2.2 is the default)

## CVars You May Consider Tweaking
<a id="c"></a>
Yapping aside, here are some of the CVars you may consider tweaking on your end.

---



# DeviceProfiles CVars
<a id="d"></a>

### 1. DeviceScore

- Set this to an insanely high value and you're never getting that overloaded **"Current Setup Load"** ever again. It will always show up **"Smooth" / GREEN** in color.
- Please don't be a fool and assume that a "smooth/green" visual indicator is also the corresponding indicator of the actual device performance/load.  
- We use the `DeviceScore` here to bypass the annoying overloaded notification in-game as well as to detect if your `DeviceProfiles.ini` is correctly working.

**Sample code:**
```ini
DeviceScore=6969
```

As per Zakro, a value of **150000** will remove the bars entirely (insert lauf emoji here)

---

### 2. CVars=r.MobileContentScaleFactor=1.3

- The usual default is actually **1.5**, you can change it to:
  - **1.0** (better perf, poorer quality)
  - **2.0** (better quality, worse perf)
- Low/Mid phone users may prefer **1.0**, while flagships could handle **2.0** without breaking a sweat

---

### 3. CVars=r.ViewDistanceScale=5

- This is actually pretty high, you might consider lowering this value to **2.0**

---

### 4. CVars=r.DetailMode=2  
- I lowered this to 2 so mid-end devices can handle this better
- This is the mid-level detailmode, consider lowering to **1** if low-end  
- If using flagship devices, feel free to raise it up to ***3***

---

### 5. Scalability Groups

- The scalability groups (`sg.*`) are limited to max value of **4**, except the `PostProcessQuality` which goes to **6**.

A fully maxed out value of sg. groups would be something like this:

```ini
CVars=sg.ViewDistanceQuality=4  
CVars=sg.AntiAliasingQuality=4  
CVars=sg.ShadowQuality=4  
CVars=sg.PostProcessQuality=6  
CVars=sg.TextureQuality=4  
CVars=sg.EffectsQuality=4  
CVars=sg.FoliageQuality=4  
CVars=sg.ShadingQuality=4
```

---

### 6. r.imp.*

- You can set this to **0.00** for auto scaling  
```
CVars=r.imp.SSMbScaleLod0=0.00
CVars=r.imp.SSMbScaleLod1=0.00
CVars=r.imp.Lod0Screensize=0.00
CVars=r.imp.Lod1Screensize=0.00
```

---
# Engine.ini CVars
<a id="e"></a>

### 1. r.TonemapperGamma

- This one controls the overall gamma of your game. Consider lowering this value only after tuning your visuals using the in-game settings.  
  (Brightness, Saturation, Contrast, Shadows, Bloom, Grayscale)

---

### 2. r.FidelityFX.FSR.QualityMode=1

- high-end devices may opt to use a value of **0** for this cvar for the best quality

---

### 3. r.TemporalAA.HistoryScreenPercentage=85

- You may consider increasing this to **100**

---

### 4. r.TemporalAAFilterSize=0.75

- You may consider increasing this to **1.0**

---

### 5. r.VSync=1

- For some reasons, this is a hit or miss cvar. Consider trying setting the value to **0**, whichever works better for your device.

---

### 6. Frame Generation Users (Additional Tweaks)

For those with Frame Generation, you may want to additionally consider:

- `FrameRateLock=60` change to **120**  
- `RHI.TargetRefreshRate=60` change to **120**  
- `bEnableDynamicMaxFPS=False`

# Final Notes
<a id="f"></a>

1. Make sure to recompile your shaders before using the config.  
    Tutorial: https://youtu.be/uxio8GI85PY
2. Suppose you are using Mediatek or Snapdragon DeviceProfiles.ini and you're experiencing some sort of flickering/blinking problem, ***AND*** you **DO NOT HAVE** a flagship device, switch to the Android's DeviceProfiles.ini