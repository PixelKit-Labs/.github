## PixelKit

**Google Pixel hardware and on-device AI as React hooks.** Nothing is simulated.

```tsx
const cpu = useCPU();
<MetricCard label="Big core" value={cpu.cores[0]?.curMHz} unit="MHz" source={cpu.source} />
```

Every hook returns `source: 'hardware' | 'derived' | 'unavailable'`. There is deliberately no
`simulated` member, so a fabricated reading is not representable in the type system. A value that
cannot be read is `null`, renders as an em dash, and the control that depends on it refuses rather
than pretending. If a reading cannot be taken for real, the honest answer is a blank — not a
plausible default.

### Repositories

| | |
| :--- | :--- |
| **[pixelkit](https://github.com/PixelKit-Labs/pixelkit)** | The SDK: 32 hooks for silicon telemetry, sensors, radios, security and Gemini. Two Kotlin Expo Modules, a design system, and an observability layer. Also the demo app that proves all of it works on real hardware. |

### Packages

| Package | What it is |
| :--- | :--- |
| `pixelkit` | The hooks, the components and the theme |
| `@pixelkit/native` | Kotlin Expo Module for telemetry and actuators. Zero third-party dependencies. |
| `@pixelkit/mlkit` | Kotlin Expo Module for on-device ML Kit and Gemini Nano. Opt-in, because it adds 19 ML Kit artifacts to your APK. |
| `@pixelkit/cli` | `pixelkit doctor` — tells you why a reading is unavailable instead of leaving you guessing |

### Before you start

**Android only**, and it **cannot run in Expo Go** — the hooks talk to Kotlin Expo Modules that have
to be compiled in, so you need a development build. Most of it is Pixel-specific: on other hardware
the generic hooks work and the rest report `unavailable`, which is the design behaving correctly
rather than a bug.

MIT.
