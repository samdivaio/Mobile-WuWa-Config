# Wuthering Waves Unreal Engine CVARs Wiki

This page is UNDER DEVELOPMENT. Mistakes may be present.

Welcome to the **Wuthering Waves CVAR Wiki**, a comprehensive reference for all console variables (CVARs) and engine settings used in **Wuthering Waves** on mobile platforms. This guide is intended for players, modders, and enthusiasts who want to optimize the game’s visual quality, performance, and overall experience.

---

## What Are CVARs?

CVARs, or **console variables**, are engine-level settings that control how Unreal Engine renders graphics, manages memory, processes physics, handles audio, and runs the game logic. They are essentially "knobs" that can be tuned to improve performance, enhance visuals, or balance both, depending on your device's capabilities.

Every CVAR in this wiki is **directly extracted from the official Wuthering Waves engine configuration files**. Each variable has been carefully documented with:

- Its **category** (e.g., Rendering, Streaming, Memory, Post-Processing)
- The **config section** it belongs to in `engine.ini`
- Default value ranges
- Functional explanation
- The effect of increasing or decreasing the value
- Performance impact on mobile devices
- Recommended values for mobile gameplay

> ⚠️ **Note:** Changing CVARs can significantly affect performance and visuals. Always backup your configuration files before making modifications.

---

## How to Use This Wiki

The CVARs are presented in **tables grouped by category** for easier navigation. Each column provides essential information:

| Column | Description |
|--------|-------------|
| **CVAR** | The exact name of the console variable as defined in Unreal Engine. |
| **Category** | The functional group it belongs to (Rendering, Streaming, Memory, etc.). |
| **Section** | The `engine.ini` section where the CVAR is located. |
| **Default Range** | The expected range of values for this variable. Some cvars may exceed value depending on customizations. |
| **Function** | A short description of what the CVAR controls. |
| **Effect of ↑/↓** | What happens if you increase or decrease the value. |
| **Performance Impact** | How the CVAR affects performance on mobile devices (Low, Medium, High). |
| **Recommended (Mobile)** | Suggested values for smooth performance on mobile devices. |

---

## Mobile Optimization Guidelines

For **mobile players**, consider the following tips when modifying CVARs:

1. **Prioritize performance:** Some CVARs drastically increase GPU load (e.g., post-processing, shadows, volumetric effects). If your device lags, lower values or disable heavy effects.
2. **Incremental changes:** Adjust one variable at a time to understand its impact.
3. **Use recommended ranges:** Values listed under “Recommended (Mobile)” are for stable gameplay without excessive battery drain or overheating.
4. **Backup first:** Always save a copy of your original `engine.ini` or user settings before experimenting.
5. **FPS limits:** Keep `t.MaxFPS` and `t.MinFPS` within your device’s display and thermal capabilities.
6. **Visual balance:** Some CVARs (like color grading, bloom, and tonemapping) can be tweaked to improve visual fidelity without a heavy performance penalty.

---

## About This Documentation

- All CVARs come **directly from the released Wuthering Waves configs**.
- Duplicates have been removed, and all variables are sorted by **category** and alphabetically for clarity.
- This wiki serves as a reference; it does **not automatically apply changes**—modifications require editing your `engine.ini` or using in-game console commands.

---

Next, this wiki will present the **complete CVAR table** with recommended mobile-friendly values. Each batch is carefully curated and grouped for easier reading and adjustment.



