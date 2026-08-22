# Changelog

All notable changes to the Car Mount Phone Holder Generator are documented here.

## [5.9.0] - 2026-08-21

### Added
- Added **Export settings** and **Import settings** for saving and restoring complete generator configurations as JSON files.
- Configuration files include all user-editable input/select/checkbox values, including phone/case dimensions, holder geometry, charging settings, Brodit/back-mount settings, fit-test options, preview options and language.
- Added configuration metadata with file-format version, generator version and export timestamp.
- Added phone brand/name metadata so imported phone selections can be resolved by model identity rather than relying only on the phone-list index.
- Import ignores settings that do not exist in the current generator and reports how many values were restored/ignored.
- Import rejects unsupported newer configuration-file formats with a clear status message.
- Imported values are restored directly without invoking phone defaults or automatic connector presets, preventing saved custom dimensions from being overwritten.

### Documentation
- Added configuration export/import documentation to README.
- Confirmed the GitHub Pages setup guide remains removed and the cover image remains at the top of README.md.

## [5.8.8] - 2026-08-21

### Changed
- Changed the **Embedded dock** forward offset from **2.0 mm to 1.0 mm** from the rear-wall reference.
- The connector pocket, sleeve body and locking-screw path all follow the same 1.0 mm position.
- Applied consistently to the interactive 3D preview, STL export and OpenSCAD export.

### Documentation
- Updated README and in-app wording for the new 1.0 mm offset.
- Confirmed the GitHub Pages setup guide remains removed and the cover image remains at the top of README.md.

## [5.8.7] - 2026-08-21

### Fixed
- Corrected the default **Brodit ball-joint 3-hole spacing** from 18.0 mm to **20.5 mm centre-to-centre between adjacent holes**.
- The upper-to-centre and centre-to-lower distances are each 20.5 mm, giving 41.0 mm centre-to-centre between the two outer holes.
- Updated both the UI default and the geometry fallback value, so the same spacing is used by the interactive 3D preview, STL export and OpenSCAD export.
- The spacing remains manually adjustable for ball-joint variants with different dimensions.

### Documentation
- Updated the Brodit ball-joint description in README and the in-app help text with the 20.5 mm default.
- Confirmed the GitHub Pages setup guide remains removed and the cover image remains at the top of README.md.

## [5.8.6] - 2026-08-20

### Fixed
- Fixed the **Embedded bottom dock** sleeve not being physically connected to the holder in some configurations, particularly the default Minimalist design.
- Replaced the embedded dock's generic charging-opening gap with a dedicated gap derived from the connector pocket and sleeve-wall dimensions.
- The lower left and right supports now overlap the embedded sleeve side walls by approximately 1.0–1.6 mm while keeping the connector pocket clear.
- Added a rear attachment web from the shifted sleeve into the holder spine/back for an additional structural connection.
- The rear attachment web terminates inside the sleeve rear wall and does not block the connector insertion pocket.
- Applied the same geometry to the interactive 3D preview, STL export and OpenSCAD export.

### Documentation
- Updated README with the embedded dock attachment method.
- Preserved the v5.8.5 language/3D-preview fix unchanged.
- Confirmed the GitHub Pages setup guide remains removed and the cover image remains at the top of README.md.

## [5.8.5] - 2026-08-20

### Fixed
- Reverted the language-switch implementation to the stable **v5.8.2 code base** before applying the language fix again.
- Fixed the 3D-preview regression caused by the v5.8.3/v5.8.4 refactor accidentally removing the `plateSpec()` function used by `calc()`.
- Language switching is now intentionally minimal: it only translates interface text, refreshes the phone source label and rebuilds previews from the values already present in the form.
- Language switching no longer calls `loadPhone()` and therefore does not overwrite custom phone dimensions.
- Language switching does not reapply automatic connector presets.
- Phone/contact defaults are initialized once on first page load and still reload normally when the user deliberately selects another phone.

### Documentation
- Updated README to describe the non-destructive language switching behaviour.
- Confirmed the GitHub Pages setup guide remains removed and the cover image remains at the top of README.md.

## [5.8.2] - 2026-08-20

### Changed
- Made **Minimalist / Minimalistiskt** the first and default holder design.
- Removed **Dock – hold the charging connector / Docka – håll fast laddkontakten** completely from the generator.
- Removed the old open-front dock's dedicated controls, geometry branches, OpenSCAD modules, STL/JSCAD logic and export filename handling.
- Charging options are now:
  - Embedded bottom dock with locking screw
  - Two-piece screw-on L-shaped cable clamp
  - Open charging cut-out
- Removed obsolete **Front opening for insertion** and **Extra dock forward grip** controls because they only applied to the deleted dock design.

### Documentation
- Updated README to show Minimalist as the default design.
- Removed documentation for the deleted open-front dock.
- Confirmed the GitHub Pages setup guide remains removed and the cover image remains at the top of README.md.

## [5.8.1] - 2026-08-20

