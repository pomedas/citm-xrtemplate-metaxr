# CITM XR Template — Meta XR

A minimal Unity starter project for the **AR/VR course (804244 RAVJ) at CITM – UPC**.
It comes with the **Meta XR SDK** and **Building Blocks** already installed and configured,
so you can skip the setup and start building for Meta Quest from day one.

---

## What's inside

- Unity project configured for **Android / Meta Quest**
- **Meta XR All-in-One SDK** (Core, Interaction, Building Blocks…)
- A sample scene with a basic XR rig (camera + hands/controllers) ready to run
- Unity-friendly `.gitignore`

## Requirements

| Item | Version / notes |
|---|---|
| Unity | `TODO: e.g. 6000.0.xx LTS` — use **exactly** this version |
| Unity modules | **Android Build Support** (incl. OpenJDK and Android SDK & NDK Tools) |
| Meta XR SDK | `TODO: e.g. v7x` (already included in the project) |
| Headset | Meta Quest 2 / 3 / 3S / Pro, with **Developer Mode** enabled |
| PC (optional) | Windows + **Meta Quest Link** app, to test in Play Mode without building |

## Getting started

### 1. Get the project

Clone it (or click **Code → Download ZIP**):

```bash
git clone https://github.com/pomedas/citm-xrtemplate-metaxr.git
```

> 💡 For your own project, click **Use this template** / **Fork** on GitHub so you get your own repository.

### 2. Open it in Unity

1. Open **Unity Hub → Add → Add project from disk** and select the cloned folder.
2. Make sure it opens with the Unity version listed above.
3. The first import takes a few minutes (Unity rebuilds the `Library/` folder).
4. Open the sample scene in `Assets/Scenes/`.

### 3. Prepare the headset

1. Install the **Meta Horizon** app on your phone and pair the headset.
2. Enable **Developer Mode** (Headset settings → Developer Mode).
3. Connect the headset to the PC with a USB-C cable and accept **Allow USB debugging** inside the headset.

### 4. Run it

**Option A – Play Mode via Link (Windows only, fastest iteration)**
1. Open the **Meta Quest Link** app on the PC and connect the headset (cable or Air Link).
2. Press **Play** in Unity.

**Option B – Build to the headset**
1. **File → Build Profiles** (or *Build Settings*) → check that **Android** is the active platform.
2. Select your headset under **Run Device**.
3. Click **Build And Run**.

## Adding features with Building Blocks

Open **Meta → Tools → Building Blocks** and drag blocks into the scene, for example:

- **Camera Rig** – the XR camera and tracking space
- **Hand Tracking** / **Controller Tracking**
- **Grab Interaction**, **Ray Interaction**, **Poke Interaction**
- **Passthrough** – see the real world (mixed reality)
- **Room Model / Scene Mesh** – use your real room as geometry

Each block adds its dependencies automatically.

## Project health check

If something isn't working, open **Meta → Tools → Project Setup Tool** and click **Fix All**.
It checks and fixes the XR plug-in, Android settings, graphics API and other common issues.

## Troubleshooting

| Problem | Try this |
|---|---|
| Headset not shown in *Run Device* | Re-plug the cable, accept USB debugging in the headset, click **Refresh** |
| Black screen in Play Mode | Make sure Link is active and **Meta Quest Link** is set as the OpenXR runtime |
| Build errors about Android SDK/JDK | Reinstall the Android modules from Unity Hub with the version listed above |
| Pink materials | The render pipeline isn't configured — run the **Project Setup Tool** |
| Huge / slow repository | Never commit `Library/`, `Temp/`, `Logs/` or builds — the `.gitignore` already handles this |

## Useful links

- [Meta XR SDK for Unity – documentation](https://developers.meta.com/horizon/documentation/unity/)
- [Building Blocks](https://developers.meta.com/horizon/documentation/unity/bb-overview/)
- [Interaction SDK](https://developers.meta.com/horizon/documentation/unity/unity-isdk-interaction-sdk-overview/)
- [Enable Developer Mode on Quest](https://developers.meta.com/horizon/documentation/native/android/mobile-device-setup/)

---

Maintained by Pedro Omedas — CITM, Universitat Politècnica de Catalunya.
