# Maia SDR ADALM Pluto firmware changelog

All notable changes to this project will be documented in this file.

Semantic versioning for the firmware image is based on the user-facing
features. A major version change involves new user features. There might be
changes in Maia SDR that cause a major version change because of API changes but
only cause a minor version change in the firmware image because from the point
of view of the user the features have not changed significantly.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.3.1] - 2023-09-03

### Changed

- Update Maia SDR to v0.5.1. Fixed SigMF formatting. Updated Rust dependencies.

## [0.3.0] - 2023-07-08

### Added

- Update Maia SDR to v0.5.0. Added Support for Pluto+.

## [0.2.1] - 2023-06-10

### Changed

- Update Maia SDR to v0.3.2. Updated Rust dependencies.

## [0.2.0] - 2023-04-08

### Changed

- Update base ADI Pluto firmware to v0.37.
- Update Maia SDR to v0.3.0. Includes new recording options and inferno waterfall colormap.

## [0.1.2] - 2023-03-18

### Changed

- Updated Maia SDR to v0.2.0. The main change is the adaptive vertical size of the waterfall.

## [0.1.1] - 2023-02-14

### Fixed

- Problems with Pluto rev. C device tree (see [issue #2](https://github.com/maia-sdr/plutosdr-fw/issues/2)).

## [0.1.0] - 2023-02-11

Initial release of the Maia SDR ADALM Pluto firmware. This corresponds to the
[default ADI firmware v0.35](https://github.com/analogdevicesinc/plutosdr-fw/releases/tag/v0.35).

[unreleased]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.3.1...HEAD
[0.3.1]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.3.0...maia-sdr-v0.3.1
[0.3.0]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.2.1...maia-sdr-v0.3.0
[0.2.1]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.2.0...maia-sdr-v0.2.1
[0.2.0]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.1.2...maia-sdr-v0.2.0
[0.1.2]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.1.1...maia-sdr-v0.1.2
[0.1.1]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.1.0...maia-sdr-v0.1.1
[0.1.0]: https://github.com/maia-sdr/plutosdr-fw/releases/tag/maia-sdr-v0.1.0
