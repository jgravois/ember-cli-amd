# Change Log
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

## [1.1.2]
- Small improvement for ember-cli-arcgis

## [1.1.1]
- Improved thw way AMD modules are discovered. Build time should be fatser.
- Support for Engines and Addons.
- amdModulePaths is not necessary anymore as the AMD modules are dicovered on the built code.

## [1.0.0]
- Based on Ember 2.18
- Changed the way we find and replace the conflicting Ember require and define function/references. Instead of using a regex and replacing string occurences, we are now using esprima to replace Identifiers and Literals.

## [0.4.9]
- Add support for addons and custom amd module paths

## [0.4.8]
- Don't replace #define with #efineday
- Add support for package main shorthand in module names
- Fix type for `buildOutput` and update README.

## [0.4.7]
### Fix
- Fix regular expression check for "require" in test loader

## [0.4.6]
### Fix
- Fix esprima parsing issue for functions with parameters with a default value

## [0.4.5]
### Changed
- Only scripts with src !== undefined are removed from the body. This allows us to put Google Analytics in the page or other json payloads

## [0.4.4]
### Added
- support for inlining of scripts
### Changed
- if not inlined, the amd-start and amd-config scripts are fingerprinted to enable cache-busting
- also ensured that other script tags in the body are not removed (i.e. google analytics)

## [0.4.1]
### Added
- support for assets deployed to cdn. If `fingerprint.prepend` is defined in the consuming project's `ember-cli-build.js` file, the specified path will be prepended to the AMD asset urls. If not present, the standard root-relative path of `/assets/SCRIPTNAME.js` is used.
