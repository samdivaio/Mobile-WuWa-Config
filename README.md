
<h1 align="center">📢 Announcements 📢</h1>  

## February 12, 2026  
1. V2.8 Configs are temporarily placed in Old Configs until I find time updating them and integrating them into the V3.x Working Configs  
2. Some headers may be incomplete(no impact on actual config but rather for transparency). These will be reviewed and completed on a later date, along with some possible code optimizations.  
3. V3.1 DeviceProfiles will be constantly updated especially for those Devices whose DeviceProfiles' names have been changed.   
```  
;		==How to Obtain your DeviceProfile's Name==  
; 	1. ...\Internal shared storage\Android\data\com.kurogame.wutheringwaves.global\files\UE4Game\Client\Client\Saved\Logs  
;	2. Open Client.Log (usually around 1-15MB)  
;	3. Search "Selected Device Profile"  
;	4. It will show up something like "Selected Device Profile: Mali-G1x_Mid"  
;	5. Create an issue(if GitHub) or tag me(@Arglax) with the devprof name in discord in #config-help   
```
## Config Selector Guide for [ V3.x Configs](https://github.com/Arglax/Mobile-WuWa-Config/tree/main/%5BV3.x%5D%20Working%20Configs#readme)  
<div align="center">
  <img src="https://img.shields.io/badge/Update-February13-blue?style=for-the-badge&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/🎯_Target_Version-3.0-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Support-Vulkan_&_Non--Vulkan-orange?style=for-the-badge&logo=cog&logoColor=white" />
</div>
<h1 align="center">🎮 WuWa-Config: Mobile Configuration for Wuthering Waves</h1>

[![Stars](https://img.shields.io/github/stars/Arglax/WuWa-Config?style=social)](https://github.com/Arglax/WuWa-Config/stargazers) &nbsp;&nbsp;&nbsp;&nbsp; [![License](https://img.shields.io/badge/License-CustomizedMIT-lightgrey)](https://github.com/Arglax/WuWa-Config/blob/main/LICENSE) &nbsp;&nbsp;&nbsp;&nbsp; [![Discord](https://img.shields.io/badge/Discord-7289DA?logo=discord&logoColor=white)](https://discord.gg/renjxYBEZM)

**WuWa-Config** is a custom-built set of configuration files designed to **boost graphics, stability, and performance** in *Wuthering Waves* on Android devices.

Hopefully, this guide will help you unlock your device’s full visual and gameplay potential.  

## Disclaimer
These configurations are provided "as is", without warranty of any kind.
Use at your own risk.

I am not responsible for crashes, performance issues, data loss,
or any consequences arising from the use of these configs.

Donations are voluntary and do not constitute a purchase or service.

---

## 📖 Table of Contents
- [What’s Inside](#-whats-inside)
- [How to Install](#how-to-install)
- [File Location](#file-location)
- [Need Help?](#-need-help)
- [Credits](#-credits)
- [Tags](#-tags-for-seo-indexing)

---

## 📁 What’s Inside

- `Engine.ini` – Core rendering and graphics tweaks  
- `DeviceProfiles.ini` – Device-specific enhancements  

---
<a id="how-to-install"></a>
## 🛠️ How to Install (Beginner Friendly)
You can view video tutorial here: https://youtu.be/bB6C8hp_dFQ

### ✅ Requirements:
- A **Windows PC or laptop**
- A **Connecting Cable (USB,Lightning, or Type C)** 
- Your **Android device**

---

### 🔧 Step-by-Step Instructions:

1. **Connect** your Android device to your PC via USB.  
2. Select **"File Transfer" (MTP)** mode on your phone.  
3. Open **File Explorer** on your PC.  
4. Navigate to the following folder:

<details>
<summary>📂 File Location Path</summary>
<a id="file-location"></a>
To access or modify configuration files for *Wuthering Waves*, navigate to the following folder of your Android device:

```
Internal Storage/
└── Android/
    └── data/
        └── com.kurogame.wutheringwaves.global/
            └── files/
                └── UE4Game/
                    └── Client/
                        └── Client/
                            └── Saved/
                                └── Config/
                                    └── Android/
```

</details>

5. Paste the provided:
   - `Engine.ini`
   - `DeviceProfiles.ini`

The complete path to the correct config folder should look something like this.  
In this case, the device I used is Poco X6 Pro 5G
```
This PC\POCO X6 Pro 5G\Internal shared storage\Android\data\com.kurogame.wutheringwaves.global\files\UE4Game\Client\Client\Saved\Config\Android
```

> ⚠️ Overwrite existing files if prompted.  

6. *(Optional)* Paste the `VulkanProgramBinaryCache` folder one level above if included.  
7. **Launch Wuthering Waves** and enjoy! 🚀  

---

## 📬 Need Help?

Join the **Discord** community for support, updates, and discussions:  
👉 https://discord.gg/renjxYBEZM

---

## 📝 Credits

Maintained by **Arglax**  
Optimized for **Mid-end/Flagship Android devices with Vulkan support**

Also giving credits to these entities as I have had config creation learnings through them indirectly and some directly:  
1. Kuya Thirdy 
2. Brandy (AlteriaX)  
3. em00se  
4. Eggsee  
5. RGCloud  


---

## 🔎 Tags (for SEO indexing)
`Wuthering Waves config`, `WuWa graphics optimization`, `Android ini mod`,  
`Vulkan shader cache`, `increase WuWa FPS`, `WuWa Engine.ini tweak`,  
`DeviceProfiles.ini tutorial`, `WuWa config Poco X6 Pro`, `WuWa lag fix Android`,  
`Mobile gaming performance`, `Arglax WuWa`, `wuwa config android`, `wuwa config`,  
`arglax`, `wuwa`, `config`, `tweak wuwa`, `wuwa configs`, `mobile wuwa config`,  
`mobile configs wuwa`, `wuthering waves optimization`, `fps boost wuwa`,  
`unreal engine 4.27 config`, `android fps boost`, `dimensity 8300 optimization`,  
`arglax tweaks`, `wuwa optimization guide`, `vulkan optimization`, `low-end optimization wuwa`

---

<a href="https://www.buymeacoffee.com/arglaxaqwv" target="_blank"> <img src="https://cdn.buymeacoffee.com/buttons/v2/arial-violet.png" alt="Optional Support Me" style="height: 60px !important; width: 217px !important;"></a>  

> Support is voluntary and does not affect config availability or updates. I will always do what I can to further optimize and improve our experiences.

# ChangeLog  
## January 3, 2026
> Updated [V3.x] High-End Config
> Updated Stable Config  
> [V3.x] Configs will be updated by this weekend, along with V2.8 Configs  
## December 30, 2025  
> Updated [V3.x] Configs  
## December 27, 2025
> Updated Config Selector Guides for [V2.8] and [V.3x]  
> [V2.8 Configs](https://github.com/Arglax/Mobile-WuWa-Config/tree/main/%5BV2.8%5D%20Working%20Configs#readme)  
> [V3.x Configs](https://github.com/Arglax/Mobile-WuWa-Config/tree/main/%5BV3.x%5D%20Working%20Configs#readme)  
## December 25, 2025
> Updated README.md of [V2.8] Config Folder  
> Added [V3.x] Config Folder
