# SensAI World Model Kits 🌍

This is a collection of world model kits for building immersive world model experiences across WebXR, Unity and Unreal Engine.

## 🎥 Tutorials & Demos

[Watch the playlist](https://www.youtube.com/playlist?list=PLNJ7-FU87tTY)
▶️ Explore step-by-step tutorials and demos

<img width="734" alt="image" src="https://github.com/user-attachments/assets/066aeb38-a90e-4cd4-8194-c3a2ad826a29" />


---

## 📝 Table of Contents

1. [Splat Analyzer](#1-splat-analyzer)
2. [WorldLabs WebXR Kit](#2-worldlabs-webxr-kit) 
3. [WorldLabs Unity Kit](#3-worldlabs-unity-kit) 
4. [WorldLabs Unreal Kit](#4-worldlabs-unreal-kit)  
5. [Acknowledgements & Credits](#5-acknowledgements--credits)  
6. [License](#6-license)
7. [Contact](#7-contact)


## Overview

## 1. Splat Analyzer

Detects objects in 3D Gaussian Splats using Claude skills and OWLv2 - no manual annotation or training.

Upload a `.ply` or `.spz` file, prompt it with object names (e.g. "chair, table, monitor"), and get 3D bounding boxes ready for interactions in WebXR, games, or robotics.

### Quickstart
1. Clone the repo: `git clone https://github.com/nigelhartman/splat_analyzer`
2. Enter the directory: `cd splat_analyzer`
3. Run locally (Mac Apple Silicon or NVIDIA GPU, 8GB+ VRAM) or use the hosted web app + REST API
4. Upload your splat file and prompt with the object names you want detected

### Description
Pipeline: renders views → detects objects with OWLv2 → converts 2D detections into 3D boxes. Works with standard Gaussian Splats, including World Labs and XGRIDS exports.

### Setup Notes
- **Mac**: Metal support, no NVIDIA GPU needed
- **PC/Linux**: CUDA GPU required (8GB+ VRAM recommended)
- Ensure splat orientation is correct before running


#### GitHub: 👉 [Splat Analyzer](https://github.com/nigelhartman/splat_analyzer)

<img width="540px" alt="SplatanalyzerCompressed" src="https://github.com/user-attachments/assets/74c5a814-18df-4d8c-974c-a6cc4563ba17" />



---

## 2. WorldLabs WebXR Kit

A WebXR template for building immersive world model experiences with Gaussian splats, spatial UI, and locomotion - runs in any WebXR-capable browser.

### Quickstart
1. Clone the repo: `git clone https://github.com/V4C38/sensai-webxr-worldmodels`
2. Enter the directory: `cd sensai-webxr-worldmodels`
3. Install dependencies (Node ≥ 20.19.0 required)
4. Load a local or remote `.spz`/`.ply` splat and launch in a WebXR-capable browser

### Description
Renders splats using SparkJS 2.0 with GPU-accelerated fly-in/fly-out animations. Includes Level-of-Detail (LoD) support to adjust splat quality by distance and maintain stable framerates on headsets. Built on IWSDK for locomotion, grabbing, spatial UI, and XR session management.

### Setup Notes
- **Prerequisites**: Node ≥ 20.19.0 and a WebXR-capable browser
- **Splat Files**: Keep large splat files outside the repo and load via URL


#### GitHub: 👉 [WorldLabs WebXR Kit](https://github.com/V4C38/sensai-webxr-worldmodels) 

<img src="https://github.com/user-attachments/assets/c91ccbd8-23dd-473b-9515-86ca40365e50" alt="WorldLabsWebXRKit" width="540px">

---

## 3. WorldLabs Unity Kit

A Unity package for generating and rendering 3D Gaussian Splatting scenes using the WorldLabs API, with a built-in runtime VR world browser.

### Quickstart
1. Clone the repo: `git clone https://github.com/nigelhartman/worldlabs_unity`
2. Open the project in Unity 6000.2.10f1 (recommended)
3. Add your WorldLabs API key to a `.env` file at the project root
4. Generate a scene from a text prompt via the WorldLabs API

### Description
Real-time Gaussian Splat rendering with runtime loading and splat layer support. Includes an in-game VR/screen-space world browser and creator (WorldBrowserController), plus an editor importer for browsing and importing worlds as project assets.

### Setup Notes
- **Unity Version**: 6000.2.10f1 recommended
- **Render Pipeline**: URP required
- **Graphics API**: D3D11 is NOT supported - use D3D12/Vulkan (Windows), Metal (Mac), or Vulkan (Android/Quest)
- **Render Graph**: Enable "Compatibility Mode (Render Graph disabled)" in Project Settings > Graphics
- **XR**: Set OpenXR Render Mode to Multi-pass for VR builds
- **Meta Quest**: Adding a Camera Rig from "Meta Building Blocks" may force D3D11 - switch back to Vulkan manually


#### GitHub: 👉 [WorldLabs Unity Kit](https://github.com/nigelhartman/worldlabs_unity) 

<img src="https://github.com/user-attachments/assets/b151d0c7-90e7-496c-a21f-804151f25466" alt="WorldLabsUnityKit" width="540px">

---

## 4. WorldLabs Unreal Kit

An Unreal Engine 5.5 template for rendering Gaussian splats using the XVERSE XV3DGS plugin.

### Quickstart
1. Clone the repo: `git clone https://github.com/V4C38/sensai-unreal-worldmodels`
2. Open the project in Unreal Engine 5.5 (XV3DGS is not compatible with later versions)
3. Import a `.ply` splat file via the XV3DGS editor tab - produces a converted splat and a placeable Blueprint
4. To convert video instead, use the included training tool (`.mp4` → `.ply`, requires CUDA 11+)

### Description
Plugin is included under `Plugins/XV3dGS` and enabled automatically.

### Setup Notes
- **Engine Version**: Unreal Engine 5.5 only - XV3DGS is not compatible with later versions
- **Hardware Ray Tracing**: Make sure it is disabled in project settings, due to incompatibility with XV3DGS


#### GitHub: 👉 [WorldLabs Unreal Kit](https://github.com/V4C38/sensai-unreal-worldmodels)  

<img src="https://github.com/user-attachments/assets/31b9611d-ce9b-4651-ad35-e5e891d1699e" alt="WorldLabsUnrealKit" width="540px">

---

## 5. Acknowledgements & Credits
* Check out our [Master SensAI Kits](https://github.com/SensAIHackademy/SensAIKits) for a full collection of context-aware AI tools for Unity and Meta XR.
* Explore [SensAI PICO Kits](https://github.com/SensAIHackademy/SensAI-PICO-Kits) for world model & voice-command templates for PICO.
* Check out [SensAI Hacks](https://sensaihack.com) and connect with a community of creators and innovators.
* Visit our [SensAI Knowledge Hub](https://xrbootcamp.notion.site/SensAI-Knowledge-Hub-21f0095e34d880ec9826d9749ae56619) for curated learning resources and inspiration.
* Thanks to [Nigel Hartman](https://www.linkedin.com/in/nigelhartman/) and [Johannes Tscharn](https://x.com/JohannesTscharn) for the kits.

Powered by [SensAI Hackademy](https://sensaihackademy.com)

---

## 6. License
📜 By downloading and using these kits, you agree to the [License Terms](./LICENSE).


---

## 7. Contact
✉️ Have questions, suggestions, or feedback? We'd love to hear from you!
Reach out to us at hello@sensaihack.com

<br>

---
