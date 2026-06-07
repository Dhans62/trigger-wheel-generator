# Trigger Wheel Generator

**A free, browser-based tool to design and export trigger wheels (reluctor rings) for EFI/ECU systems.**

No installation. No server. Open the HTML file and use it directly.

---

## Live Demo

> **[Open Tool → dhans62.github.io/trigger-wheel-generator](https://dhans62.github.io/trigger-wheel-generator)**

---

## What is a Trigger Wheel?

A trigger wheel (also called a reluctor ring or crank wheel) is a toothed disc attached to a rotating shaft. A VR or Hall effect sensor reads the passing teeth and gaps to determine crankshaft position, RPM, and TDC — essential for EFI ignition timing.

Common patterns: **12-1, 24-1, 36-1, 60-2**

---

## Features

### Wheel Configuration
- Custom total teeth count (3–120)
- Custom missing teeth (gap) count
- Gap position adjustment (0–359°)
- Tooth width ratio (20–80%)
- Rotation direction: CW / CCW

### Dimensions
- Outer diameter (mm)
- Tooth height (mm)
- Bore diameter (mm)
- **Full Plate Mode** — input raw plate diameter, auto-calculates body disc OD
- Mounting holes with custom PCD, count, and diameter

### Display Options
- TDC marker
- Tooth numbers
- Degree marks
- Direction arrow
- Sensor reference position
- Bore hole toggle
- Light / Dark background

### Signal Waveform Simulator
- Real-time waveform preview based on current config
- Shows HIGH pulse, LOW gap, and GAP region widths in degrees

### Trigger Angle Calculator
- Input sensor offset from TDC
- Auto-calculates trigger angle for ECU input (Megasquirt, Speeduino, etc.)
- Shows tooth number after gap

### Calculated Values
- Tooth spacing (°)
- Gap angle (°)
- Actual tooth count
- Circumference (mm)
- HIGH pulse width (°)
- LOW gap width (°)
- Body disc OD (in Full Plate Mode)

### Export
| Format | Use Case |
|--------|----------|
| SVG | Laser cutting / waterjet — full precision |
| PNG Dark | Digital reference / documentation |
| PNG Light | Print-friendly reference |
| PDF / Print A4, A3, Letter | Physical template for machinist |

Print export includes:
- True 1:1 scale option (verify with ruler)
- Dimension annotations (OD, bore, tooth height, spacing)
- Title block with full specs and 10mm reference bar

---

## Presets

| Pattern | Common Application |
|---------|--------------------|
| 12-1 | Small motorcycles, DIY bench test |
| 24-1 | Mid-range EFI |
| 36-1 | Ford EDIS, popular aftermarket |
| 60-2 | OEM European (high resolution) |
| 36-2 | Aftermarket variant |
| 4-1 | Simple/legacy distributor |

---

## Recommended Settings (12-1 for DIY bench)

```
Total teeth     : 12
Missing         : 1
Tooth ratio     : 50% (optimal HIGH:LOW balance)
Outer diameter  : 100–120mm
Tooth height    : 4–5mm
Material        : Mild steel 2–3mm
```

> **Why 50% ratio?**
> At 50%, tooth HIGH = 15° and LOW gap = 15° for a 12-tooth wheel.
> The missing tooth creates a 45° LOW — a clean 3:1 ratio that ECUs reliably detect.

---

## How to Use

### Online (GitHub Pages)
Just open the link above. No install needed.

### Offline
```bash
git clone https://github.com/dhans62/trigger-wheel-generator.git
```
Then open `index.html` in any browser. Works fully offline.

---

## For Machinists / Fabricators

Export the SVG file and send directly to laser cutting or waterjet services.

The SVG contains:
- Accurate geometry based on entered dimensions
- All dimensions in mm (real scale)
- Center bore circle
- Mounting hole positions

For print template: use **Print / Export PDF** with Scale **1:1** and set printer margins to **None**.

---

## ECU Compatibility

Trigger angle output is compatible with:
- **Megasquirt** (MS1, MS2, MS3)
- **Speeduino**
- **RusEFI**
- **LibreEMS**
- Any ECU accepting missing-tooth crank patterns

---

## Roadmap

- [x] Basic wheel generator with presets
- [x] Full Plate Mode (raw material input)
- [x] Signal waveform simulator
- [x] Trigger angle calculator
- [x] Zoom / pan canvas
- [x] Export SVG, PNG, PDF/Print A4
- [x] Mounting holes
- [ ] Spoke & cutout patterns (weight reduction)
- [ ] Hole Manager (custom position & type)
- [ ] Custom body shape editor

---

## Contributing

Pull requests welcome. Please open an issue first to discuss what you want to change.

---

## License

MIT License — free to use, modify, and distribute.
See [LICENSE](LICENSE) for details.

---

## Author

**dhans62** — DIY automotive electronics enthusiast

If this tool helped your project, consider giving it a star on GitHub.

---

## Tags

`trigger-wheel` `reluctor-ring` `crank-sensor` `efi` `megasquirt` `speeduino` `rusefi` `ignition-timing` `automotive-diy` `vr-sensor` `hall-sensor` `missing-tooth` `12-1` `36-1` `60-2` `javascript` `svg` `no-install`
