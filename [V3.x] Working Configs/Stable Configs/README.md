## Stable Configuration Overview

This stable configuration closely follows the game’s default settings to minimize bugs and crashes while still delivering strong visual quality.

If you encounter any issues, crashes, or settings that do not work as expected, please **open an issue**. You are also welcome to join the **Discord** to help improve the config or report problems.  

Here are two CVars that may help your DIY troubleshooting:  
Suppose your game is blinking like crazy even after 3 minutes in-game, add this under [SystemSettings]  
r.HZBOcclusion=1  

If you're experiencing weird black graphics, add this under [SystemSettings]  
r.DefaultBackBufferPixelFormat=0  

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
