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

## [0.7.0] - 2024-10-12

### Changed

- Update Maia SDR to v0.9.0. Adds spectrum display to waterfall.

## [0.6.1] - 2024-09-07

### Changed

- Update Maia SDR to v0.8.1. Updated to Amaranth v0.5.2 and updated dependencies.

## [0.6.0] - 2024-05-05

### Changed

- Update Maia SDR to v0.8.0. Adds DDC to select slice in input spectrum.

## [0.5.0] - 2024-02-23

### Changed

- Update Maia SDR to v0.7.0. Adds IQEngine to view IQ recordings done in the DDR.

## [0.4.2] - 2024-01-07

### Fixed

- Deleted axi_tdd from Pluto rev C device tree. Fixes boot crash in Pluto rev C.

## [0.4.1] - 2023-11-19

### Changed

- Update base ADI Pluto firmware to v0.38.
- Update Maia SDR to v0.6.1. Fixes SigMF formatting and waterfall crashes in large resolution.

## [0.4.0] - 2023-09-30

### Changed

- Update Maia SDR to v0.6.0. Add spectrometer peak detect mode.

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

[unreleased]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.7.0...HEAD
[0.7.0]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.6.1...maia-sdr-v0.7.0
[0.6.1]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.6.0...maia-sdr-v0.6.1
[0.6.0]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.5.0...maia-sdr-v0.6.0
[0.5.0]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.4.2...maia-sdr-v0.5.0
[0.4.2]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.4.1...maia-sdr-v0.4.2
[0.4.1]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.4.0...maia-sdr-v0.4.1
[0.4.0]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.3.1...maia-sdr-v0.4.0
[0.3.1]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.3.0...maia-sdr-v0.3.1
[0.3.0]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.2.1...maia-sdr-v0.3.0
[0.2.1]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.2.0...maia-sdr-v0.2.1
[0.2.0]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.1.2...maia-sdr-v0.2.0
[0.1.2]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.1.1...maia-sdr-v0.1.2
[0.1.1]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.1.0...maia-sdr-v0.1.1
[0.1.0]: https://github.com/maia-sdr/plutosdr-fw/releases/tag/maia-sdr-v0.1.0
