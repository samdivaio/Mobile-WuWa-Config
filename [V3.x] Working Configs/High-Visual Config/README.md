# Override Announcement  
> If you're having trouble with the frame generation of the High-Visual Config, please use the Experimental Config in the mean time.  


# High-End Config for Wuthering Waves (v3.1)


---

## Contents

This repository includes **4 configuration files**:

- **3 DeviceProfiles** (Includes Mid-end DeviceProfiles)  
  - Android (Generic)  
  - MediaTek
  - Snapdragon
- **1 Engine.ini**
  - Shared across all supported devices

- **Also included is 1 folder dedicated for an experimental config**
---

## Compatibility

- **Game Version**: Wuthering Waves 3.x  
- **Target Devices**: High-end Android devices  
- **Supported Chipsets**: MediaTek and Snapdragon  

Configs may be updated if future game patches introduce instability or rendering issues.

---

## Performance Tuning (Quick Fix)

If you experience lag or frame drops, adjust the following value:

```
r.MobileContentScaleFactor=1.0
```

In case of weird black/white flickering: switch from 0 to 1 or 1 to 0 depending what works for your device  
```
r.HZBOcclusion=1
```

---

## Device Profile Not Applying?

If your `DeviceProfile` is not being read correctly, open an issue and include:
- CPU or chipset
- GPU

If you are unsure, please send your **`Client.log`** instead (Discord preferred).

### Log File Location
```yaml   
/Internal shared storage/Android/data/com.kurogame.wutheringwaves.global/files/UE4Game/Client/Client/Saved/Logs
```


## Notes

- Shader recompilation after updates is normal  

---

## Updates

This repository is actively maintained and subject to change based on:

- Game updates  
- Engine behavior changes  
- Community-reported issues  


---
