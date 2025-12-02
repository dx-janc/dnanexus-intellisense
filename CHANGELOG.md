# Change Log

All notable changes to the DNAnexus IntelliSense project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/).

## [Unreleased]

### In Development

- Comprehensive JSON schema definitions for DNAnexus configuration files
  - `dxapp.json` - App/Applet metadata and configuration
  - `dxworkflow.json` - Workflow definitions
  - `dxasset.json` - Asset bundle specifications
- Instance type schemas for multiple cloud providers (AWS, Azure, OCI)
- Dependency specification schemas (execDepends, bundledDepends, assetDepends)
- System requirements and resource allocation schemas
- VS Code extension implementation with JSON validation
- Enhanced markdown documentation in schemas for rich IDE integration

### Planned

- IntelliJ IDEA plugin implementation leveraging the same JSON schemas
- Additional refinements to schema definitions based on DNAnexus platform updates

## [0.0.1] - Initial Development

### Added

- Initial VS Code extension scaffold
- JSON validation for `dxapp.json`, `dxworkflow.json`, and `dxasset.json`
- Schema-driven architecture foundation
