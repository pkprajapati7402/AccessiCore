# Security Policy

## Supported Versions

We release patches for security vulnerabilities in the following versions:

| Version | Supported          |
| ------- | ------------------ |
| 0.x.x   | :white_check_mark: |

As this is an early-stage project, we currently support the latest version. Once we reach v1.0, we will maintain security updates for multiple versions.

## Reporting a Vulnerability

We take the security of AccessiCore seriously. If you believe you have found a security vulnerability, please report it to us as described below.

### Please Do Not

- **Open a public GitHub issue** if the bug is a security vulnerability
- **Discuss the vulnerability publicly** until it has been addressed

### Please Do

**Email us directly at:** security@accessicore.example.com

Include the following information (as much as you can provide):

- **Type of vulnerability** (e.g., XSS, injection, privilege escalation)
- **Full paths of source file(s)** related to the vulnerability
- **Location of the affected source code** (tag/branch/commit or direct URL)
- **Step-by-step instructions** to reproduce the issue
- **Proof-of-concept or exploit code** (if possible)
- **Impact of the vulnerability**, including how an attacker might exploit it
- **Any potential mitigations** you've identified

### What to Expect

After you submit a vulnerability report, here's what will happen:

1. **Acknowledgment**: We'll acknowledge receipt of your vulnerability report within 48 hours
2. **Assessment**: We'll confirm the vulnerability and determine its impact (within 5 business days)
3. **Fix Development**: We'll work on a fix and keep you informed of progress
4. **Release**: We'll release a patch and publicly disclose the vulnerability
5. **Credit**: We'll credit you in the security advisory (unless you prefer to remain anonymous)

### Disclosure Policy

- **Coordinated disclosure**: We practice coordinated vulnerability disclosure
- **Timeline**: We aim to patch vulnerabilities within 90 days of report
- **Public disclosure**: After a patch is released, we'll publish a security advisory
- **Credit**: Security researchers will be credited for their discoveries

## Security Best Practices for Users

### Extension Installation

- **Install from official sources** only (Chrome Web Store, Firefox Add-ons, GitHub releases)
- **Verify the publisher** before installing
- **Keep the extension updated** to the latest version
- **Review permissions** requested by the extension

### Privacy & Data

- **Local-first by default**: AccessiCore runs locally and doesn't send data externally by default
- **No tracking**: We don't track your browsing or collect analytics
- **User control**: You control when and where the extension activates
- **Review the code**: As FOSS software, you can audit our code yourself

### Reporting Other Issues

For non-security issues:
- **Bug reports**: [GitHub Issues](https://github.com/yourusername/AccessiCore/issues)
- **Feature requests**: [GitHub Discussions](https://github.com/yourusername/AccessiCore/discussions)
- **Questions**: [GitHub Discussions](https://github.com/yourusername/AccessiCore/discussions)

## Security Update Process

When we release a security patch:

1. **Release the patch** immediately for critical vulnerabilities
2. **Publish a security advisory** on GitHub
3. **Notify users** through extension update mechanisms
4. **Update documentation** with any required user actions
5. **Post-mortem** (for serious vulnerabilities) explaining what happened and how we're preventing similar issues

## Security Features in AccessiCore

### Current Security Measures

- **Content Security Policy (CSP)**: Strict CSP to prevent XSS attacks
- **Minimal permissions**: We request only necessary browser permissions
- **Sandboxed execution**: Extension components run in isolated contexts
- **No remote code execution**: All code is bundled with the extension
- **Local-first processing**: No data sent to external servers by default
- **Secure communication**: HTTPS-only API calls (when cloud features are enabled)
- **Input validation**: All user inputs and DOM data are sanitized
- **Dependency scanning**: Regular automated scans for vulnerable dependencies

### Planned Security Enhancements

- **Automated security testing** in CI/CD pipeline
- **Regular penetration testing** by security researchers
- **Bug bounty program** (once we have funding)
- **Security audit** by independent third parties
- **Cryptographic signing** of releases

## Dependencies

We regularly:
- **Audit dependencies** for known vulnerabilities using `npm audit`
- **Update dependencies** to patched versions promptly
- **Review new dependencies** before adding them
- **Minimize dependencies** to reduce attack surface

Run `npm audit` to check for vulnerable dependencies yourself.

## Build Verification

You can verify the integrity of releases:

1. **Download the release** from GitHub Releases
2. **Check the SHA256 hash** (provided in release notes)
3. **Build from source** and compare with released version

```bash
# Build from source
git clone https://github.com/yourusername/AccessiCore.git
cd AccessiCore
git checkout v0.1.0  # or latest version tag
npm install
npm run build

# Compare with official release
sha256sum dist/*
```

## Security Hall of Fame

We recognize and thank security researchers who help keep AccessiCore safe:

<!-- This section will be populated as vulnerabilities are responsibly disclosed -->

*No vulnerabilities have been reported yet.*

---

## Contact

**Security Email**: security@accessicore.example.com  
**PGP Key**: [Available on request]

For general inquiries: accessicore@example.com

---

*Last Updated: February 2026*

**Thank you for helping keep AccessiCore and its users safe!** 🔒
