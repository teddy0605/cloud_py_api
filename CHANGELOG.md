# Changelog

All notable changes to this project will be documented in this file.

## [0.2.2 - 2026-10-04]

First release of the maintained fork (teddy0605/cloud_py_api).

### Changed

- Nextcloud 35 support (`max-version` 35).
- The default Python command falls back to the `MEDIADC_PYTHON` environment variable, and
  `nc_py_api` detects `occ` in the official Nextcloud Docker image.
- Updated frontend dependencies for security fixes.
- Releases are built by GitHub Actions from the tag and published with a build provenance
  attestation and `SHA256SUMS`; the built `js/` is not committed.

## [0.2.0 - 2024-10-20]

Maintenance update. Update NC versions to support NC30+ only.

### Added

- Added basic ObjectStorage support (/tmp folder used to execute binary scripts)

## [0.1.9 - 2023-12-14]

Maintenance update.

### Updated

- Updated npm packages
- Updated l10n

## [0.1.8 - 2023-06-19]

Maintenance update to add Nextcloud Hub 5 (27) support.

### Updated

- Updated packages
- Updated l10n

## [0.1.7 - 2023-03-27]

### Fixed

- Fixed `str_contains` (only in PHP8) function usage to `strpos` (available in PHP7)
- Fixed archive unpack on snap instances

## [0.1.6 - 2023-03-23]

### Fixed

- Fixed binary hashes check

## [0.1.5 - 2023-02-25]

### Changed

- Changed binary package format from one file to folder to speedup startup

## [0.1.4 - 2023-01-23]

### Removed

- Removed Thrift as not used and being replaced

## [0.1.3 - 2023-01-18]

### Fixed

- Fixed os arch detection (for arm64)

## [0.1.2 - 2023-01-17]

### Added

- Added check of sha256 pre-compiled binary checksum

### Fixed

- Fixed incorrect pre-compiled binary download (for Alpine-based systems)
- Fixed escape colon symbol in logs file names

## [0.1.1 - 2022-12-23]

### Changed

- Changed Admin settings list

## [0.1.0 - 2022-12-18]

This is the first `cloud_py_api` release

### Added

- Added MediaDC get file contents command
- Added Utils service for general actions
- Added Python service for running python scripts or binaries
- Added Python FS functions:
  * `fs_node_info`
  * `fs_list_directory`
  * `fs_file_data`
  * `fs_apply_exclude_lists`
  * `fs_apply_ignore_flags`
  * `fs_extract_sub_dirs`
  * `fs_filter_by`
  * `fs_sort_by_id`
