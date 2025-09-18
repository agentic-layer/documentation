# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an Antora documentation project for the Agentic Layer ecosystem. It consists of two main documentation modules:

1. **home** - Main documentation hub aggregating content from various repositories
2. **architecture** - Architecture documentation following the arc42 template

## Commands

### Building Documentation Locally
```bash
# Install dependencies
npm install

# Build the documentation site using the local playbook
npm run build

# Serve the built site locally (will be available at http://localhost:3000)
npm run serve

# Build and serve in one command
npm run dev
```

## Architecture Structure

### Documentation Modules
- `home/docs/` - Aggregated documentation hub with ROOT module containing index, tutorials, how-to guides, reference, and explanations
- `architecture/docs/` - arc42 architecture documentation with modules:
  - `building-blocks/` - System building blocks and components
  - `constraints/` - Architecture constraints
  - `context/` - System context and scope
  - `crosscutting/` - Cross-cutting concepts
  - `decisions/` - Architecture decisions
  - `deployment/` - Deployment view
  - `glossary/` - Terms and definitions
  - `introduction/` - Introduction and goals
  - `quality/` - Quality requirements
  - `risks/` - Risks and technical debt
  - `runtime/` - Runtime view
  - `solution-strategy/` - Solution strategy

### File Organization
- All documentation is written in **AsciiDoc format** (.adoc files)
- Each module has an `antora.yml` configuration file
- Navigation is defined in `nav.adoc` files within each module
- Content pages are in `modules/{module-name}/pages/` directories

### Content Inclusion
The home module aggregates content from other repositories using includes:
```adoc
include::<antora.name>:ROOT:partial$tutorials.adoc[]
```

## Development Guidelines
- Follow arc42 template structure for architecture documentation
- Maintain AsciiDoc format for all documentation files
- Update navigation files when adding new pages
- Use consistent style and tone with existing documentation