| CVAR                                   | Category                       | Section          | Default Range | Function                                  | Effect of ↑/↓                | Performance Impact    | Recommended (Mobile) |
| -------------------------------------- | ------------------------------ | ---------------- | ------------- | ----------------------------------------- | ---------------------------- | --------------------- | -------------------- |
| Async.ParallelFor.YieldingTimeout      | System / Threading             | RendererSettings | 0–1000000     | Controls yield timeout for parallel tasks | ↑ = longer wait for threads  | Minor                 | 300000               |
| AudioThread.UseBackgroundThreadPool    | System / Threading             | RendererSettings | 0–1           | Enable background thread pool for audio   | ↑ = more threads             | Low CPU/memory impact | 1                    |
| FX.AllowAsyncTick                      | Effects / FX                   | RendererSettings | 0–1           | Allow FX to tick asynchronously           | ↑ = more async FX processing | Medium                | 1                    |
| FX.BatchAsync                          | Effects / FX                   | RendererSettings | 0–1           | Enables batched async FX updates          | ↑ = faster FX                | Medium                | 1                    |
| FX.BatchAsyncBatchSize                 | Effects / FX                   | RendererSettings | 1–64          | Number of FX processed per async batch    | ↑ = larger batch             | Slight CPU spike      | 32                   |
| TaskGraph.EnableForkedMultithreading   | System / Threading             | RendererSettings | 0–1           | Enables multithreaded task graph          | ↑ = more threads             | Medium                | 1                    |
| TaskGraph.IgnoreThreadToDoGatherOn     | System / Threading             | RendererSettings | 0–1           | Optimization for task collection          | ↑ = ignore more              | Negligible            | 0                    |
| TaskGraph.RenderThreadPollPeriodMs     | System / Threading             | RendererSettings | 0–100         | Poll interval in ms for render thread     | ↑ = slower poll              | Low                   | 1                    |
| foliage.DensityScale                   | Rendering / Foliage            | RendererSettings | 0–10          | Scale density of foliage                  | ↑ = denser foliage           | Medium GPU            | 1.0                  |
| foliage.LODDistanceScale               | Rendering / Foliage            | RendererSettings | 0–10          | Scale distance LOD for foliage            | ↑ = LOD stays farther        | Medium GPU            | 2                    |
| grass.DensityScale                     | Rendering / Foliage            | RendererSettings | 0–10          | Grass density multiplier                  | ↑ = denser grass             | Medium GPU            | 1.0                  |
| r.Android.DisableVulkanSupport         | Mobile / Rendering             | RendererSettings | 0–1           | Enable/disable Vulkan on Android          | ↑ = disables Vulkan          | Major                 | 0                    |
| r.AllowGlobalClipPlane                 | Rendering / General            | RendererSettings | 0–1           | Enables global clipping plane             | ↑ = enabled                  | Low                   | 1                    |
| r.AsyncPipelineCompile                 | Rendering / General            | RendererSettings | 0–2           | Async pipeline compile mode               | ↑ = more async               | Medium                | 2                    |
| r.BBM.BoundsScale                      | Rendering / General            | RendererSettings | 0.0–1.0       | Scale for BBM bounds                      | ↑ = larger bounds            | Negligible            | 0.6                  |
| r.BloomQuality                         | Post-Processing / Bloom        | RendererSettings | 0–5           | Bloom effect quality                      | ↑ = more bloom               | Medium GPU            | 5                    |
| r.Color.Brightness                     | Post-Processing / Tonemapping  | RendererSettings | 0–2           | Adjusts scene brightness                  | ↑ = brighter                 | Negligible            | 1.08                 |
| r.Color.ContrastAdaptation             | Post-Processing / Tonemapping  | RendererSettings | 0–5           | Contrast adaptation intensity             | ↑ = higher contrast          | Low                   | 1.45                 |
| r.Color.GradingLUTQuality              | Post-Processing / Tonemapping  | RendererSettings | 0–3           | LUT quality for grading                   | ↑ = sharper grading          | Low                   | 2                    |
| r.Color.GradingQuality                 | Post-Processing / Tonemapping  | RendererSettings | 0–3           | Overall color grading quality             | ↑ = more accurate            | Low                   | 1                    |
| r.Color.Max                            | Post-Processing / Tonemapping  | RendererSettings | 0–5           | Maximum scene brightness                  | ↑ = brighter                 | Negligible            | 1.22                 |
| r.Color.Mid                            | Post-Processing / Tonemapping  | RendererSettings | 0–5           | Midtone adjustment                        | ↑ = midtones brighter        | Negligible            | 0.48                 |
| r.Color.Saturation                     | Post-Processing / Tonemapping  | RendererSettings | 0–2           | Scene color saturation                    | ↑ = more saturated           | Low                   | 1.10                 |
| r.Color.SaturationBoost                | Post-Processing / Tonemapping  | RendererSettings | 0–2           | Additional saturation boost               | ↑ = stronger colors          | Low                   | 1.12                 |
| r.ColorGrading                         | Post-Processing / Tonemapping  | RendererSettings | 0–1           | Enable color grading                      | ↑ = enabled                  | Low                   | 1                    |
| r.ColorGradingIntensity                | Post-Processing / Tonemapping  | RendererSettings | 0–5           | Strength of color grading                 | ↑ = stronger effect          | Low                   | 2.0                  |
| r.DetailMode                           | Rendering / General            | RendererSettings | 0–3           | Mesh detail level                         | ↑ = higher detail            | Medium GPU            | 3                    |
| r.DistanceFieldBuild.EightBit          | Rendering / Shadows            | RendererSettings | 0–1           | Use 8-bit distance fields                 | ↑ = lower precision          | Low                   | 1                    |
| r.EyeAdaptationQuality                 | Post-Processing / Tonemapping  | RendererSettings | 0–3           | Eye adaptation quality                    | ↑ = smoother adaptation      | Low                   | 2                    |
| r.ForwardShading                       | Rendering / General            | RendererSettings | 0–1           | Forward shading toggle                    | ↑ = enabled                  | Low                   | 1                    |
| r.GPUCrashDebugging                    | System / Debugging             | RendererSettings | 0–1           | Enable GPU crash debug                    | ↑ = more debugging           | Slight                | 1                    |
| r.HDR.Display.ColorGamut               | Post-Processing / HDR          | RendererSettings | 0–5           | HDR color gamut                           | ↑ = wider gamut              | Low                   | 2                    |
| r.HDR.Display.OutputDevice             | Post-Processing / HDR          | RendererSettings | 0–5           | HDR output device                         | ↑ = higher device            | Low                   | 5                    |
| r.HDR.EnableHDROutput                  | Post-Processing / HDR          | RendererSettings | 0–1           | Enable HDR output                         | ↑ = enabled                  | Low                   | 1                    |
| r.HZBOcclusion                         | Rendering / Occlusion          | RendererSettings | 0–1           | Horizon-based ambient occlusion           | ↑ = stronger AO              | Medium GPU            | 1                    |
| r.HZBOcclusion.UseConservativeMipBias  | Rendering / Occlusion          | RendererSettings | 0–1           | Use conservative mip bias                 | ↑ = more conservative        | Negligible            | 1                    |
| r.imp.Compress                         | Rendering / Textures           | RendererSettings | 0–1           | Compress imposter textures                | ↑ = more compression         | Low GPU               | 1                    |
| r.imp.ImpBelowHorizonZ                 | Rendering / Textures           | RendererSettings | -10000–10000  | Horizon limit for imposter rendering      | ↑ = lower                    | Low GPU               | -1000                |
| r.imp.half                             | Rendering / Textures           | RendererSettings | 0–1           | Half-resolution imposters                 | ↑ = half res                 | Low                   | 1                    |
| r.Kuro.MaterialQualityLevel            | Rendering / Kuro               | RendererSettings | 0–3           | Material quality for Kuro                 | ↑ = higher quality           | Medium                | 1                    |
| r.Kuro.PlanarReflection.LimitWidth     | Rendering / Kuro               | RendererSettings | 0–8           | Width limit for planar reflection         | ↑ = higher width             | Low GPU               | 1                    |
| r.Kuro.PlanarReflection.WidthThreshold | Rendering / Kuro               | RendererSettings | 0–2048        | Width threshold for planar reflections    | ↑ = higher threshold         | Low GPU               | 512                  |
| r.KuroTonemapping                      | Post-Processing / Tonemapping  | RendererSettings | 0–1           | Kuro tonemapping                          | ↑ = enabled                  | Low                   | 1                    |
| r.LandscapeLOD0ScreenSizeScale         | Rendering / Landscape          | RendererSettings | 0–5           | Scale for LOD0 screen size                | ↑ = larger LOD0              | Medium GPU            | 1                    |
| r.LandscapeReverseLODScaleFactor       | Rendering / Landscape          | RendererSettings | 0–5           | Reverse LOD scaling                       | ↑ = more aggressive LOD      | Medium GPU            | 2                    |
| r.LensFlareQuality                     | Post-Processing / Lens Flare   | RendererSettings | 0–5           | Lens flare quality                        | ↑ = stronger flares          | Low GPU               | 1                    |
| r.LightShaftQuality                    | Post-Processing / Light Shafts | RendererSettings | 0–5           | Light shaft quality                       | ↑ = more detail              | Medium GPU            | 1                    |
| r.MaterialQualityLevel                 | Rendering / Materials          | RendererSettings | 0–3           | Global material quality                   | ↑ = higher quality           | Medium GPU            | 1                    |
| r.MaxAnisotropy                        | Rendering / Materials          | RendererSettings | 1–16          | Max texture anisotropy                    | ↑ = sharper textures         | Medium GPU            | 16                   |

