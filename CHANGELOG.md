# Changelog

All notable changes to the Car Mount Phone Holder Generator are documented here.

## [5.6.6] - 2026-08-16

### Changed
- Cleaned up project documentation and source notes for the current Minimalist design.
- Updated related documentation files for consistency.

## [5.6.5] - 2026-08-16

### Fixed
- Realigned both Minimalist side clamps to the exact vertical band of the cross-bridge.
- Increased the cross-bridge/clamp band to 14 mm for a clearer and stronger phone-retaining contact area.
- Left and right clamps now use identical Y position, height and phone-cavity edge coordinates.
- Disabled automatic button cut-outs in Minimalist mode because device-specific cut-outs could remove one of the two compact side clamps.
- Disabled the button-access controls while Minimalist mode is selected to reflect that behaviour.
- Updated the 2D schematic to draw both clamps explicitly in the same band as the cross-bridge.

## [5.6.4] - 2026-08-16

### Fixed
- Rebuilt the Minimalist side supports from the proven standard-holder side-channel geometry.
- Removed the experimental outward X-offset entirely.
- Left and right side-wall inner faces now align exactly with the generated phone cavity boundaries.
- The selected phone clearance is therefore preserved automatically.
- Front retaining lips are connected directly to the side walls and extend only inward over the phone front.
- The short side channels overlap the Minimalist cross-bridge by approximately 6 mm for structural continuity.
- Updated JSCAD/STL, OpenSCAD and 2D schematic geometry consistently.

## [5.6.3] - 2026-08-16

### Fixed
- Fixed a 3D-preview runtime failure introduced in v5.6.2.
- Removed negative-axis JSCAD scaling from the Minimalist right-grip mirror operation.
- The right grip is now generated using directly mirrored coordinates instead.
- Left and right grip dimensions remain mathematically symmetric without relying on a negative transform.
- Improved internal 3D-preview error reporting for easier diagnosis if a future render error occurs.

## [5.6.2] - 2026-08-16

### Fixed
- Fixed asymmetry in the Minimalist right-hand side grip.
- The right grip is now generated as an exact geometric mirror of the left grip around the holder centreline.
- The same mirrored construction is used in JSCAD/STL, OpenSCAD and the 2D schematic.
- This prevents the right grip from becoming differently oriented or offset for different phone dimensions.

## [5.6.1] - 2026-08-16

### Fixed
- Corrected the Minimalist side-grip orientation and placement.
- Replaced the inward full-depth shoulder blocks with dedicated outward-set C-shaped grips.
- Moved the load-bearing side walls slightly outside the phone cavity.
- Reduced the inward front-lip overlap so the grips do not extend as far over the phone.
- Kept several millimetres of direct overlap between the grip side walls and the cross-bridge for structural continuity.
- Updated the 2D schematic, JSCAD preview/STL geometry and OpenSCAD geometry consistently.

## [5.6.0] - 2026-08-16

### Changed
- Lowered the side grips in the Minimalist design.
- Added deep rounded shoulder blocks so the side grips overlap and structurally join the tapered central back instead of relying on a very small contact area.
- Brodit ball-joint centre hole is now automatically 2 mm larger in diameter than the upper and lower holes; the centre screw-head recess is also 2 mm larger.

### Added
- New **Two-piece cable clamp** charging mode.
- The holder receives an open cable cradle with side retention ribs.
- A separate U-shaped retaining clip is generated and printed beside the holder in the same STL/OpenSCAD model.
- Adjustable retaining-clip clearance and wall thickness.
- Small snap teeth on the separate clip to help retain it after installation.

## [5.5.0] - 2026-08-16

### Added
- New **Minimalist / Minimalistiskt** holder design.
- Minimalist geometry uses a tapered central spine, short upper side grips, an open upper rear area, and a centred lower support.
- New **Brodit ball joint / Brodit Kulled** back-mount option with three vertically centred screw holes.
- Adjustable ball-joint hole spacing, defaulting to 18 mm.
- 2D preview, interactive 3D preview, STL export and OpenSCAD export support the new Minimalist design and three-hole mounting pattern.

### Changed
- Version 5.5.0 is based on **v5.4.4 geometry**. The experimental lower-corner taper from v5.4.5 is not included.
- Minimalist mode automatically disables controls that do not apply to its fixed short-rail geometry.

## [5.4.4] - 2026-08-16

### Fixed
- Fixed the integrated charging-dock front-insertion opening.
- **Front opening for insertion** now changes the actual visible width of the front slot instead of only extending an already-through cut in depth.
- The insertion slot is cut through the complete front half of the charging dock, allowing the connector housing to be inserted and removed from the front.
- The dock status now shows the calculated front-opening width.

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
