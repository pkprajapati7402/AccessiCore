# AccessiCore

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![FOSS](https://img.shields.io/badge/FOSS-100%25-brightgreen.svg)](https://en.wikipedia.org/wiki/Free_and_open-source_software)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](CONTRIBUTING.md)
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)

### Free and Open Source AI-Powered Semantic Web Accessibility Repair Tool

> 🌐 Built by the community, for the community.  
> Rebuilding web accessibility in real time using a local Small Language Model (SLM).  
> Turning inaccessible websites into conversational, navigable experiences.

**AccessiCore** is a 100% free and open source (FOSS) project committed to making the web accessible to everyone. We believe that digital accessibility is a fundamental human right, not a paid feature.

---

## 🌍 The Problem

Millions of essential websites — government portals, small business platforms, educational dashboards, and legacy forums — remain inaccessible to visually impaired users.

Common issues include:

* Missing or incorrect ARIA roles
* Broken semantic HTML structure
* Layouts dependent on visual cues
* Complex dynamic components unreadable by screen readers
* Poor keyboard navigation support

When the DOM lacks meaningful structure, traditional screen readers struggle. The result: frustration, exclusion, and lost access to critical services.

---

## 🚀 The Solution

**AccessiCore** is a browser extension that re-indexes web pages in real time using a local Small Language Model (SLM).

Instead of just reading text, it understands:

* The intent of the page
* The purpose of UI components
* The logical structure of navigation
* The primary actions and user flows

It then creates a semantic overlay and enables a conversational interface, allowing users to **talk to the website** instead of struggling through it.

---

## ✨ Core Features

### 🧠 Real-Time Semantic Reindexing

Understands page structure beyond raw HTML and builds a meaningful semantic map.

### 💬 Conversational Interface

Users can ask:

* “What is the main action on this page?”
* “Show me payment options.”
* “Read the important section.”
* “Go to contact form.”

### 🏷 AI-Generated Accessibility Overlay

Automatically adds:

* ARIA labels
* Corrected roles
* Improved focus order
* Landmark regions

Without breaking the site’s original functionality.

### 🔒 Local-First Privacy

* Runs locally by default
* No page data sent externally unless user explicitly opts in
* Minimal storage footprint

### 🛠 Developer Mode

* Visualize inferred semantic tree
* Inspect intent classification
* Override AI decisions manually

---

## 🏗 How It Works (Conceptual Flow)

1. The extension analyzes the rendered DOM.
2. A local SLM interprets structure, hierarchy, and intent.
3. A semantic map is generated.
4. A non-destructive accessibility layer is injected.
5. Users interact via voice or text.
6. Commands are translated into real DOM interactions.

The original site remains untouched — AccessiCore acts as an intelligent interpretation layer.

---

## 🧩 System Architecture

### Browser Extension Layer

* Content analysis
* Overlay injection
* Conversation UI
* Site-level preferences

### Local SLM Runtime

* Lightweight model execution
* Structured semantic output
* Intent detection & mapping

### Fallback Heuristic Engine

* DOM-based analysis if no model is available
* Ensures baseline functionality even on low-resource systems

---

## 🔐 Privacy & Security Philosophy

* Local inference by default
* Explicit consent for cloud features
* No hidden telemetry
* Per-site activation model
* Non-destructive overlays

Accessibility should never compromise privacy.

---

## 🎯 Example User Experience

### Scenario 1: Navigating a Government Portal

User:

> “What can I do on this page?”

AccessiCore:

> “You can:
>
> 1. File a new application
> 2. Check application status
> 3. Download forms”

User:

> “Open file new application.”

Focus shifts directly to the correct button.

---

### Scenario 2: Filling a Form

AccessiCore clearly identifies:

* Required fields
* Field purposes
* Error messages
* Submission actions

Users can navigate field-by-field conversationally.

---

### Scenario 3: Understanding a Complex Dashboard

Instead of chaotic reading order, AccessiCore summarizes:

* Primary section
* Secondary panels
* Important alerts
* Key metrics

---

## 🧪 Testing & Accessibility Standards

AccessiCore aligns with:

* WCAG accessibility principles
* ARIA best practices
* Keyboard-first navigation
* Screen reader compatibility

Extensive testing includes:

* Real user feedback loops
* Dynamic content handling
* Performance optimization
* Mutation observation for single-page apps

---

## 🛣 Roadmap

* Fine-tuned accessibility-specific SLM
* Multi-language semantic understanding
* Community-driven site repair templates
* Screen reader API integrations
* Cloud-assisted optional inference
* Shared semantic correction library

---

## 📦 Installation & Setup

### Prerequisites

* Node.js (v16 or higher)
* npm or yarn package manager
* Modern web browser (Chrome, Firefox, or Edge)
* Git for version control

### Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/AccessiCore.git
cd AccessiCore

# Install dependencies
npm install

# Build the extension
npm run build

# For development mode with hot reload
npm run dev
```

### Loading the Extension

#### Chrome/Edge
1. Open `chrome://extensions/` or `edge://extensions/`
2. Enable "Developer mode"
3. Click "Load unpacked"
4. Select the `dist` folder from the project directory

#### Firefox
1. Open `about:debugging#/runtime/this-firefox`
2. Click "Load Temporary Add-on"
3. Navigate to the `dist` folder and select `manifest.json`

---

## 🔧 Development

### Project Structure

```
AccessiCore/
├── src/                    # Source code
│   ├── background/         # Background scripts
│   ├── content/            # Content scripts
│   ├── popup/              # Extension popup UI
│   ├── models/             # SLM integration
│   └── utils/              # Utility functions
├── public/                 # Static assets
├── tests/                  # Test suites
├── docs/                   # Documentation
├── LICENSE                 # MIT License
└── README.md              # This file
```

### Running Tests