| CVAR                                               | Category                    | Section          | Default Range | Function                                         | Effect of ↑/↓                   | Performance Impact | Recommended (Mobile) |
| -------------------------------------------------- | --------------------------- | ---------------- | ------------- | ------------------------------------------------ | ------------------------------- | ------------------ | -------------------- |
| r.MeshDrawCommands.ParallelPassSetup               | System / Threading          | RendererSettings | 0–1           | Enable parallel setup for mesh draw commands     | ↑ = more parallelization        | Low CPU            | 1                    |
| r.MeshDrawCommands.UseCachedCommands               | System / Threading          | RendererSettings | 0–1           | Use cached draw commands                         | ↑ = faster draw calls           | Low                | 1                    |
| r.MipMapLODBias                                    | Rendering / Textures        | RendererSettings | -10–10        | LOD bias for mipmaps                             | ↑ = lower detail textures       | Medium GPU         | 0                    |
| r.Mobile.AdrenoOcclusionMode                       | Mobile / Rendering          | RendererSettings | 0–3           | Ambient occlusion mode on Adreno                 | ↑ = higher quality AO           | Medium GPU         | 1                    |
| r.Mobile.CustomDepthForToonRim                     | Mobile / Rendering          | RendererSettings | 0–1           | Custom depth for toon rim lighting               | ↑ = enabled                     | Low                | 1                    |
| r.Mobile.DeviceEvaluation                          | Mobile / Rendering          | RendererSettings | 0–5           | Device performance evaluation                    | ↑ = higher evaluation           | Negligible         | 3                    |
| r.Mobile.DynamicPointLightsUseStaticBranch         | Mobile / Rendering          | RendererSettings | 0–1           | Use static branch for dynamic lights             | ↑ = more static branching       | Low                | 1                    |
| r.Mobile.EnableStaticAndCSMShadowReceivers         | Mobile / Shadows            | RendererSettings | 0–1           | Enable static and CSM shadow receivers           | ↑ = enabled                     | Medium GPU         | 1                    |
| r.Mobile.GTAO.Quality                              | Mobile / Post-Processing    | RendererSettings | 0–4           | GTAO quality                                     | ↑ = higher quality AO           | Medium GPU         | 2                    |
| r.Mobile.HighQualityMaterial                       | Mobile / Materials          | RendererSettings | 0–1           | Enable high-quality materials                    | ↑ = higher quality              | Medium GPU         | 1                    |
| r.Mobile.KuroSeparateTranslucency                  | Mobile / Materials          | RendererSettings | 0–1           | Separate translucency for Kuro                   | ↑ = enabled                     | Medium GPU         | 1                    |
| r.Mobile.SceneColorFormat                          | Mobile / Rendering          | RendererSettings | 0–5           | Scene color format                               | ↑ = higher precision            | Medium GPU         | 4                    |
| r.Mobile.SceneObjMobileSSR                         | Mobile / Post-Processing    | RendererSettings | 0–1           | Mobile SSR on objects                            | ↑ = higher SSR                  | Medium GPU         | 1                    |
| r.Mobile.TonemapperFilm                            | Mobile / Post-Processing    | RendererSettings | 0–1           | Film tonemapper                                  | ↑ = enabled                     | Low                | 1                    |
| r.Mobile.TreeRimLight                              | Mobile / Materials          | RendererSettings | 0–1           | Tree rim lighting                                | ↑ = enabled                     | Medium GPU         | 1                    |
| r.Mobile.WaterSSRResDiv                            | Mobile / Water              | RendererSettings | 1–8           | Screen-space water reflection resolution divisor | ↑ = lower res SSR               | Medium GPU         | 1.5                  |
| r.Mobile.WaterSSRStep                              | Mobile / Water              | RendererSettings | 16–512        | Step count for water SSR                         | ↑ = higher accuracy             | Medium GPU         | 192                  |
| r.Mobile.WaterTAAWeight                            | Mobile / Post-Processing    | RendererSettings | 0–1           | Water TAA blending weight                        | ↑ = stronger TAA                | Low                | 0.8                  |
| r.MobileHDR                                        | Mobile / Post-Processing    | RendererSettings | 0–1           | Enable mobile HDR                                | ↑ = enabled                     | Medium GPU         | 1                    |
| r.MobileHDR32bppMode                               | Mobile / Post-Processing    | RendererSettings | 0–1           | HDR 32-bit mode                                  | ↑ = enabled                     | Medium GPU         | 1                    |
| r.MultithreadedLightmapEncode                      | System / Threading          | RendererSettings | 0–1           | Encode lightmaps multithreaded                   | ↑ = enabled                     | Medium CPU         | 1                    |
| r.ParallelBasePass                                 | System / Threading          | RendererSettings | 0–1           | Parallelize base pass                            | ↑ = enabled                     | Medium GPU         | 1                    |
| r.ParallelInitViews                                | System / Threading          | RendererSettings | 0–1           | Parallel view initialization                     | ↑ = enabled                     | Medium GPU         | 1                    |
| r.ParallelPrePass                                  | System / Threading          | RendererSettings | 0–1           | Parallel pre-pass rendering                      | ↑ = enabled                     | Medium GPU         | 1                    |
| r.ParallelTranslucency                             | System / Threading          | RendererSettings | 0–1           | Parallel translucency pass                       | ↑ = enabled                     | Medium GPU         | 1                    |
| r.ParallelVelocity                                 | System / Threading          | RendererSettings | 0–1           | Parallel velocity buffer pass                    | ↑ = enabled                     | Medium GPU         | 1                    |
| r.PipelineCache.BatchSize                          | System / Rendering          | RendererSettings | 1–16          | Batch size for pipeline cache compilation        | ↑ = more compiled at once       | Low                | 4                    |
| r.PSO.CompilationMode                              | System / Rendering          | RendererSettings | 0–2           | Pipeline state object compilation mode           | ↑ = more aggressive             | Low                | 2                    |
| r.RefractionQuality                                | Rendering / Post-Processing | RendererSettings | 0–3           | Refraction quality                               | ↑ = sharper refraction          | Medium GPU         | 1                    |
| r.ReflectionCaptureResolution                      | Rendering / Reflections     | RendererSettings | 64–2048       | Resolution for reflection captures               | ↑ = sharper reflections         | Medium GPU         | 256                  |
| r.ReflectionEnvironment                            | Rendering / Reflections     | RendererSettings | 0–1           | Enable reflection environment                    | ↑ = enabled                     | Medium GPU         | 1                    |
| r.ReflectionEnvironmentLightmapMixBasedOnRoughness | Rendering / Reflections     | RendererSettings | 0–1           | Mix reflection/lightmap based on roughness       | ↑ = more accurate               | Low                | 1                    |
| r.RenderTargetPoolMin                              | System / Rendering          | RendererSettings | 128–2048      | Minimum render target pool size                  | ↑ = more memory used            | Medium             | 512                  |
| r.RHICmdUseParallelAlgorithms                      | System / Threading          | RendererSettings | 0–1           | Use parallel RHI algorithms                      | ↑ = enabled                     | Medium GPU         | 1                    |
| r.Roughness.ApplyToSSR                             | Rendering / Materials       | RendererSettings | 0–1           | Apply roughness to SSR                           | ↑ = stronger effect             | Low                | 1                    |
| r.Roughness.MinRoughness                           | Rendering / Materials       | RendererSettings | 0–1           | Minimum roughness                                | ↑ = more matte                  | Low                | 0.35                 |
| r.Roughness.Override                               | Rendering / Materials       | RendererSettings | 0–1           | Override roughness globally                      | ↑ = stronger override           | Low                | 0                    |
| r.SecondaryScreenPercentage.GameViewport           | Rendering / Post-Processing | RendererSettings | 50–150        | Secondary screen percentage for viewport         | ↑ = higher resolution           | Medium GPU         | 75                   |
| r.SeparateTranslucency                             | Rendering / Post-Processing | RendererSettings | 0–1           | Enable separate translucency                     | ↑ = enabled                     | Medium GPU         | 1                    |
| r.ShaderPipelineCache.BackgroundBatchSize          | System / Rendering          | RendererSettings | 1–16          | Background shader pipeline batch size            | ↑ = more compiled in background | Low                | 6                    |
| r.ShaderPipelineCache.PrecompileBatchSize          | System / Rendering          | RendererSettings | 1–32          | Precompile batch size                            | ↑ = more compiled               | Low                | 20                   |
| r.ShaderPipelineCache.PreOptimizeEnabled           | System / Rendering          | RendererSettings | 0–1           | Pre-optimize shaders                             | ↑ = enabled                     | Low                | 1                    |
| r.ShaderPipelineCache.StartupMode                  | System / Rendering          | RendererSettings | 0–3           | Startup mode for shader pipeline cache           | ↑ = more aggressive             | Low                | 3                    |
| r.Shadow.RadiusThresholdFar                        | Rendering / Shadows         | RendererSettings | 0–1           | Shadow radius threshold                          | ↑ = shadows render farther      | Medium GPU         | 0.2                  |
| r.SkinCache.Mode                                   | Rendering / Materials       | RendererSettings | 0–2           | Skin cache mode                                  | ↑ = more aggressive caching     | Low                | 1                    |
| r.SkyBlending.AllowSettingLerpPerFrame             | Rendering / Sky             | RendererSettings | 0–1           | Allow sky blending per frame                     | ↑ = enabled                     | Low                | 1                    |
| r.Specular.Scale                                   | Rendering / Materials       | RendererSettings | 0–2           | Specular intensity scale                         | ↑ = brighter specular           | Medium GPU         | 0.8                  |
| r.SpecularHighlights                               | Rendering / Materials       | RendererSettings | 0–1           | Enable specular highlights                       | ↑ = enabled                     | Medium GPU         | 1                    |
| r.SSGI.Quality                                     | Rendering / Post-Processing | RendererSettings | 0–3           | Screen-space global illumination                 | ↑ = higher quality              | Medium GPU         | 1                    |
| r.SSR.HalfResSceneColor                            | Rendering / Post-Processing | RendererSettings | 0–1           | Half-resolution SSR                              | ↑ = lower resolution            | Low                | 1                    |
| r.SSR.MaxRoughness                                 | Rendering / Post-Processing | RendererSettings | 0–1           | Max roughness for SSR                            | ↑ = rougher reflections         | Low                | 1                    |

