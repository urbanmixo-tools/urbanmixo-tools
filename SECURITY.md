# Security Policy & Vulnerability Disclosure

Urban Mixo is built on a strict **zero-trust, 100% client-side computing architecture**. We take code integrity, execution sandboxing, and algorithmic precision seriously.

## Supported Versions

Security and mathematical accuracy updates are applied continuously to active releases:

| Version | Supported          | Status |
| ------- | ------------------ | ------ |
| 1.0.x   | :white_check_mark: | Production |
| < 1.0   | :x:                | Deprecated |

## Threat Model & Architecture

Because Urban Mixo possesses **zero backend databases and zero remote APIs for tool computation**, standard server-side attack vectors (e.g. SQL injection, remote credential exfiltration, database breaches) are structurally eliminated.

Our primary security posture focuses on:
1. **Client-Side Sandbox Integrity:** Preventing Cross-Site Scripting (DOM-XSS) inside browser execution contexts.
2. **Hardware CSPRNG Verification:** Guaranteeing that random number and password generation utilize uncompromised native `crypto.getRandomValues()` entropy without modulo bias.
3. **Data Isolation:** Ensuring that personal inputs (financial balances, clinical measurements, source code diffs) remain strictly in ephemeral device memory and are never transmitted over network protocols.

## Reporting a Vulnerability

If you discover an algorithmic discrepancy, a cryptographic flaw, or a DOM execution vulnerability:

1. **Do not open a public GitHub issue.**
2. Send a detailed report directly to our security and editorial desk at:
   **`contact@urbanmixo.online`**
3. Please include:
   - The affected tool URL or module name.
   - A description of the mathematical variance or security bug.
   - Steps to reproduce or input parameters used.

### Response Timeline
- **Triage & Acknowledgment:** Within 24–48 hours.
- **Remediation & Patching:** Within 72 hours of verification.
