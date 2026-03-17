I'll format this properly in the next update.  

Here's what you need to know related to the Z_Experimental Config:  
1. Personally tested **ONLY** on Poco X6 Pro. Therefore create an issue or let me know through Discord if you encounter problems.  
2. There was a weird lighting last time which exposed rectangular textures with fixed light, as well as a lod distance issue that will make a character pass through terrains/appear submerged. This is now fixed, especially in the Lahai-Roi snowy region.  


## Notable CVars:  

1. r.MobileContentScaleFactor  
    > Contrary to the value(1.5) in the file, I mostly test play using 1.3 or 1.35  
    > Default is 1.5, use 1.75 or 2.0 if you have a larger resolution/bigger screen(like a tablet or external monitor)  

2. RHI-related/r.Vulkan.*  
    > Most of the crashing problems root to renderer-related CVar. The values in both .ini files uses the game's default. If your game autocrashes, try removing **ALL** r.Vulkan lines ***EXCEPT*** ```r.Android.DisableVulkanSupport=0```

3. r.FidelityFX.FSR3.QualityMode  
    > Set to 1 in the config, if you need more performance, set higher (2,3 or 4).  
    > Set to 0 for Maximum visual quality  



^ Only these for now, see you on the next update and good luck on your Lingyang pulls!  