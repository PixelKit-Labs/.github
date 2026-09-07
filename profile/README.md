<p align="center">
  <a href="https://github.com/PixelKit-Labs/pixelkit">
    <img src="https://raw.githubusercontent.com/PixelKit-Labs/pixelkit/master/PixelKit_readme.jpg" alt="PixelKit" width="640">
  </a>
</p>

<h1 align="center">Google Pixel hardware as React hooks.</h1>

<p align="center">
  32 typed hooks that give an Expo app real access to the device: per-core CPU frequencies straight
  from cpufreq, battery temperature from the fuel gauge, the camera and microphone, every radio from
  NFC to ultra-wideband, biometrics and the hardware keystore, and Gemini Nano running on-device.
  <br><br>
  Every value tells you where it came from. A reading the hardware cannot give you comes back
  <code>null</code> instead of a guess, so <strong>you always know whether a number is real</strong>.
</p>

<p align="center">
  <a href="https://github.com/PixelKit-Labs/pixelkit#readme">Get started</a>
  &middot;
  <a href="https://github.com/PixelKit-Labs/pixelkit/tree/master/docs">Read the docs</a>
  &middot;
  <a href="https://github.com/PixelKit-Labs/pixelkit/issues/new?labels=bug">Report a bug</a>
</p>

## Repositories

- **[pixelkit](https://github.com/PixelKit-Labs/pixelkit)** — the SDK, two Kotlin Expo Modules, the `pixelkit doctor` CLI, the docs, and the demo app that proves it all works on real hardware.

**Android only.** Build it onto your phone with `npx expo run:android` - one command, a few minutes
the first time. It will not run in Expo Go: reading a thermal sensor takes native code compiled into
the app, and Expo Go only ships the native code Expo put in it.