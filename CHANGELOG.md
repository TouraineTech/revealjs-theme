# Changelog

All notable changes to this theme are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.0] - 2026-11-08

### Added

- reveal.js 6 support. The theme still works with reveal.js 5.
- Automatic npm publishing from CI, with provenance attestation.

### Fixed

- The `end` slide no longer overflows the screen when it follows a `section` slide.
- Titles on `section` slides render above the decorative triangles.
- Footer documentation: the `.slide-footer.light` class does not exist, and the handle sits to the right of the logo.

### Changed

- The example and README load reveal.js 6.0.2, whose plugins now live under `dist/plugin/`.
- The Touraine Tech handle in the example is now `@tourainetech`.

## [1.0.0] - 2025-12-23

### Added

- Initial release: `cover`, `section`, `default`, `end` and `two-cols` layouts, footer with logo and handle, SVG TNT logo, utility classes.

[Unreleased]: https://github.com/TouraineTech/revealjs-theme/compare/v1.1.0...HEAD
[1.1.0]: https://github.com/TouraineTech/revealjs-theme/compare/7499cb3...v1.1.0
[1.0.0]: https://github.com/TouraineTech/revealjs-theme/commit/7499cb3
