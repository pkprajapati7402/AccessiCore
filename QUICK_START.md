# Quick Start Guide

Get AccessiCore up and running in minutes!

## For Users

### Installation (When Available)

#### From Chrome Web Store
1. Visit the [Chrome Web Store](https://chrome.google.com/webstore) (link coming soon)
2. Search for "AccessiCore"
3. Click "Add to Chrome"
4. Click "Add extension"

#### From Firefox Add-ons
1. Visit [Firefox Add-ons](https://addons.mozilla.org) (link coming soon)
2. Search for "AccessiCore"
3. Click "Add to Firefox"

#### Manual Installation (Current Development)

**Chrome/Edge:**
1. Download the latest release from [GitHub Releases](https://github.com/pkprajapati7402/AccessiCore/releases)
2. Unzip the downloaded file
3. Open `chrome://extensions/` (or `edge://extensions/`)
4. Enable "Developer mode" (top right)
5. Click "Load unpacked"
6. Select the unzipped folder

**Firefox:**
1. Download the `.xpi` file from [GitHub Releases](https://github.com/pkprajapati7402/AccessiCore/releases)
2. Open `about:addons`
3. Click the gear icon → "Install Add-on From File"
4. Select the downloaded `.xpi` file

### First Use

1. **Navigate to any website**
2. **Click the AccessiCore icon** in your browser toolbar
3. **Enable AccessiCore** for the current site
4. **Try the conversational interface**:
   - Press `Ctrl+Shift+A` (or `Cmd+Shift+A` on Mac)
   - Ask: "What can I do on this page?"
   - Follow the suggestions

### Basic Commands

Try asking AccessiCore:
- "What is the main action on this page?"
- "Show me navigation options"
- "Read the important section"
- "Go to the contact form"
- "What are the required fields?"
- "Help me fill in this form"

### Settings

Click the AccessiCore icon → Settings to:
- Enable/disable automatic activation
- Choose your preferred interaction mode
- Adjust verbosity level
- Configure keyboard shortcuts
- Manage site permissions

---

## For Developers

### Prerequisites

- **Node.js** v16 or higher ([Download](https://nodejs.org/))
- **npm** v7 or higher (comes with Node.js)
- **Git** ([Download](https://git-scm.com/))
- Modern web browser (Chrome, Firefox, or Edge)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/pkprajapati7402/AccessiCore.git
cd AccessiCore

# 2. Install dependencies
npm install

# 3. Start development mode
npm run dev
```

### Loading the Extension

#### Chrome/Edge
1. Open `chrome://extensions/` or `edge://extensions/`
2. Enable "Developer mode"
3. Click "Load unpacked"
4. Select the `dist` folder from your AccessiCore directory

#### Firefox
1. Open `about:debugging#/runtime/this-firefox`
2. Click "Load Temporary Add-on"
3. Navigate to `dist` folder and select `manifest.json`

### Development Workflow

```bash
# Start development mode (with hot reload)
npm run dev

# Run tests
npm test

# Run tests in watch mode
npm run test:watch

# Lint code
npm run lint

# Format code
npm run format

# Build for production
npm run build:prod
```

### Making Changes

1. **Make your changes** in the `src/` directory
2. **The extension will reload automatically** (if using `npm run dev`)
3. **Refresh the web page** you're testing on
4. **Check browser console** for any errors

### Project Structure

```
src/
├── background/     # Background service worker
├── content/        # Content scripts (runs on web pages)
├── popup/          # Extension popup UI
├── models/         # AI/ML integration
└── utils/          # Helper functions
```

See [PROJECT_STRUCTURE.md](docs/PROJECT_STRUCTURE.md) for complete details.

### Running Tests

```bash
# All tests
npm test

# With coverage report
npm run test:coverage

# Specific test file
npm test -- path/to/test.spec.js

# Watch mode (runs tests on file changes)
npm run test:watch
```

### Building for Production

```bash
# Build optimized version
npm run build:prod

# Output will be in dist/ folder
# dist/ is what you package for distribution
```

### Common Issues

#### Port already in use
```bash
# Kill the process or change the port in webpack config
```

#### Extension not loading
- Check browser console for errors
- Ensure `dist/` folder exists
- Try `npm run build` manually
- Verify manifest.json is valid

#### Changes not reflecting
- Refresh the extension in browser's extension page
- Reload the web page
- Clear browser cache
- Restart `npm run dev`

### Debugging

**Browser DevTools:**
- Right-click extension icon → "Inspect popup"
- For content scripts: Inspect the web page
- Console logs appear in relevant DevTools

**Background Scripts:**
- `chrome://extensions/` → Click "Service worker" under AccessiCore
- View logs and debug the background script

### Next Steps

1. Read [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines
2. Check [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) for system design
3. Look for `good first issue` labels on GitHub
4. Join [GitHub Discussions](https://github.com/pkprajapati7402/AccessiCore/discussions)

---

## For Contributors

### First Contribution

1. **Fork the repository** on GitHub
2. **Clone your fork**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/AccessiCore.git
   ```
3. **Create a branch**:
   ```bash
   git checkout -b feature/my-awesome-feature
   ```
4. **Make your changes**
5. **Test thoroughly**
6. **Commit with conventional commits**:
   ```bash
   git commit -m "feat: add amazing feature"
   ```
7. **Push to your fork**:
   ```bash
   git push origin feature/my-awesome-feature
   ```
8. **Open a Pull Request** on GitHub

### Code Style

We use:
- **ESLint** for code quality
- **Prettier** for formatting
- **Conventional Commits** for commit messages

Run before committing:
```bash
npm run lint:fix
npm run format
npm test
```

### Getting Help

- 📖 Read the docs in `docs/`
- 💬 Ask in [GitHub Discussions](https://github.com/pkprajapati7402/AccessiCore/discussions)
- 🐛 Check existing issues on GitHub
- 📧 Email: help@accessicore.example.com

---

## Troubleshooting

### Extension Not Working
1. Check if it's enabled for the current site
2. Verify permissions are granted
3. Look for error messages in browser console
4. Try disabling/re-enabling the extension

### Performance Issues
- Disable on complex single-page apps initially
- Adjust settings to reduce processing
- Report the site URL so we can optimize

### Accessibility Issues
- Report them! This is an accessibility tool, irony is not lost on us
- Use [Accessibility Issue template](https://github.com/pkprajapati7402/AccessiCore/issues/new?template=accessibility_issue.md)

### Getting Support

- **Users**: [GitHub Discussions](https://github.com/pkprajapati7402/AccessiCore/discussions)
- **Developers**: [Contributing Guide](CONTRIBUTING.md)
- **Security**: [Security Policy](SECURITY.md)

---

## Resources

- [Full Documentation](docs/)
- [API Reference](docs/API.md)
- [Architecture Guide](docs/ARCHITECTURE.md)
- [User Guide](docs/USER_GUIDE.md)

---

**Welcome to AccessiCore! Let's make the web accessible together.** 🌐♿