```bash
# Run all tests
npm test

# Run with coverage
npm run test:coverage

# Run specific test suite
npm test -- --grep "semantic-analysis"
```

### Building for Production

```bash
npm run build:prod
```

---

## 🛠 Technical Stack

### Core Technologies

* **Frontend**: Vanilla JavaScript/TypeScript
* **UI Framework**: Web Components
* **SLM Runtime**: ONNX Runtime / TensorFlow.js
* **Build Tool**: Webpack/Vite
* **Testing**: Jest, Playwright

### Dependencies

All dependencies are open source and carefully vetted for:
- Security vulnerabilities
- License compatibility
- Active maintenance
- Community support

See `package.json` for the complete list.

---

## 🤝 Contributing

**We welcome and celebrate all contributors!** AccessiCore is built by the community, for the community.

### How to Contribute

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`)
4. **Push to the branch** (`git push origin feature/AmazingFeature`)
5. **Open a Pull Request**

### Areas We Need Help With

* 🧠 **Accessibility Research** - Testing with real assistive technologies
* 💻 **Frontend Development** - Extension UI/UX improvements
* 🤖 **AI/ML Engineering** - SLM optimization and training
* 🎨 **Design** - User experience for visually impaired users
* 📝 **Documentation** - Tutorials, guides, and API docs
* 🧪 **Testing** - Writing tests, manual QA
* 🌍 **Localization** - Translating the extension
* ♿ **User Testing** - Feedback from assistive technology users

### Code of Conduct

We are committed to providing a welcoming and inclusive environment for all contributors. Please read our [Code of Conduct](CODE_OF_CONDUCT.md) before contributing.

### Contribution Guidelines

* Write clear, documented code
* Follow existing code style and conventions
* Include tests for new features
* Update documentation as needed
* Be respectful and constructive in discussions
* Focus on accessibility and privacy in all contributions

### First-Time Contributors

Look for issues labeled `good first issue` or `help wanted`. Don't hesitate to ask questions — we're here to help!

### Recognition

All contributors will be:
- Listed in our CONTRIBUTORS.md file
- Credited in release notes
- Celebrated in our community channels

---

## 💬 Community & Support

### Get Involved

* **GitHub Discussions**: Ask questions, share ideas, get help
* **Issue Tracker**: Report bugs, request features
* **Pull Requests**: Contribute code and documentation

### Communication Channels

* **Discussions**: [GitHub Discussions](https://github.com/yourusername/AccessiCore/discussions)
* **Issues**: [GitHub Issues](https://github.com/yourusername/AccessiCore/issues)
* **Email**: accessicore@example.com (for sensitive matters)

### Reporting Security Vulnerabilities

If you discover a security vulnerability, please **DO NOT** open a public issue. Email us directly at security@accessicore.example.com.

---

## 🌟 Vision

AccessiCore is not just a browser extension.

It’s an attempt to create a semantic safety net for the web — ensuring that no user is excluded because a website was poorly structured.

**The web should be understandable.  
The web should be navigable.  
The web should be inclusive.**

AccessiCore exists to make that real.

As a FOSS project, we believe:
- **Freedom**: Users have the right to run, study, modify, and share the software
- **Transparency**: All code is open for inspection and improvement
- **Community**: Built collaboratively by developers, accessibility advocates, and users
- **Privacy**: No data collection, no tracking, no monetization of user data
- **Sustainability**: Maintained by the community, not dependent on corporate interests

---

## 📄 License

**AccessiCore** is free and open source software licensed under the [MIT License](LICENSE).

### What this means:
✅ **Commercial use** - Use it in your projects, even commercially  
✅ **Modification** - Change and adapt the code to your needs  
✅ **Distribution** - Share the software with anyone  
✅ **Private use** - Use it privately without restrictions  
✅ **No warranty** - Software is provided "as is"

### MIT License Summary

```
MIT License

Copyright (c) 2026 AccessiCore Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

See the [LICENSE](LICENSE) file for the full license text.

### Third-Party Licenses

AccessiCore uses various open source libraries and tools. All third-party dependencies maintain their original licenses, which are compatible with our MIT License. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for details.

---

## 🎓 FOSS Hackathon 2026

This project was created for the FOSS Hackathon with the goal of demonstrating how open source technology can solve real-world accessibility challenges.

### Project Goals
- Demonstrate the power of local-first AI for accessibility
- Build a community around web accessibility improvements
- Create reusable patterns for semantic web interpretation
- Inspire similar FOSS projects in the accessibility space

### Why FOSS?
- **Accessibility tools should be free** - No one should pay for basic digital access rights
- **Trust through transparency** - Users can verify privacy claims by reading the code
- **Community innovation** - The best solutions come from diverse contributors
- **Sustainable impact** - FOSS projects outlive commercial products

---

## 🏆 Acknowledgments

Built with ❤️ by the open source community.

Special thanks to:
- All contributors who donated their time and expertise
- Accessibility advocates who provided feedback and testing
- The broader FOSS community for tools and inspiration
- Screen reader users who helped validate the approach

---

## 📚 Additional Resources

* [Contributing Guidelines](CONTRIBUTING.md)
* [Code of Conduct](CODE_OF_CONDUCT.md)
* [Security Policy](SECURITY.md)
* [Changelog](CHANGELOG.md)
* [Developer Documentation](docs/)
* [API Reference](docs/API.md)

---

## ⭐ Support the Project

If you find AccessiCore useful:
- ⭐ Star this repository
- 🐛 Report bugs and suggest features
- 💻 Contribute code or documentation
- 📢 Spread the word about accessible web design
- ♿ Share your accessibility insights

**Together, we can make the web accessible for everyone.**

---

*Made with 💙 by the AccessiCore community | Licensed under MIT | 100% Free and Open Source*

