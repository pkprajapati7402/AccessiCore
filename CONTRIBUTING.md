# Contributing to AccessiCore

First off, thank you for considering contributing to AccessiCore! 🎉

It's people like you who make AccessiCore such a great tool for improving web accessibility.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Style Guidelines](#style-guidelines)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

## How Can I Contribute?

### Reporting Bugs 🐛

Before submitting a bug report:
- Check the [issue tracker](https://github.com/yourusername/AccessiCore/issues) to see if the issue has already been reported
- Check the [discussions](https://github.com/yourusername/AccessiCore/discussions) for known issues
- Collect information about the bug (browser version, OS, steps to reproduce)

When submitting a bug report, include:
- A clear and descriptive title
- Detailed steps to reproduce the issue
- Expected behavior vs actual behavior
- Screenshots or recordings if applicable
- Browser console logs if relevant
- System information (OS, browser version, extension version)

### Suggesting Enhancements 💡

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, include:
- A clear and descriptive title
- Detailed explanation of the proposed feature
- Why this enhancement would be useful
- Possible implementation approach (if you have ideas)
- Examples from other projects (if applicable)

### Contributing Code 💻

#### Good First Issues

Look for issues labeled:
- `good first issue` - Great for newcomers
- `help wanted` - We need community help on these
- `accessibility` - Accessibility-specific improvements
- `documentation` - Documentation improvements

#### Areas We Need Help

- **Accessibility Testing**: Testing with real screen readers and assistive technologies
- **SLM Integration**: Optimizing and integrating language models
- **Browser Compatibility**: Testing across different browsers
- **Documentation**: Improving docs, tutorials, examples
- **Internationalization**: Translating the extension
- **Testing**: Writing unit tests, integration tests, E2E tests
- **Performance**: Optimizing the extension for speed and memory
- **UI/UX**: Improving the user interface and experience

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- Git
- A GitHub account
- A modern web browser (Chrome, Firefox, or Edge)

### Setup Development Environment

1. **Fork the repository** on GitHub

2. **Clone your fork**
   ```bash
   git clone https://github.com/YOUR_USERNAME/AccessiCore.git
   cd AccessiCore
   ```

3. **Add upstream remote**
   ```bash
   git remote add upstream https://github.com/originalowner/AccessiCore.git
   ```

4. **Install dependencies**
   ```bash
   npm install
   ```

5. **Create a branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

6. **Start development mode**
   ```bash
   npm run dev
   ```

## Development Workflow

### Making Changes

1. **Keep your fork synced**
   ```bash
   git fetch upstream
   git merge upstream/main
   ```

2. **Make your changes**
   - Write clean, readable code
   - Follow the existing code style
   - Add comments for complex logic
   - Update documentation as needed

3. **Test your changes**
   ```bash
   npm test
   npm run test:integration
   ```

4. **Build the project**
   ```bash
   npm run build
   ```

5. **Load and test the extension manually**
   - Load the unpacked extension in your browser
   - Test the functionality thoroughly
   - Check browser console for errors

### Running Tests

```bash
# Run all tests
npm test

# Run with coverage
npm run test:coverage

# Run specific test file
npm test -- path/to/test.spec.js

# Run tests in watch mode
npm run test:watch
```

## Style Guidelines

### JavaScript/TypeScript Style

- Use ES6+ features
- Use meaningful variable and function names
- Keep functions small and focused
- Add JSDoc comments for public functions
- Use TypeScript types where applicable
- Follow the existing code style

Example:
```javascript
/**
 * Analyzes the DOM structure and builds a semantic map
 * @param {HTMLElement} root - The root element to analyze
 * @param {Object} options - Configuration options
 * @returns {SemanticMap} The generated semantic map
 */
function analyzeDOM(root, options = {}) {
  // Implementation
}
```

### Code Formatting

We use Prettier for code formatting. Run before committing:
```bash
npm run format
```

To check formatting:
```bash
npm run format:check
```

### Linting

We use ESLint for code quality. Run before committing:
```bash
npm run lint
```

To auto-fix issues:
```bash
npm run lint:fix
```

## Commit Guidelines

We follow [Conventional Commits](https://www.conventionalcommits.org/) specification.

### Commit Message Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, missing semicolons, etc.)
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Adding or updating tests
- `chore`: Maintenance tasks
- `ci`: CI/CD changes

### Examples

```
feat(semantic): add support for dynamic content analysis

Add real-time monitoring of DOM mutations to update semantic map
when content changes dynamically.

Closes #123
```

```
fix(accessibility): correct ARIA label generation for buttons

Previously, buttons without text were getting empty ARIA labels.
Now we use adjacent text or title attributes as fallback.

Fixes #456
```

## Pull Request Process

### Before Submitting

- [ ] Code follows the project's style guidelines
- [ ] All tests pass locally
- [ ] New tests added for new features
- [ ] Documentation updated
- [ ] Commit messages follow guidelines
- [ ] Branch is up to date with main

### Submitting a Pull Request

1. **Push your changes**
   ```bash
   git push origin feature/your-feature-name
   ```

2. **Open a Pull Request** on GitHub

3. **Fill out the PR template** completely
   - Clear description of the changes
   - Link to related issues
   - Screenshots/recordings if UI changes
   - Testing performed

4. **Wait for review**
   - Maintainers will review your PR
   - Address any feedback or requested changes
   - Keep the PR up to date with main branch

5. **After approval**, maintainers will merge your PR

### PR Review Criteria

- Code quality and readability
- Test coverage
- Documentation completeness
- Accessibility improvements (not regressions)
- Performance impact
- Browser compatibility
- Security considerations

## Community

### Getting Help

- **GitHub Discussions**: Ask questions and get help
- **Issue Comments**: Discuss specific issues
- **Documentation**: Check the docs folder

### Recognition

All contributors will be:
- Added to CONTRIBUTORS.md
- Mentioned in release notes
- Celebrated in our community

## License

By contributing to AccessiCore, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for contributing to making the web more accessible! 🌐♿**