| CVAR                                              | Category                        | Section          | Default Range | Function                                    | Effect of ↑/↓                | Performance Impact | Recommended (Mobile) |
| ------------------------------------------------- | ------------------------------- | ---------------- | ------------- | ------------------------------------------- | ---------------------------- | ------------------ | -------------------- |
| r.SSR.Quality                                     | Rendering / Post-Processing     | RendererSettings | 0–5           | Screen-space reflections quality            | ↑ = higher quality           | Medium GPU         | 3                    |
| r.SSR.Temporal                                    | Rendering / Post-Processing     | RendererSettings | 0–1           | Enable temporal SSR                         | ↑ = more stable SSR          | Low                | 1                    |
| r.SSS.Filter                                      | Rendering / Post-Processing     | RendererSettings | 0–1           | Enable subsurface scattering filter         | ↑ = smoother scattering      | Medium GPU         | 1                    |
| r.SSS.HalfRes                                     | Rendering / Post-Processing     | RendererSettings | 0–1           | Half-resolution SSS                         | ↑ = lower resolution         | Low                | 1                    |
| r.SSS.Quality                                     | Rendering / Post-Processing     | RendererSettings | 0–3           | Subsurface scattering quality               | ↑ = higher quality           | Medium GPU         | 1                    |
| r.SSS.SampleSet                                   | Rendering / Post-Processing     | RendererSettings | 0–4           | SSS sample set selection                    | ↑ = more samples             | Medium GPU         | 2                    |
| r.SSS.Scale                                       | Rendering / Post-Processing     | RendererSettings | 0–5           | SSS intensity scale                         | ↑ = stronger effect          | Low                | 1                    |
| r.SupportPointLightWholeSceneShadows              | Rendering / Shadows             | RendererSettings | 0–1           | Enable whole-scene shadows for point lights | ↑ = enabled                  | Medium GPU         | 1                    |
| r.TemporalAA.Algorithm                            | Post-Processing / Anti-Aliasing | RendererSettings | 0–2           | Temporal AA algorithm                       | ↑ = higher quality           | Medium GPU         | 1                    |
| r.TemporalAA.HistoryScreenPercentage              | Post-Processing / Anti-Aliasing | RendererSettings | 50–200        | TAA history resolution                      | ↑ = sharper AA               | Medium GPU         | 150                  |
| r.TemporalAA.Upsampling                           | Post-Processing / Anti-Aliasing | RendererSettings | 0–1           | Enable TAA upsampling                       | ↑ = enabled                  | Medium GPU         | 1                    |
| r.TemporalAA.FilterSize                           | Post-Processing / Anti-Aliasing | RendererSettings | 0–5           | TAA filter size                             | ↑ = smoother AA              | Medium GPU         | 1.0                  |
| r.TemporalAA.TAAUpsampling                        | Post-Processing / Anti-Aliasing | RendererSettings | 0–1           | Enable TAA upsampling                       | ↑ = enabled                  | Medium GPU         | 1                    |
| r.Tonemapper.GrainQuantization                    | Post-Processing / Tonemapping   | RendererSettings | 0–1           | Quantize grain in tonemapper                | ↑ = stronger grain           | Low                | 1                    |
| r.Tonemapper.Quality                              | Post-Processing / Tonemapping   | RendererSettings | 0–5           | Tonemapper quality                          | ↑ = sharper                  | Medium GPU         | 5                    |
| r.Tonemapper.Sharpen                              | Post-Processing / Tonemapping   | RendererSettings | 0–1           | Tonemapper sharpening                       | ↑ = sharper image            | Low                | 0.04                 |
| r.TonemapperFilm                                  | Post-Processing / Tonemapping   | RendererSettings | 0–1           | Film tonemapper                             | ↑ = enabled                  | Low                | 1                    |
| r.TonemapperFilmContrast                          | Post-Processing / Tonemapping   | RendererSettings | 0–2           | Film contrast                               | ↑ = higher contrast          | Low                | 1.1                  |
| r.TonemapperFilmGrainIntensity                    | Post-Processing / Tonemapping   | RendererSettings | 0–1           | Film grain intensity                        | ↑ = more grain               | Low                | 0.02                 |
| r.TonemapperFilmMid                               | Post-Processing / Tonemapping   | RendererSettings | 0–1           | Midtone film curve                          | ↑ = brighter midtones        | Low                | 0.46                 |
| r.TonemapperFilmSaturation                        | Post-Processing / Tonemapping   | RendererSettings | 0–2           | Film saturation                             | ↑ = more saturated           | Low                | 1.12                 |
| r.TonemapperFilmShadow                            | Post-Processing / Tonemapping   | RendererSettings | 0–2           | Shadow intensity                            | ↑ = darker shadows           | Low                | 0.88                 |
| r.TonemapperFilmToneCurveAmount                   | Post-Processing / Tonemapping   | RendererSettings | 0–3           | Tone curve strength                         | ↑ = stronger curve           | Low                | 1.2                  |
| r.TonemapperFilmWhitePoint                        | Post-Processing / Tonemapping   | RendererSettings | 0–3           | Film white point                            | ↑ = brighter whites          | Low                | 1.1                  |
| r.TonemapperGamma                                 | Post-Processing / Tonemapping   | RendererSettings | 0–5           | Gamma correction                            | ↑ = brighter image           | Low                | 1.95                 |
| r.Upscale.Quality                                 | Post-Processing / Upscaling     | RendererSettings | 0–5           | Upscaling quality                           | ↑ = sharper upscale          | Medium GPU         | 5                    |
| r.ViewDistanceScale                               | Rendering / General             | RendererSettings | 0.1–10        | Scale view distance                         | ↑ = render farther objects   | High GPU           | 1.5                  |
| r.VTMaxAnisotropy                                 | Rendering / Materials           | RendererSettings | 1–16          | Virtual texture anisotropy                  | ↑ = sharper virtual textures | Medium GPU         | 16                   |
| r.Vulkan.CPURHIThreadFramePacer                   | System / Vulkan                 | RendererSettings | 0–1           | Enable CPU RHI thread pacing                | ↑ = more pacing              | Low                | 1                    |
| r.Vulkan.CPURenderthreadFramePacer                | System / Vulkan                 | RendererSettings | 0–1           | Enable CPU render thread pacing             | ↑ = more pacing              | Low                | 1                    |
| r.Vulkan.DelayAcquireBackBuffer                   | System / Vulkan                 | RendererSettings | 0–1           | Delay back buffer acquisition               | ↑ = enabled                  | Low                | 1                    |
| r.Vulkan.ExtensionFramePacer                      | System / Vulkan                 | RendererSettings | 0–1           | Use extension frame pacing                  | ↑ = enabled                  | Low                | 1                    |
| r.Vulkan.PipelineCacheFromShaderPipelineCache     | System / Vulkan                 | RendererSettings | 0–1           | Pipeline cache from shader pipeline         | ↑ = enabled                  | Low                | 1                    |
| r.Vulkan.PipelineLRUCacheEvictBinaryPreloadScreen | System / Vulkan                 | RendererSettings | 0–1           | Evict LRU cache on preload                  | ↑ = enabled                  | Low                | 1                    |
| r.Vulkan.PresentMode                              | System / Vulkan                 | RendererSettings | 0–2           | Vulkan swapchain present mode               | ↑ = more aggressive          | Low                | 0                    |
| r.Vulkan.SwapChainMemoryType                      | System / Vulkan                 | RendererSettings | 0–2           | Swapchain memory type                       | ↑ = higher memory usage      | Medium             | 2                    |
| r.Vulkan.UseRealUBs                               | System / Vulkan                 | RendererSettings | 0–1           | Use real uniform buffers                    | ↑ = enabled                  | Low                | 1                    |
| Slate.AllowBackgroundBlurWidgets                  | UI / Slate                      | RendererSettings | 0–1           | Background blur in widgets                  | ↑ = enabled                  | Low                | 0                    |
| Slate.TargetFrameRateForResponsiveness            | UI / Slate                      | RendererSettings | 30–120        | Target responsiveness frame rate            | ↑ = smoother UI              | Low                | 60                   |
| Slate.TooltipIntroDuration                        | UI / Slate                      | RendererSettings | 0–1           | Tooltip intro animation duration            | ↑ = longer intro             | Negligible         | 0.0                  |
| Slate.TooltipSummonDelay                          | UI / Slate                      | RendererSettings | 0–2           | Delay before tooltip shows                  | ↑ = longer delay             | Negligible         | 0.1                  |
| tick.AllowAsyncComponentTicks                     | System / Threading              | RendererSettings | 0–1           | Async component ticking                     | ↑ = enabled                  | Medium CPU         | 1                    |
| tick.AllowAsyncTickCleanup                        | System / Threading              | RendererSettings | 0–1           | Async tick cleanup                          | ↑ = enabled                  | Medium CPU         | 1                    |
| tick.AllowAsyncTickDispatch                       | System / Threading              | RendererSettings | 0–1           | Async tick dispatch                         | ↑ = enabled                  | Medium CPU         | 1                    |
| tick.AllowConcurrentTickQueue                     | System / Threading              | RendererSettings | 0–1           | Enable concurrent tick queue                | ↑ = enabled                  | Medium CPU         | 1                    |
| tick.SecondsBeforeEmbeddedAppSleeps               | System / Threading              | RendererSettings | 0–60          | Time before app sleep                       | ↑ = longer wait              | Negligible         | 12                   |
| wp.Runtime.KuroRuntimeStreamingRangeOverallScale  | Streaming / Kuro                | RendererSettings | 0–5           | Runtime streaming range scale               | ↑ = wider range              | Medium GPU/Memory  | 2.0                  |
| wp.Runtime.SoraGridBlackListHeight                | Streaming / Kuro                | RendererSettings | 0–100000      | Max height for Sora blacklist               | ↑ = higher limit             | Negligible         | 10000                |

