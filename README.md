# Ape42 Taxi Speed Gauge

A custom gauge for [Lorby Axis and Ohs (AAO)](https://www.axisandohs.com/) that displays the aircraft's current ground speed in knots during taxi operations in Microsoft Flight Simulator 2020/2024.

## Features

- Displays ground speed as `Speed: XX.X kts` with one decimal place
- Automatically **hides** when the aircraft exceeds 30 knots (runway roll / airborne)
- Automatically **reappears** when speed drops below 28 knots (hysteresis prevents flickering)
- Always hidden when the aircraft is airborne (`SIM ON GROUND = 0`)

## Visibility Logic

| Condition | Gauge |
|---|---|
| Airborne | Hidden |
| Ground speed > 30 kts | Hidden |
| Ground speed 28–30 kts | Keeps previous state |
| Ground speed < 28 kts | Visible |

## Installation

1. Download the latest `Ape42-Taxispeed-vX.X.zip` from the [Releases](../../releases) page.
2. Extract the `Ape42-Taxispeed` folder into your AAO UserGauges directory:
   ```
   %USERPROFILE%\Documents\LorbyAxisAndOhs Files\UserGauges\
   ```
3. Restart AAO and add the gauge **Ape42 Taxispeed** to your panel layout.

## Files

```
Ape42-Taxispeed/
├── Ape42Taxispeed.xml   # Gauge definition
└── 1024/
    └── background.png   # Gauge background image (378 × 64 px)
```

## Requirements

- [Lorby Axis and Ohs](https://lorby-si.webs.com/)
- Microsoft Flight Simulator 2020 or 2024

## License

See [LICENSE](LICENSE).