### Changed
- Made **Embedded dock – bottom-insert connector + locking screw** the first and default charging mode.
- Shifted the embedded dock's connector pocket **2.0 mm forward from the rear wall** to improve alignment between the retained cable connector and the phone charging port.
- Shifted the embedded sleeve body and front locking-screw path by the same 2.0 mm so wall thickness and locking-screw alignment remain consistent.
- The change is applied consistently to the interactive 3D preview, STL export and OpenSCAD export.
- Added the 2.0 mm forward-offset information to the charging-status summary.

### Documentation
- Updated README and charging-mode help text to identify the embedded dock as the default option and document its 2.0 mm forward offset.
- Confirmed the GitHub Pages setup guide remains removed and the cover image remains at the top of README.md.

## [5.8.0] - 2026-08-20

### Added
- Added a new **Embedded dock – bottom-insert connector + locking screw** charging mode.
- The new dock builds a rectangular connector sleeve directly through the lower holder construction.
- The charging connector is inserted from underneath instead of from the front.
- Added an adjustable front locking-screw pilot hole, defaulting to Ø2.7 mm.
- The locking-screw height is calculated automatically to press against the middle region of the connector's plastic housing.
- The embedded dock uses a thicker front wall around the locking-screw hole for improved support length.

### Changed
- Removed the U-shaped cable cut-out from the front plate of the separate L-shaped cable clamp.
- The L-cover front plate is now solid except for its two screw holes.
- The cable passage remains only through the lower under-tab, where the cable actually requires clearance.
- Kept the existing open-front charging dock as a separate charging mode.

### Documentation
- Updated README and charging-mode help text for all connector-retention options.
- Added guidance that the locking screw should press against the plastic connector housing, not the electrical/metal connector.
- Confirmed the GitHub Pages setup guide remains removed and the cover image remains at the top of README.md.

## [5.7.2] - 2026-08-20

### Fixed
- Corrected screw-hole alignment for the separate L-shaped cable clamp.
- The generator now accounts for the physical thickness of the under-tab that slides underneath the cable mount.
- Holder pilot holes remain at their cradle-relative mounting height.
- Screw clearance holes in the loose L-cover are automatically shifted upward by exactly the configured **L-cover thickness**.
- Increased the loose cover's total height by the same offset so its upper edge remains correctly positioned after assembly.
- Extended the front cable notch by the same offset so the notch remains aligned with the cable cradle.
- The compensation updates automatically whenever **L-cover thickness** changes.

### Documentation
- Updated README and charging-mode help text to explain the automatic L-cover mounting-height compensation.
- Confirmed the GitHub Pages setup guide remains removed and the cover image remains at the top of README.md.

## [5.7.1] - 2026-08-20

### Fixed
- Rebuilt the fixed charging dock as a true U-shaped connector cradle with a permanent front insertion opening.
- The connector can now be inserted directly from the front without relying on a boolean slot through a closed outer block.
- The rear portions of the side cheeks remain full thickness while the front portions open wider according to **Front opening for insertion**.
- Retained the adjustable **Extra dock forward grip** depth and added a small lower support shelf without closing the front opening.

### Changed
- Redesigned the separate part for the two-piece charging option as an **L-shaped screw-on cable clamp**.
- The lower tongue of the L-cover slides underneath the cable mount while the upright/front plate is secured using the existing two screws.
- Added an adjustable **Under-tab length**, defaulting to 6.0 mm.
- Added a cable notch through both the front plate and the lower tongue so the cable is not trapped or pinched.
- The L-cover is generated beside the holder in STL/OpenSCAD exports and is oriented with its front face flat for straightforward printing.

### Documentation
- Updated README and charging-mode descriptions for the U-shaped dock and L-shaped cable clamp.
- Removed the GitHub Pages setup guide from the repository package while retaining the direct live-generator link.
- Confirmed the cover image remains at the top of README.md.

## [5.7.0] - 2026-08-20

### Changed
- Redesigned both integrated charging-connector retention options.
- The fixed charging dock now extends farther toward the front of the connector housing so the two side cheeks wrap around and support more of the cable connector.
- Added an adjustable **Extra dock forward grip** setting, defaulting to 3.0 mm.
- The dock insertion slot now begins near the connector housing's front face instead of cutting away the full front half of the dock, leaving longer side supports.

### Replaced
- Replaced the previous two-piece snap-fit cable clamp with a **two-piece screw-on protective cable cover**.
- The new system uses an open integrated cradle, two screw bosses with pilot holes, and a separately printed front cover.
- The cover includes a bottom cable notch and two screw clearance holes.
- Default dimensions are aimed at M3 hardware, with adjustable cover thickness, cable-notch clearance, screw clearance-hole diameter and holder pilot-hole diameter.
- The separate protective cover is included beside the holder in STL and OpenSCAD exports, including bottom fit-test exports.

### Documentation
- Updated the README charging section and current version information for the new charging-retention designs.

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
