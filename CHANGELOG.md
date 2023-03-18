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

## [0.1.2] - 2023-03-18

### Changed

- Updated Maia SDR to v0.2.0. The main change is the adaptive vertical size of the waterfall.

## [0.1.1] - 2023-02-14

### Fixed

- Problems with Pluto rev. C device tree (see [issue #2](https://github.com/maia-sdr/plutosdr-fw/issues/2)).

## [0.1.0] - 2023-02-11

Initial release of the Maia SDR ADALM Pluto firmware. This corresponds to the
[default ADI firmware v0.35](https://github.com/analogdevicesinc/plutosdr-fw/releases/tag/v0.35).

[unreleased]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.1.2...HEAD
[0.1.2]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.1.0...maia-sdr-v0.1.2
[0.1.1]: https://github.com/maia-sdr/plutosdr-fw/compare/maia-sdr-v0.1.0...maia-sdr-v0.1.1
[0.1.0]: https://github.com/maia-sdr/plutosdr-fw/releases/tag/maia-sdr-v0.1.0
