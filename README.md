# DNAnexus IntelliSense

Schema-driven validation and IntelliSense for DNAnexus configuration files across multiple IDEs.

## Overview

This project provides comprehensive JSON schema definitions for DNAnexus configuration files (`dxapp.json`, `dxworkflow.json`, `dxasset.json`), enabling intelligent code completion, validation, and documentation directly in your IDE.

### Schema-Driven Architecture

The core of this project is a collection of **JSON schemas** that serve as the single source of truth for DNAnexus configuration file specifications. These schemas define:

- Required and optional fields
- Field types and validation rules
- Allowed values and enumerations (e.g., instance types for AWS, Azure, OCI)
- Inline documentation and help text
- Cross-field relationships and dependencies

### Multi-Platform Support

**Current Implementation:**
- **VS Code Extension** - Currently functional, providing validation and IntelliSense for DNAnexus config files

**Planned Implementation:**
- **IntelliJ IDEA Plugin** - Planned for future development

Both implementations will leverage the same underlying JSON schemas, ensuring consistent behavior and validation rules across all supported IDEs.

## Features

- **Real-time Validation**: Catch configuration errors as you type
- **IntelliSense/Autocomplete**: Context-aware suggestions for field names, values, and structure
- **Inline Documentation**: View field descriptions and usage guidelines directly in your editor
- **Schema Completeness**: Comprehensive coverage of DNAnexus configuration specifications including:
  - App and Applet configurations (`dxapp.json`)
  - Workflow definitions (`dxworkflow.json`)
  - Asset specifications (`dxasset.json`)
  - System requirements and instance types (AWS, Azure, OCI)
  - Dependency specifications
  - DNAnexus links and resources

## Supported Files

The extension automatically activates for the following file types:

- `dxapp.json` - App and applet metadata and configuration
- `dxworkflow.json` - Workflow and global workflow definitions
- `dxasset.json` - Asset bundle specifications

## Project Structure

```
dnanexus-intellisense/
├── schemas/              # JSON Schema definitions (source of truth)
│   ├── dxapp.schema.json
│   ├── dxworkflow.schema.json
│   ├── dxasset.schema.json
│   ├── instanceTypes.*.schema.json
│   └── ...additional schema files
├── src/                  # VS Code extension implementation
│   └── extension.ts
└── package.json          # Extension manifest
```

## Development Status

**Current Phase**: Schema refinement and VS Code extension development

The JSON schemas are actively being developed and refined to ensure comprehensive coverage of all DNAnexus configuration options. Once the schemas are stable, they will serve as the foundation for both the VS Code extension and the planned IntelliJ IDEA plugin.

## Installation

### VS Code Extension

The extension is currently in development. To use it locally:

1. Clone this repository
2. Run `npm install`
3. Run `npm run watch` to start the build process
4. Press `F5` to launch the Extension Development Host

## Contributing

Contributions to the JSON schemas and extension implementations are welcome. Please ensure any schema changes maintain backward compatibility and include appropriate documentation.

## Schema Development

The schemas follow the [JSON Schema Draft 2020-12](https://json-schema.org/draft/2020-12/schema) specification and include:

- Standard JSON Schema validation rules
- Enhanced descriptions using `markdownDescription` for rich formatting in IDEs
- Comprehensive enumerations for cloud provider-specific configurations
- Modular structure with referenced sub-schemas for reusability

## License

[License information to be added]

## Resources

- [DNAnexus Documentation](https://documentation.dnanexus.com/)
- [DNAnexus API Specification](https://documentation.dnanexus.com/developer)
- [JSON Schema Specification](https://json-schema.org/)
