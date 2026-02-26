# Project Structure

This document outlines the structure of the AccessiCore project.

```
AccessiCore/
│
├── .github/                      # GitHub-specific files
│   ├── ISSUE_TEMPLATE/          # Issue templates
│   │   ├── bug_report.md
│   │   ├── feature_request.md
│   │   ├── accessibility_issue.md
│   │   └── config.yml
│   ├── workflows/               # GitHub Actions CI/CD
│   │   ├── ci.yml
│   │   └── release.yml
│   └── PULL_REQUEST_TEMPLATE.md
│
├── src/                         # Source code
│   ├── background/              # Background scripts
│   │   ├── background.js        # Main background service worker
│   │   ├── message-handler.js   # Message passing logic
│   │   └── storage.js           # Storage management
│   │
│   ├── content/                 # Content scripts
│   │   ├── content.js           # Main content script
│   │   ├── dom-analyzer.js      # DOM analysis logic
│   │   ├── semantic-mapper.js   # Semantic tree generation
│   │   ├── overlay-injector.js  # Accessibility overlay
│   │   └── overlay.css          # Overlay styles
│   │
│   ├── popup/                   # Extension popup UI
│   │   ├── popup.html           # Popup HTML
│   │   ├── popup.js             # Popup logic
│   │   └── popup.css            # Popup styles
│   │
│   ├── options/                 # Extension settings page
│   │   ├── options.html         # Settings HTML
│   │   ├── options.js           # Settings logic
│   │   └── options.css          # Settings styles
│   │
│   ├── models/                  # AI/ML model integration
│   │   ├── model-loader.js      # SLM loading logic
│   │   ├── inference.js         # Model inference
│   │   ├── semantic-analysis.js # Intent classification
│   │   └── fallback-engine.js   # Heuristic fallback
│   │
│   ├── conversation/            # Conversational interface
│   │   ├── conversation-ui.js   # Chat interface
│   │   ├── command-parser.js    # Natural language parsing
│   │   ├── action-executor.js   # DOM interaction
│   │   └── conversation.css     # Chat styles
│   │
│   ├── utils/                   # Utility functions
│   │   ├── dom-utils.js         # DOM manipulation helpers
│   │   ├── aria-utils.js        # ARIA attribute helpers
│   │   ├── logger.js            # Logging utility
│   │   └── config.js            # Configuration
│   │
│   └── constants/               # Constants and enums
│       ├── aria-roles.js        # ARIA role definitions
│       ├── semantic-types.js    # Semantic classification types
│       └── commands.js          # Conversation commands
│
├── public/                      # Static assets
│   ├── icons/                   # Extension icons
│   │   ├── icon-16.png
│   │   ├── icon-48.png
│   │   └── icon-128.png
│   │
│   └── assets/                  # Other static assets
│       ├── sounds/              # Audio feedback
│       └── images/              # UI images
│
├── models/                      # Pre-trained models (gitignored if large)
│   ├── .gitkeep
│   └── README.md                # Model documentation
│
├── tests/                       # Test suites
│   ├── unit/                    # Unit tests
│   │   ├── dom-analyzer.test.js
│   │   ├── semantic-mapper.test.js
│   │   └── command-parser.test.js
│   │
│   ├── integration/             # Integration tests
│   │   ├── extension.test.js
│   │   └── conversation.test.js
│   │
│   ├── e2e/                     # End-to-end tests
│   │   └── user-flows.test.js
│   │
│   ├── accessibility/           # Accessibility tests
│   │   ├── aria.test.js
│   │   └── keyboard-nav.test.js
│   │
│   └── fixtures/                # Test fixtures
│       └── sample-pages/
│
├── docs/                        # Documentation
│   ├── API.md                   # API reference
│   ├── ARCHITECTURE.md          # System architecture
│   ├── DEVELOPMENT.md           # Development guide
│   ├── USER_GUIDE.md            # User guide
│   ├── MODEL_TRAINING.md        # ML model training guide
│   └── BROWSER_COMPAT.md        # Browser compatibility notes
│
├── scripts/                     # Build and utility scripts
│   ├── build.js                 # Build script
│   ├── package-extension.js     # Packaging script
│   └── update-manifest.js       # Manifest updater
│
├── config/                      # Configuration files
│   ├── webpack.config.js        # Webpack configuration
│   ├── babel.config.js          # Babel configuration
│   ├── jest.config.js           # Jest configuration
│   └── eslint.config.js         # ESLint configuration
│
├── .gitignore                   # Git ignore patterns
├── .prettierrc                  # Prettier configuration
├── .eslintrc.json              # ESLint rules
├── package.json                 # NPM dependencies and scripts
├── manifest.json                # Browser extension manifest
├── LICENSE                      # MIT License
├── README.md                    # Project overview
├── CHANGELOG.md                 # Version history
├── CONTRIBUTING.md              # Contribution guidelines
├── CODE_OF_CONDUCT.md          # Code of conduct
├── SECURITY.md                  # Security policy
└── CONTRIBUTORS.md              # Contributor recognition
```

## Directory Descriptions

### `/src`
The main source code directory containing all extension functionality.

### `/src/background`
Background service worker that manages extension state, handles browser events, and coordinates between content scripts.

### `/src/content`
Content scripts that run in the context of web pages, analyzing the DOM and injecting accessibility improvements.

### `/src/models`
AI/ML model integration code for semantic understanding and intent classification.

### `/src/conversation`
The conversational interface that allows users to interact with websites through natural language.

### `/tests`
Comprehensive test suites including unit, integration, E2E, and accessibility tests.

### `/docs`
Detailed documentation for developers, contributors, and users.

### `/public`
Static assets like icons and images that are bundled with the extension.

### `/.github`
GitHub-specific files including issue templates, PR templates, and CI/CD workflows.

## Key Files

- **manifest.json**: Browser extension manifest (v3)
- **package.json**: NPM dependencies and build scripts
- **webpack.config.js**: Build configuration
- **LICENSE**: MIT License terms
- **README.md**: Project overview and getting started guide

## Build Output

When built, the extension is compiled to:
```
dist/                            # Build output (gitignored)
├── background/
├── content/
├── popup/
├── icons/
└── manifest.json
```

This directory is what gets loaded as an unpacked extension during development or packaged for distribution.

## Development Workflow

1. Make changes in `/src`
2. Run `npm run dev` for development mode with hot reload
3. Load `dist/` as unpacked extension in browser
4. Test changes manually and with automated tests
5. Build for production with `npm run build:prod`
6. Package with scripts in `/scripts` directory

---

*This structure follows best practices for browser extensions and FOSS projects.*
