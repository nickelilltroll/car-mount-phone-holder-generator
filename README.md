<h1 align="center">Car Mount Phone Holder Generator</h1>

<p align="center">
  A browser-based generator for customizable, 3D-printable phone holders for car mounts, including Brodit/AMPS mounting options.
</p>

<p align="center">
  <strong>Current version: 5.4</strong>
</p>

---

## About

Car Mount Phone Holder Generator makes it easy to create a phone holder adapted to a specific smartphone, protective case, charging cable and car-mount solution — without requiring advanced CAD knowledge. Brodit/AMPS mounting options are included.

The generator runs directly in a modern web browser and can create models for 3D printing.

The main application is contained in [`index.html`](index.html), which also makes the project suitable for hosting with GitHub Pages.

## Live Generator

After enabling **GitHub Pages** for this repository, the generator can be used directly in the browser without installation.

See [`GITHUB_PAGES.md`](GITHUB_PAGES.md) for the short setup guide.

## Features

### Phone presets

The generator includes predefined dimensions for a growing number of devices, including:

- Apple iPhone models
- Samsung Galaxy S-series from S20 and newer
- Samsung Galaxy FE models
- Google Pixel models
- Custom phone dimensions

### Holder designs

Choose between:

- **Full Plate** — full-height rear plate
- **Half Plate** — shortened design ending just above the upper mounting holes

### Adjustable fit and geometry

Customize:

- Phone width, height and thickness
- Protective case allowance
- Print tolerance / clearance
- Wall thickness
- Corner radius
- Rounded rails and supports
- Bottom support dimensions
- Camera clearance
- Button access
- Charging-port clearance

### Integrated Charging Dock

The holder can optionally secure a USB-C or Lightning charging connector in the bottom of the mount so the phone can connect to power when inserted.

Adjust:

- Connector body width
- Connector body thickness
- Connector body height
- Connector clearance
- Dock wall thickness
- Cable diameter
- Cable channel
- Distance between connector body and phone

Because charging cable housings vary between manufacturers, measuring the connector with a caliper before printing is recommended.

### Fit Test Pieces

Generate a smaller test section before printing the complete holder.

Available areas include:

- Bottom
- Middle
- Top

The bottom test piece is particularly useful for checking phone fit, case clearance and charging-connector alignment while using much less filament.

### Brodit Mounting

Supported options include:

- AMPS mounting pattern
- 42 × 50 mm mounting plate
- 100 × 50 mm extension plate
- Angled mounting plate
- Custom mounting plate dimensions
- Mounting without holes

Hole spacing, hole diameter, recesses, orientation and position can be adjusted manually.

### Interactive 3D Preview

Inspect the generated holder before export with:

- Rotate
- Zoom
- Pan
- Front view
- Rear view
- Side view
- Top view
- Isometric view
- Optional transparent phone preview

### Export

The generator supports:

- **STL export** for slicing and 3D printing
- **OpenSCAD export** for further modification

### Languages

The interface currently supports:

- English
- Swedish

English is the default for new users. The last selected language is remembered in the browser.

The main configuration sections can be collapsed individually, while the OpenSCAD code section starts collapsed by default.

---

## How to Use

1. Open the live GitHub Pages version or open `index.html` locally.
2. Select your phone model.
3. Adjust case dimensions or custom phone measurements if needed.
4. Choose **Full Plate** or **Half Plate**.
5. Adjust holder geometry and fit.
6. Select a Brodit mounting configuration.
7. Optionally enable the integrated charging dock.
8. Enter the dimensions of your charging connector if required.
9. Inspect the result in the interactive 3D preview.
10. Generate a fit test piece if needed.
11. Export the final model as STL.
12. Slice and print.

---

## 3D Printing Recommendations

Car interiors can become very hot, especially in direct sunlight. Materials with better temperature resistance than standard PLA are generally preferable.

Possible materials include:

- PETG
- ASA
- ABS

A starting clearance of approximately **0.2–0.3 mm** can be useful, but the correct value depends on printer calibration, filament, layer height, phone case and desired fit.

Use the built-in fit test feature before printing the full holder whenever possible.

---

## Project Structure

```text
car-mount-phone-holder-generator/
├── index.html
├── README.md
├── CHANGELOG.md
├── GITHUB_PAGES.md
├── LICENSE
├── TERMS.md
├── COMMERCIAL_LICENSE.md
├── THIRD_PARTY_NOTICES.md
├── .nojekyll
├── .gitignore
└── assets/
    └── screenshots/
        └── README.md
```

---

## Technology

The project uses:

- HTML
- CSS
- JavaScript
- JSCAD
- Three.js
- OpenSCAD-compatible model generation

No application server is required for normal use.

---

## Support the Project

If this generator is useful to you and you would like to support continued development:

<p align="center">
  <a href="https://www.buymeacoffee.com/lilltroll">
    <img src="https://img.buymeacoffee.com/button-api/?text=Buy%20me%20a%20coffee&emoji=&slug=lilltroll&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff" alt="Buy me a coffee">
  </a>
</p>

**Buy Me a Coffee:**  
https://www.buymeacoffee.com/lilltroll

Support helps fund:

- New phone profiles
- Additional Brodit mounting options
- Charging-dock improvements
- UI improvements
- Testing
- Continued development

---

## Commercial Use and Development

This project is **source available, not open source**.

Personal, non-commercial use is permitted only as described in the repository license.

Modification, further development, redistribution, hosting, integration, resale and commercial use require prior written permission unless a separate agreement explicitly grants those rights.

For commercial licensing or development permission, see [`COMMERCIAL_LICENSE.md`](COMMERCIAL_LICENSE.md) and contact the project owner through the official GitHub repository/profile or:

https://www.buymeacoffee.com/lilltroll

A donation does **not** grant commercial or development rights.

---

## Generated Models

Generated STL/OpenSCAD models may be used for personal, non-commercial purposes as described in [`LICENSE`](LICENSE) and [`TERMS.md`](TERMS.md).

Selling printed holders, selling generated model files, operating a paid customization/printing service or other commercial use requires separate permission.

---

## Contributions and Feedback

Bug reports, feature suggestions and requests for additional phone models are welcome.

Because this is a source-available project rather than an open-source project, please obtain permission before submitting or publishing source-code modifications.

Useful feedback includes:

- Incorrect phone dimensions
- Missing devices
- Print-fit issues
- Charging-dock fit reports
- Brodit mounting suggestions
- Browser compatibility issues
- UI suggestions

---

## License

**Copyright © 2026 Niklas Forsgren. All rights reserved.**

See:

- [`LICENSE`](LICENSE)
- [`TERMS.md`](TERMS.md)
- [`COMMERCIAL_LICENSE.md`](COMMERCIAL_LICENSE.md)
- [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md)

Third-party libraries remain subject to their own licenses.

---

## Disclaimer

This is an independent project and is not affiliated with, sponsored by, approved by or endorsed by Brodit AB, Apple Inc., Samsung Electronics, Google LLC or other device manufacturers.

Brodit and other product names and trademarks belong to their respective owners.

Phone, case, cable and mounting dimensions may vary. Always verify dimensions, print quality, mounting security and safe placement before using a printed holder in a vehicle.

Use generated holders at your own risk.

---

## Roadmap

Possible future improvements include:

- More phone models
- Additional holder styles
- More Brodit mounting profiles
- More charging-connector presets
- Improved automatic button and camera positioning
- Saved user presets
- More languages
- Print-orientation recommendations
- Material estimates
- Additional fit-test geometries

---

## Changelog

See [`CHANGELOG.md`](CHANGELOG.md).
