# Changelog

All notable changes to the Car Mount Phone Holder Generator are documented here.

## [5.4] - 2026-08-15

### Added
- Buy Me a Coffee support button below the language selector.
- Buy Me a Coffee support button below the main export controls.

### Changed
- Project branding renamed to **Car Mount Phone Holder Generator**.
- Previous branded holder terminology replaced with **Car mount phone holder** terminology.
- Repository naming updated to `car-mount-phone-holder-generator`.
- Generated STL and OpenSCAD filenames now use the `car_mount_phone_holder_` prefix.
- Car-mount configuration wording is more generic while retaining Brodit/AMPS compatibility references where technically relevant.
- Existing language preference is migrated from the previous local-storage key so returning users keep their selected language.

## [5.3] - 2026-08-15

### Added
- Collapsible configuration sections 1–4.
- Collapsible OpenSCAD code section.

### Changed
- English is now the default language for first-time users.
- The most recently selected language is still remembered.
- Configuration sections are expanded by default.
- OpenSCAD code is collapsed by default.

## [5.2] - 2026-08-15

### Added
- Samsung Galaxy FE presets:
  - Galaxy S20 FE 5G
  - Galaxy S21 FE 5G
  - Galaxy S23 FE
  - Galaxy S24 FE
  - Galaxy S25 FE
- Full English interface alongside Swedish.
- Language selector in the upper-right area of the interface.
- Browser persistence for the selected language.

## [5.1] - 2026-08-15

### Fixed
- Improved dropdown readability.
- Dropdown options now use dark text on a light background so unselected items remain legible in dark mode.

## [5.0] - 2026-08-15

### Added
- Full Plate and Half Plate holder-design options.
- Half Plate height calculated relative to the upper AMPS mounting holes.
- Integrated charging-connector dock.
- USB-C and Lightning starting profiles.
- User-defined charging connector body dimensions.
- Adjustable cable diameter, dock wall thickness, clearance and connector-to-phone distance.
- Additional Samsung Galaxy S models from S20 onward.

### Changed
- Bottom geometry can automatically adapt to the charging-connector housing height.

## [4.0] - 2026-08-15

### Added
- Fit-test-piece generator for bottom, middle and top sections.
- Separate fit-test STL/OpenSCAD export.
- Adjustable fit-test height.

### Changed
- Softer, more rounded holder design.
- Increased outer corner radius.
- Rounded rails, front lips and camera opening.
- Reworked bottom supports with recessed rounded support points.
- Removed the protruding outer lower corners.

## [3.0] - 2026-08-15

### Added
- Interactive 3D preview.
- Rotate, zoom and pan controls.
- Front, rear, side, top and isometric camera presets.
- Optional transparent phone model in the preview.
- Live model updates using the same geometry used for STL generation.

## [2.0] - 2026-08-15

### Added
- Direct STL export in the browser.
- OpenSCAD export retained.
- Multiple Brodit rear-plate presets.
- AMPS mounting options.
- Automatic charging-port opening.
- Automatic button-access zones.
- Adjustable button-access clearance.

## [1.0] - 2026-08-15

### Added
- Initial browser-based phone-holder generator.
- Phone-model presets.
- Custom phone dimensions.
- Case and printer-clearance adjustments.
- Brodit/AMPS mounting geometry.
- OpenSCAD generation.
