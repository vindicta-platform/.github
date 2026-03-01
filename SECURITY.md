# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.x.x   | ✅ Yes             |
| < 1.0   | ❌ No (pre-release) |

## Reporting a Vulnerability

**⚠️ Please do NOT open a public GitHub issue for security vulnerabilities.**

If you discover a security vulnerability within any Vindicta Platform repository, please report it responsibly using one of the following methods:

### Preferred: GitHub Security Advisories

1. Navigate to the affected repository
2. Go to the **Security** tab
3. Click **Report a vulnerability**
4. Fill out the advisory form with as much detail as possible

### Alternative: Email

If you cannot use GitHub Security Advisories, email **security@vindicta-platform.dev** with:

- A description of the vulnerability
- Steps to reproduce
- Affected repository and version
- Potential impact assessment

## Response Timeline

| Phase | Timeline |
|-------|----------|
| Acknowledgment | Within **48 hours** |
| Initial assessment | Within **5 business days** |
| Fix development | Within **30 days** (severity dependent) |
| Public disclosure | After fix is released |

## Scope

This security policy applies to all repositories under the [vindicta-platform](https://github.com/vindicta-platform) organization.

### In Scope

- All source code in organization repositories
- GitHub Actions workflows and CI/CD pipelines
- API endpoints and authentication mechanisms
- Cryptographic implementations (Dice Engine, Entropy Buffer)
- Configuration files that may contain sensitive defaults

### Out of Scope

- Social engineering attacks
- Denial of service attacks
- Issues in third-party dependencies (report upstream, then notify us)

## Disclosure Policy

We follow a **coordinated disclosure** model:

1. Reporter submits vulnerability privately
2. We confirm and assess the issue
3. We develop and test a fix
4. We release the fix and publish an advisory
5. Reporter is credited (unless they prefer anonymity)

## Recognition

We appreciate responsible disclosure and will credit reporters in our security advisories unless they prefer to remain anonymous.

---

*This policy is maintained by the Vindicta Platform architects.*