| CVAR                                          | Category                        | Section           | Default Range | Function                              | Effect of ↑/↓           | Performance Impact | Recommended (Mobile) |
| --------------------------------------------- | ------------------------------- | ----------------- | ------------- | ------------------------------------- | ----------------------- | ------------------ | -------------------- |
| r.Streaming.Boost                             | Streaming / General             | StreamingSettings | 0–10          | Streaming boost multiplier            | ↑ = faster streaming    | Medium GPU/Memory  | 2–3                  |
| r.Streaming.DefragDynamicBounds               | Streaming / General             | StreamingSettings | 0–1           | Defragment dynamic bounds             | ↑ = enabled             | Low                | 1                    |
| r.Streaming.FullyLoadUsedTextures             | Streaming / Textures            | StreamingSettings | 0–1           | Fully load textures                   | ↑ = enabled             | Medium Memory      | 1                    |
| r.Streaming.HiddenPrimitiveScale              | Streaming / Textures            | StreamingSettings | 0–1           | Scale for hidden primitives           | ↑ = larger textures     | Low                | 0.5                  |
| r.Streaming.HLODStrategy                      | Streaming / Textures            | StreamingSettings | 0–3           | HLOD streaming strategy               | ↑ = more aggressive     | Low                | 2                    |
| r.Streaming.KuroMinFOVFactorForStreaming      | Streaming / Kuro                | StreamingSettings | 0–1           | Min FOV factor for streaming          | ↑ = more aggressive     | Low                | 0.06                 |
| r.Streaming.LimitPoolSizeToVRAM               | Streaming / Memory              | StreamingSettings | 0–1           | Limit pool size to VRAM               | ↑ = stricter limit      | Medium GPU/Memory  | 1                    |
| r.Streaming.MipBias                           | Streaming / Textures            | StreamingSettings | -5–5          | Global mip bias                       | ↑ = lower detail        | Medium GPU         | 0.5                  |
| r.Streaming.MinMipForSplitRequest             | Streaming / Textures            | StreamingSettings | 0–12          | Minimum mip for split request         | ↑ = higher quality      | Medium GPU         | 8                    |
| r.Streaming.OverlapAssetAndLevelTicks         | Streaming / General             | StreamingSettings | 0–1           | Overlap asset & level streaming       | ↑ = enabled             | Low                | 1                    |
| r.Streaming.PoolSize                          | Streaming / Memory              | StreamingSettings | 128–8192      | Streaming pool size (MB)              | ↑ = larger pool         | Medium GPU/Memory  | 2560–5144            |
| r.Streaming.QualityExtraLODBiasSetting        | Streaming / Textures            | StreamingSettings | 0–3           | Extra LOD bias                        | ↑ = lower detail        | Medium GPU         | 0                    |
| r.Streaming.UseAsyncRequestsForDDC            | Streaming / Memory              | StreamingSettings | 0–1           | Async DDC requests                    | ↑ = enabled             | Low                | 1                    |
| r.Streaming.UseNewMetrics                     | Streaming / General             | StreamingSettings | 0–1           | Enable new streaming metrics          | ↑ = enabled             | Low                | 1                    |
| s.AsyncLoadingThreadEnabled                   | Streaming / System              | StreamingSettings | 0–1           | Async loading thread                  | ↑ = enabled             | Low                | 1                    |
| s.IoDispatcherBufferMemorySizeMB              | Streaming / System              | StreamingSettings | 128–1024      | IO dispatcher buffer size             | ↑ = larger buffer       | Medium Memory      | 256                  |
| s.IoDispatcherCacheSizeMB                     | Streaming / System              | StreamingSettings | 128–1024      | IO dispatcher cache size              | ↑ = larger cache        | Medium Memory      | 512                  |
| s.MinBulkDataSizeForAsyncLoading              | Streaming / System              | StreamingSettings | 8192–65536    | Minimum bulk data size for async      | ↑ = larger threshold    | Medium             | 16384                |
| a.URO.ForceAnimRate                           | System / Animations             | SystemSettings    | 0–1           | Force animation rate                  | ↑ = enforced            | Low                | 1                    |
| FX.AllowCulling                               | Rendering / FX                  | SystemSettings    | 0–1           | Allow FX culling                      | ↑ = more culling        | Low                | 1                    |
| r.DiscardUnusedQuality                        | System / General                | SystemSettings    | 0–1           | Discard unused quality                | ↑ = discard more        | Low                | 0                    |
| r.DontLimitOnBattery                          | System / Performance            | SystemSettings    | 0–1           | Disable battery limit                 | ↑ = enabled             | Low                | 1                    |
| r.DynamicMeshElementByParallel                | System / Rendering              | SystemSettings    | 0–1           | Parallel dynamic mesh elements        | ↑ = enabled             | Medium GPU         | 1                    |
| r.FEstimation.Option                          | Rendering / FX                  | SystemSettings    | 0–2           | Estimation option                     | ↑ = more aggressive     | Low                | 1                    |
| r.FEstimation.WorkingDeltaSec                 | Rendering / FX                  | SystemSettings    | 0–1           | Delta time for estimation             | ↑ = slower estimation   | Low                | 0                    |
| r.FrustumCullNumWordsPerTask                  | System / Rendering              | SystemSettings    | 16–64         | Frustum cull task size                | ↑ = more per task       | Low                | 32                   |
| r.MotionBlur.Amount                           | Post-Processing / Motion        | SystemSettings    | 0–1           | Motion blur amount                    | ↑ = stronger blur       | Medium GPU         | 0.2                  |
| r.ParticleLODBias                             | Rendering / Particles           | SystemSettings    | -5–5          | Particle LOD bias                     | ↑ = lower detail        | Medium GPU         | -2                   |
| r.SkeletalMeshLODBias                         | Rendering / Meshes              | SystemSettings    | -5–5          | Skeletal mesh LOD bias                | ↑ = lower detail        | Medium GPU         | 10                   |
| r.StaticMesh.VertexCompressEnabled            | Rendering / Meshes              | SystemSettings    | 0–1           | Vertex compression                    | ↑ = enabled             | Low                | 1                    |
| r.TemporalAA.MobileFrameWeight                | Post-Processing / Anti-Aliasing | SystemSettings    | 0–1           | Mobile TAA frame weight               | ↑ = stronger blending   | Medium GPU         | 0.25                 |
| r.TemporalAA.MobileStaticFrameWeight          | Post-Processing / Anti-Aliasing | SystemSettings    | 0–1           | Mobile TAA static weight              | ↑ = stronger blending   | Medium GPU         | 0.3                  |
| r.Vulkan.DescriptorSetLayoutMode              | System / Vulkan                 | SystemSettings    | 0–2           | Descriptor set layout mode            | ↑ = more aggressive     | Low                | 1                    |
| r.Vulkan.DSetCacheTargetSetsPerPool           | System / Vulkan                 | SystemSettings    | 1024–65536    | Target sets per pool                  | ↑ = more cache          | Medium Memory      | 16384                |
| s.LevelStreamingActorsUpdateTimeLimit         | Streaming / System              | SystemSettings    | 1–30          | Level streaming update time limit     | ↑ = slower updates      | Low                | 5.0                  |
| s.PriorityLevelStreamingActorsUpdateExtraTime | Streaming / System              | SystemSettings    | 1–30          | Extra update time for priority actors | ↑ = longer updates      | Low                | 5.0                  |
| s.PriorityAsyncLoadingExtraTime               | Streaming / System              | SystemSettings    | 1–30          | Extra async loading time              | ↑ = longer updates      | Low                | 10.0                 |
| rhi.SyncInterval                              | System / Rendering              | SystemSettings    | 0–2           | RHI sync interval                     | ↑ = slower frame pacing | Medium GPU         | 1                    |
| slate.AbsoluteIndices                         | UI / Slate                      | SystemSettings    | 0–1           | Absolute indices for Slate            | ↑ = enabled             | Low                | 1                    |
| Puerts                                        | Logging / Dev                   | Core.Log          | none–all      | Logging level                         | ↑ = less logging        | Negligible         | none                 |
| LogJson                                       | Logging / Dev                   | Core.Log          | none–all      | JSON logging                          | ↑ = less logging        | Negligible         | none                 |
| LogCsMobile                                   | Logging / Dev                   | Core.Log          | none–all      | CS Mobile logging                     | ↑ = less logging        | Negligible         | none                 |
| LogTpMobile                                   | Logging / Dev                   | Core.Log          | none–all      | TP Mobile logging                     | ↑ = less logging        | Negligible         | none                 |

