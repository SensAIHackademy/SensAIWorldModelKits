# SensAI World Model Kits 🌍

This is a collection of world model kits for building immersive world model experiences across WebXR, Unity and Unreal Engine.

## 📝 Table of Contents

1. [WorldLabs WebXR Kit](#1-worldlabs-webxr-kit) 
2. [WorldLabs Unity Kit](#2-worldlabs-unity-kit) 
3. [WorldLabs Unreal Kit](#3-worldlabs-webxr-kit)  
4. [Acknowledgements & Credits](#4-acknowledgements--credits)  
5. [License](#5-license)
6. [Contact](#6-contact)


## Overview

## 1. WorldLabs WebXR Kit (Spark.js)

🎯 A WebXR template project for building immersive world model experiences with Gaussian splats, spatial UI, and locomotion - runnable in any WebXR-capable browser.

<br>

- Renders local or remote .spz/.ply Gaussian splats using SparkJS 2.0 with GPU-accelerated fly-in/fly-out animations
- Includes Level-of-Detail (LoD) support - adjusts splat quality by distance to maintain stable framerates on headsets
- Built on IWSDK for locomotion, grabbing, spatial UI, and XR session management

<br>

:warning: Setup Notes
* **Prerequisites**: Node ≥ 20.19.0 and a WebXR-capable browser
* **Splat Files**: Keep large splat files outside the repo and load via URL


#### GitHub: 👉 [WorldLabs WebXR Kit](https://github.com/V4C38/sensai-webxr-worldmodels) 

---

## 2. WorldLabs Unity Kit

🎯 A Unity package for generating and rendering 3D Gaussian Splatting scenes using the WorldLabs API with a built-in runtime VR world browser.

<br>

- Generate 3D scenes from text prompts via the WorldLabs API
- Real-time Gaussian Splat rendering with runtime loading and splat layer support
- In-game VR/screen-space world browser and creator (WorldBrowserController)
- Editor importer for browsing and importing worlds as project assets

<br>

:warning: Setup Notes
* **Unity Version:**  6000.2.10f1 recommended
* **Render Pipeline:**  URP required
* **Graphics API:** D3D11 is NOT supported - use D3D12/Vulkan (Windows), Metal (Mac), or Vulkan (Android/Quest)
* **API Key:**  Obtain from WorldLabs and place in a .env file at the project root
* **Render Graph:**  Enable "Compatibility Mode (Render Graph disabled)" in Project Settings > Graphics
* **XR:**  Set OpenXR Render Mode to Multi-pass for VR builds
* **Meta Quest:**  Adding a Camera Rig from "Meta Building Blocks" may force D3D11 - switch back to Vulkan manually


#### GitHub: 👉 [WorldLabs Unity Kit](https://github.com/nigelhartman/worldlabs_unity) 

---

## 3. WorldLabs Unreal Kit

🎯 An Unreal Engine 5.5 template project for rendering Gaussian splats using the XVERSE XV3DGS plugin.
<br>

- Import .ply splat files directly via the XV3DGS editor tab - produces a converted splat and a Blueprint ready to place in your level
- Includes a training tool to convert .mp4 video into .ply splat files (requires CUDA 11+)

<br>

:warning: Setup Notes
* **Engine Version:** Unreal Engine 5.5 only - XV3DGS is not compatible with later versions
* **Plugin:**  Included under Plugins/XV3dGS, enabled automatically
* **Hardware Ray Tracking:** Make sure it is disables in project setting, due to incompatibility with XV3DGS


#### GitHub: 👉 [WorldLabs Unreal Kit](https://github.com/V4C38/sensai-unreal-worldmodels)  

---

## 4. Acknowledgements & Credits
* Join the [Worlds in Action Hack](https://sensaihack.com) and connect with a community of creators and innovators.
* Check out our [SensAI Knowledge Hub](https://xrbootcamp.notion.site/SensAI-Knowledge-Hub-21f0095e34d880ec9826d9749ae56619) for curated learning use cases and inspiration across AI, XR, and robotics.
* Thanks to [Nigel Hartman](https://www.linkedin.com/in/nigelhartman/)  for the WorldLabs Unity package - a great source of AI & XR insights.
* Big thanks to [Johannes Tscharn](https://x.com/JohannesTscharn) for the Unreal and WebXR world model templates - check out his work for more cool XR projects.

Powered by [SensAI Hackademy](https://sensaihackademy.com)

---

## 5. License
📜 By downloading and using these kits, you agree to the [License Terms](./LICENSE).


---

## 6. Contact
✉️ Have questions, suggestions, or feedback? We’d love to hear from you!
Reach out to us at hello@sensaihack.com

<br>

---
