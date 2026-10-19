# Downtown Chapter 1A — parcel developability scenarios

An interactive Three.js viewer for the Downtown Community Plan Area. Open `index.html` through an HTTP server, or use the published GitHub Pages site. All JavaScript dependencies and geometry are local; no API key or external tracking is used.

## What is included

- 14,896 source parcel geometries, with 12,858 modeled scenarios and 2,038 unresolved parcels shown as flat gray context.
- Per-parcel PIN search, source zoning, form district, floor area, story count, height sensitivity, raw use permission and review flags.
- Form filters, context visibility, wireframe, top view, zoom and image export.
- A downloadable CSV of unresolved parcels. Gray context does not mean zero development potential.

## Interpretation

These are illustrative massing scenarios, not verified regulatory envelopes, entitlements, or achievable housing yields. Existing parcel boundaries are fixed scenario constraints; no lot assembly is assumed. City Hall height restrictions are intentionally excluded at the user's direction.

Each district's available FAR, coverage and story controls inform the scenarios. No bonus eligibility is assumed. HB5 previews use a ten-story scenario with smaller floorplates preserving FAR; the actual minimum-story rule depends on frontage portions and remains subject to applicability review. The story-height display uses 12- or 17-foot upper stories with source numeric ground-story minima included conservatively. These are floor-to-floor assumptions, not legally measured maximum building heights.

On 273 modeled LN1 parcels, five-foot primary-street setbacks are provisionally applied to frontages inferred using Article 14 criteria and street/alley geometry. Another inferred parcel has a sub-one-square-foot residual and is held for geometry review. Mapped primary-street overrides were unavailable, so these assignments remain conditional. Additional footprint insets allocate scenario floor area; they are not additional zoning setbacks.

Frontage/build-to, building width/breaks, amenity configuration, river and upper-story applicability, overlays, grade, use conditions and other restrictions remain unresolved where flagged. Source lookup matches and geometry checks do not certify zoning compliance. Special river setbacks are not inferred merely from distance to a river.

The 700 sq ft minimum dwelling size is a user-selected scenario assumption, separate from the district's density denominator. Gross floor area divided by 700 is only a theoretical upper bound before circulation, nonresidential allocations, density limits and use/program conditions. It is not an achievable unit count. `S` means Special Use Program; `--` means use not permitted. Full code conditions still apply.

## Provenance and checks

Source: the user's evaluated QGIS parcel/zoning joins, City Planning Chapter 1A district tables, official Downtown Community Plan boundary, and NavigateLA reference geometry. Source coordinates are EPSG:2229 (US survey feet), converted to local metres. The model uses a flat reference plane.

Every included batch was saved and independently reopened in Blender. ID, finite-coordinate, geometry, height, placement, FAR/coverage and assembly checks are retained in the companion project repository. Rendered detail review is sampled. The public geometry payload is SHA-256 checked before display.

Code references: [Article 14](https://zoning.lacity.gov/browse/14), [Form rules](https://zoning.lacity.gov/browse/2C), [Form districts](https://zoning.lacity.gov/browse/2B).

This viewer is a clean public subset of the project. It contains no original Git history, raw GIS databases, workstation credentials or private source files. Three.js is distributed under its included MIT license.

Sixteen provisionally modeled LN1 parcels cross the Downtown boundary. Their full parcel shapes are retained under the user-directed existing-parcel scenario, with an explicit boundary-review flag; no silent clipping or resolved Downtown edge treatment is claimed. These supplement the unresolved boundary cases shown as context.
