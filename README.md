# Nextcloud Python Framework (maintained fork)

> **Maintained fork.** Upstream [cloud-py-api/cloud_py_api](https://github.com/cloud-py-api/cloud_py_api)
> is archived. This fork is maintained by [teddy0605](https://github.com/teddy0605) for use with
> the maintained [MediaDC fork](https://github.com/teddy0605/mediadc). It adds Nextcloud 35
> support (`max-version` 35), lets the Python command fall back to the `MEDIADC_PYTHON`
> environment variable, and detects `occ` in the official Nextcloud Docker image
> (`/var/www/html`). Issues and pull requests: https://github.com/teddy0605/cloud_py_api/issues

[![CI](https://github.com/teddy0605/cloud_py_api/actions/workflows/ci.yml/badge.svg)](https://github.com/teddy0605/cloud_py_api/actions/workflows/ci.yml)
![PythonVersion](https://img.shields.io/badge/python-3.9%20%7C%203.10%20%7C%203.11-blue)
![impl](https://img.shields.io/pypi/implementation/nc_py_api)
![pypi](https://img.shields.io/pypi/v/nc_py_api.svg)
[![codecov](https://codecov.io/gh/cloud-py-api/cloud_py_api/branch/main/graph/badge.svg?token=6IHPKUYUU9)](https://codecov.io/gh/cloud-py-api/cloud_py_api)

Framework(App) for Nextcloud to develop apps, that using Python.

Consists of PHP part(**cloud_py_api app**) and a Python module(**nc-py-api**).

## Current state: Abandoned
### Project was divided into two different repositories:
### https://github.com/cloud-py-api/app_ecosystem_v2
### https://github.com/cloud-py-api/nc_py_api

## Provides Convenient Functions for Python

- Read & Write File System objects
- Working with Database
- Wrapper around `OCC` calls
- Calling your python function from php part of app and return a result

## 🚀 Installation

The app is not in the App Store under this fork. Install it from a release: every release
tarball is built by the release workflow from the tagged source and signed with a GitHub
build provenance attestation. Verify it before installing:

```bash
V=0.2.2
gh release download "v$V" -R teddy0605/cloud_py_api -p "cloud_py_api-$V.tar.gz" -p SHA256SUMS
sha256sum -c SHA256SUMS
gh attestation verify "cloud_py_api-$V.tar.gz" -R teddy0605/cloud_py_api
tar -xzf "cloud_py_api-$V.tar.gz" -C /path/to/nextcloud/custom_apps   # creates cloud_py_api/
chown -R www-data:www-data /path/to/nextcloud/custom_apps/cloud_py_api
sudo -u www-data php /path/to/nextcloud/occ app:enable --force cloud_py_api
```

Do not install if either check fails. The repository contains only the source (the built
`js/` is not committed). The release tarball contains the PHP app only; the `nc_py_api`
Python module is installed separately into the Python environment of the app that uses it.
Releases are made by pushing a `vX.Y.Z` tag that matches `appinfo/info.xml`.

The app supports Nextcloud 30 to 35.

#### More information can be found on [Wiki page](https://github.com/cloud-py-api/cloud_py_api/wiki)

## Maintainers

* [Andrey Borysenko](https://github.com/andrey18106)
* [Alexander Piskun](https://github.com/bigcat88)

## Apps using this

- [MediaDC](https://github.com/andrey18106/mediadc) - Nextcloud Media Duplicate collector app. Python part - core logics for duplicates search.
