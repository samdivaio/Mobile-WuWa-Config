## Stable Configuration Overview

This stable configuration closely follows the game’s default settings to minimize bugs and crashes while still delivering stable visual quality.

If you encounter any issues, crashes, or settings that do not work as expected, please **open an issue**. You are also welcome to join the **Discord** to help improve the config or report problems.  

## Notable CVars  
1. r.MobileContentScaleFactor  
- This is your base render. Game default is 1.5 (1080p)  
> 1.0 = 720p, great performance  
> 1.5 = 1080p, default  
> 2.0 = 1440p, crisp visuals, worse perf  

2. r.KuroFI.Enable  
- This is Kuro's frame interpolation (frame gen)   
- Recently launched this Version 3.2 so it could be bad or good for some devices  
> 0 = disable  
> 1 = enable + visual frame gen toggle in-game  

Here are two CVars that may help your DIY troubleshooting:  
Suppose your game is blinking like crazy even after 3 minutes in-game, add this under [SystemSettings]  
```r.HZBOcclusion=1  ```  

If you're experiencing weird black graphics, add these under [SystemSettings]    
``` r.DefaultBackBufferPixelFormat=0  ```  
``` r.SceneColorFormat=4 ```

OR

Delete your DeviceProfiles.ini
---

## Device Profile Not Applying?

If your `DeviceProfile` is not being read correctly, open an issue and include:
- CPU or chipset
- GPU

If you are unsure, please send your **`Client.log`** instead (Discord preferred).


DIY For DeviceProfiles:  
1. Go to your Client.Log and open it (See Log File Location)  
2. Ctrl+F or use Search, search for "selected device profile"  
3. Copy the device profile name there, e.g. Android_Mali_G61x
4. Change the name of your main deviceprofile to what you found in #3  
e.g.  
> From : [Android_StableConfig DeviceProfile]  
> To: [Android_Mali_G61x DeviceProfile]  

### Log File Location
```yaml   
/Internal shared storage/Android/data/com.kurogame.wutheringwaves.global/files/UE4Game/Client/Client/Saved/Logs
```
