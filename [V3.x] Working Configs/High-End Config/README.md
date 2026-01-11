# High-End Config for Wuthering Waves (v3.x)

Optimized high-end configuration for **Wuthering Waves v3.x**, focused on visual quality while maintaining stability and balance.

---

## Contents

This repository includes **3 configuration files**:

- **2 DeviceProfiles** (Includes Mid-end DeviceProfiles)  
  - MediaTek
  - Snapdragon
- **1 Engine.ini**
  - Shared across all supported devices

---

## Design Goals

- High visual fidelity  
- Performance-balanced settings  
- Majority of values set near maximum where safe  
- Selective limits applied to prevent instability  

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

Lower the value further if needed. There's a guide within the DeviceProfiles.ini for that

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
- Do not blindly mix configs from other game versions(well ofc unless you know what you're doing xD)  
- Use with caution on non-flagship devices (So far no overheating issues but use a phone cooler if you can)  

---

## Updates

This repository is actively maintained and subject to change based on:

- Game updates  
- Engine behavior changes  
- Community-reported issues  


---
