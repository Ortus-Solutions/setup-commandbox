# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

----

## [2.0.0] => 2022-FEB-08

### Added

* Ability to install any package when installed via the `install` input
* Ability to install ANY CommandBox version by leveraging the `version` input
* Ability to disable/enable the installation of our global dependencies via the `installGlobalDependencies` input

### Changed

* `installGlobalDependencies` is now false by default. If you want cfconfig and dotenv, you must explicitly set this input to true
* Only set the FORGEBOX tokens when passed as an input
* Migrated installation from apt to binary installs