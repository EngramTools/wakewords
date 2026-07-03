# wakewords

Public hosting for tele custom microWakeWord models (ESPHome fetches raw URLs).

- hey_tele: recall 99.94%, ambient_faph 0.931, cutoff 0.06, window 6 (2026-07-03)

## Runtime model swap

Devices flashed with runtime-model support (e.g.
[TaterTotterson/microWakeWords](https://github.com/TaterTotterson/microWakeWords)
Voice PE firmware) expose a text entity in Home Assistant named
**"microWakeWord Model URL"**. Paste this repo's raw URL into that entity to
switch the device's active wake word without a firmware rebuild:

```
https://raw.githubusercontent.com/EngramTools/wakewords/main/hey_tele.json
```

The device downloads, validates, and stores the model on-device, then
reloads automatically.