| CVAR                                    | Category              | Section                   | Default Range | Function                       | Effect of ↑/↓          | Performance Impact | Recommended (Mobile) |
| --------------------------------------- | --------------------- | ------------------------- | ------------- | ------------------------------ | ---------------------- | ------------------ | -------------------- |
| bAllowPrecompiledShaders                | Shaders / Compilation | DevOptions.Shaders        | 0–1           | Allow precompiled shaders      | ↑ = enabled            | Low                | 1                    |
| bCompilePreloadShaders                  | Shaders / Compilation | DevOptions.Shaders        | 0–1           | Compile preload shaders        | ↑ = enabled            | Low                | 1                    |
| bForcePrecompiledShaders                | Shaders / Compilation | DevOptions.Shaders        | 0–1           | Force precompiled shaders      | ↑ = enabled            | Low                | 1                    |
| bPrecompileVisibleShadersForRendering   | Shaders / Compilation | DevOptions.Shaders        | 0–1           | Precompile visible shaders     | ↑ = enabled            | Low                | 1                    |
| bPreloadAllShaders                      | Shaders / Compilation | DevOptions.Shaders        | 0–1           | Preload all shaders            | ↑ = enabled            | Medium Memory      | 1                    |
| bPreloadShaderCacheOnDemand             | Shaders / Compilation | DevOptions.Shaders        | 0–1           | Preload shader cache           | ↑ = enabled            | Low                | 1                    |
| bPreloadShadersOnDemand                 | Shaders / Compilation | DevOptions.Shaders        | 0–1           | Preload shaders on demand      | ↑ = enabled            | Low                | 1                    |
| bUsePrecompiledShaders                  | Shaders / Compilation | DevOptions.Shaders        | 0–1           | Use precompiled shaders        | ↑ = enabled            | Low                | 1                    |
| bWaitForShaderCompilation               | Shaders / Compilation | DevOptions.Shaders        | 0–1           | Wait for shader compilation    | ↑ = enabled            | Low                | 1                    |
| DeviceProfileName                       | Mobile / General      | AndroidRuntimeSettings    | N/A           | Device profile selection       | ↑ = higher-end profile | Low                | Android_VeryHigh     |
| a.UseSwappyForFramePacing               | Mobile / Performance  | AndroidRuntimeSettings    | 0–1           | Use Swappy for frame pacing    | ↑ = enabled            | Low                | 1                    |
| bEnableDynamicMaxFPS                    | Mobile / Performance  | AndroidRuntimeSettings    | 0–1           | Enable dynamic max FPS         | ↑ = enabled            | Low                | 1                    |
| bSupportsVulkanSM5                      | Mobile / Rendering    | AndroidRuntimeSettings    | 0–1           | Vulkan SM5 support             | ↑ = enabled            | Medium GPU         | 1                    |
| r.VSync                                 | Mobile / Performance  | AndroidRuntimeSettings    | 0–1           | Vertical sync                  | ↑ = enabled            | Medium GPU         | 0                    |
| t.MaxFPS                                | System / Performance  | AndroidRuntimeSettings    | 30–240        | Max FPS                        | ↑ = higher FPS         | Medium CPU/GPU     | 90                   |
| t.MinFPS                                | System / Performance  | AndroidRuntimeSettings    | 30–120        | Min FPS                        | ↑ = higher floor       | Medium CPU/GPU     | 60                   |
| FrameRateLimit                          | System / Performance  | GameUserSettings          | 30–240        | FPS limit                      | ↑ = higher limit       | Medium CPU/GPU     | 90                   |
| t.MaxWorkerThreads                      | System / Threading    | ConsoleVariables          | 1–32          | Maximum worker threads         | ↑ = more threads       | Medium CPU         | 8                    |
| gc.AllowInitialGarbageCollection        | Memory / GC           | GarbageCollectionSettings | 0–1           | Allow initial GC               | ↑ = enabled            | Low                | 1                    |
| gc.BlueprintClusteringEnabled           | Memory / GC           | GarbageCollectionSettings | 0–1           | Blueprint clustering           | ↑ = enabled            | Low                | 1                    |
| gc.CollectGarbageEveryFrame             | Memory / GC           | GarbageCollectionSettings | 0–1           | Collect garbage every frame    | ↑ = more frequent      | Medium CPU         | 0                    |
| gc.DisableAutomaticGC                   | Memory / GC           | GarbageCollectionSettings | 0–1           | Disable automatic GC           | ↑ = disabled           | Medium CPU         | 0                    |
| gc.ForceGCAtRegularInterval             | Memory / GC           | GarbageCollectionSettings | 0–1           | Force GC at intervals          | ↑ = more frequent      | Medium CPU         | 0                    |
| gc.MaxGCClusterSize                     | Memory / GC           | GarbageCollectionSettings | 1–256         | Max cluster size               | ↑ = bigger clusters    | Medium Memory      | 64                   |
| gc.MaxObjectsNotConsideredByGC          | Memory / GC           | GarbageCollectionSettings | 0–1024        | Max objects ignored            | ↑ = more ignored       | Low                | 0                    |
| gc.MinDesiredObjectsPerSubTask          | Memory / GC           | GarbageCollectionSettings | 1–100         | Min objects per GC task        | ↑ = larger batches     | Low                | 20                   |
| gc.MinGCClusterSize                     | Memory / GC           | GarbageCollectionSettings | 1–16          | Min cluster size               | ↑ = bigger clusters    | Low                | 4                    |
| gc.NumRetriesBeforeForcingGC            | Memory / GC           | GarbageCollectionSettings | 1–10          | Retry attempts                 | ↑ = more retries       | Low                | 5                    |
| gc.RandomFrequency                      | Memory / GC           | GarbageCollectionSettings | 0–10          | Random frequency               | ↑ = more randomness    | Low                | 0                    |
| gc.StallCollectionWhileWaiting          | Memory / GC           | GarbageCollectionSettings | 0–1           | Stall collection while waiting | ↑ = enabled            | Low                | 0                    |
| gc.TimeBetweenPurgingPendingKillObjects | Memory / GC           | GarbageCollectionSettings | 1–60          | Time between purging           | ↑ = longer interval    | Low                | 10                   |
| gc.ValidateGCHeap                       | Memory / GC           | GarbageCollectionSettings | 0–1           | Validate GC heap               | ↑ = enabled            | Medium CPU         | 0                    |
| gc.VerifyUObjectsAreNotFGCObjects       | Memory / GC           | GarbageCollectionSettings | 0–1           | Verify UObject status          | ↑ = stricter           | Low                | 0                    |

---

Not final. Under development

