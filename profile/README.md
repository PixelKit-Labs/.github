<p align="center">
  <a href="https://github.com/PixelKit-Labs/pixelkit">
    <img src="https://raw.githubusercontent.com/PixelKit-Labs/pixelkit/master/PixelKit_readme.jpg" alt="PixelKit" width="640">
  </a>
</p>

<h1 align="center">Google Pixel hardware as React hooks.</h1>

<p align="center">
  CPU clocks and thermal headroom, the camera, the microphone, every radio from NFC to
  ultra-wideband, the fingerprint sensor and the keystore, and Gemini running on the phone itself.
  <br><br>
  <strong>Nothing is simulated.</strong> A reading that cannot be taken is <code>null</code>, never
  a plausible default.
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

Android only, and it needs a development build: the hooks talk to native modules, so Expo Go can
never run them.
