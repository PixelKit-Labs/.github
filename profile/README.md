<p align="center">
  <img src="https://raw.githubusercontent.com/PixelKit-Labs/pixelkit-sdk/master/PixelKit_readme.jpg" alt="PixelKit" width="300">
</p>

<h1 align="center">PixelKit</h1>

<p align="center">
  PixelKit is an SDK for building Expo and React Native applications on Google Pixel devices.
  It provides typed React hooks for device sensors, radios, secure hardware, camera and audio,
  display and power telemetry, haptics, on-device AI, and Cloud AI.
</p>

```bash
npx expo install @pixelkit-labs/sdk @pixelkit-labs/native
```

```tsx
import { useCPU, useGemini } from '@pixelkit-labs/sdk';
import { useGeminiNano } from '@pixelkit-labs/sdk/mlkit';
```

## Repositories

| | |
| :--- | :--- |
| **[pixelkit-sdk](https://github.com/PixelKit-Labs/pixelkit-sdk)** | The SDK and the two Kotlin Expo Modules. 32 hooks. |
| **[pixelkit-template](https://github.com/PixelKit-Labs/pixelkit-template)** | A working Expo app wired to every hook. Press **Use this template** to start. |
| **[pixelkit-docs](https://github.com/PixelKit-Labs/pixelkit-docs)** | Source of the [documentation site](https://pixelkit-labs.github.io/pixelkit-docs/), and the contract the SDK is checked against in CI. |
| **[pixelkit-cli](https://github.com/PixelKit-Labs/pixelkit-cli)** | `pixelkit doctor`, for when a reading comes back empty and you want to know why. |

## Packages

| Package | What it is |
| :--- | :--- |
| [`@pixelkit-labs/sdk`](https://www.npmjs.com/package/@pixelkit-labs/sdk) | The hooks, types, design system and observability layer |
| [`@pixelkit-labs/native`](https://www.npmjs.com/package/@pixelkit-labs/native) | Kotlin module for telemetry and actuators. No third-party dependencies. |
| [`@pixelkit-labs/mlkit`](https://www.npmjs.com/package/@pixelkit-labs/mlkit) | Kotlin module for Gemini Nano and ML Kit. Opt-in, because it adds 19 artifacts to your APK. |
| [`@pixelkit-labs/cli`](https://www.npmjs.com/package/@pixelkit-labs/cli) | `pixelkit doctor` |

## Before you start

**It needs a development build.** `npx expo run:android`, or an EAS development profile. PixelKit
cannot run in Expo Go: reading a thermal sensor takes native code compiled into the app, and Expo Go
only contains the native code Expo shipped.

It degrades rather than fails on other hardware: 13 of the 32 hooks are pure Expo and JavaScript and
work on any Android device, and the rest report `unsupported` where the silicon is not there.

<p align="center">
  <a href="https://pixelkit-labs.github.io/pixelkit-docs/">Documentation</a>
  &middot;
  <a href="https://github.com/PixelKit-Labs/pixelkit-template">Start from the template</a>
  &middot;
  <a href="https://github.com/PixelKit-Labs/pixelkit-sdk/issues/new?labels=bug">Report a bug</a>
</p>
