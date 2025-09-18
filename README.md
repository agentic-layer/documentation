# Agentic Layer Documentation

Documentation platform for the Agentic Layer ecosystem.

---

## Table of Contents

- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [Project Structure](#project-structure)

---

## Prerequisites

To work with this documentation project, you'll need the following tools installed on your system:

* **Antora** - Documentation site generator (latest stable version)
* **Node.js** - Required for Antora and related tooling

---

## Getting Started

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

## Contributing

We welcome contributions to improve the documentation! Here are the guidelines for contributors:

### Architecture Documentation
Architecture documentation is located at `architecture/docs` and follows the arc42 template structure. Each section corresponds to a specific aspect of the system architecture. When adding or updating architecture documentation, ensure that you adhere to the arc42 guidelines.

### User Guidlines
Documentation for user guidelines, tutorials, how-to guides, references, and explanations is located in the respective repositories `./docs/modules/ROOT/partials`. The pages in the `home` module aggregate this content. If you wish to add content from a new repository simply add it with the following syntax:

``` yml
# <antora.name> is defined in the antora.yml of the respective module

include::<antora.name>:ROOT:partial$tutorials.adoc[]
```

### Documentation Standards

* **Format**: All documentation is written in AsciiDoc format (.adoc files)
* **Structure**: Follow the established Antora module structure
* **Style**: Maintain consistency with existing documentation style and tone
* **Navigation**: Update navigation files (nav.adoc) when adding new pages



## Project Structure

This documentation project is organized using the Antora documentation framework with the following structure:

```
documentation/
├── architecture/           # Architecture documentation module
│   └── docs/
│       ├── antora.yml     # Module configuration
│       └── modules/       # Documentation modules
│           ├── ROOT/
│           ├── building-blocks/
│           ├── constraints/
│           ├── context/
│           ├── crosscutting/
│           ├── decisions/
│           ├── deployment/
│           ├── glossary/
│           ├── introduction/
│           ├── quality/
│           ├── risks/
│           ├── runtime/
│           └── solution-strategy/
└── home/                  # Main documentation hub module
    └── docs/
        ├── antora.yml     # Module configuration
        └── modules/
            └── ROOT/
                ├── nav.adoc
                └── pages/ # Aggregated content from various repositories
                    ├── explanation.adoc
                    ├── how-to-guides.adoc
                    ├── index.adoc
                    ├── reference.adoc
                    └── tutorials.adoc
```