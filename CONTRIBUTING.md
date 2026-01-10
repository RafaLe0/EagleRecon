# Contributing to EagleRecon

EagleRecon is a security-focused, open-source Threat Intelligence Correlation Engine written in Rust.
I welcome contributions that improve reliability, security, performance, and usability.

---

## Project Philosophy

EagleRecon is built with the following principles in mind:

- **Security first** – correctness over features
- **Low resource footprint** – optimized for Raspberry Pi and homelabs
- **Readable and maintainable Rust**
- **Explicit behavior** – no hidden magic
- **Reproducible builds**

If your contribution aligns with these principles, it is very welcome.

---

## Ways to Contribute

You can contribute by:

- Reporting bugs
- Suggesting new features
- Improving documentation
- Writing tests
- Adding new IOC collectors
- Improving correlation or scoring logic
- Reviewing pull requests

---

## Reporting Bugs

Before opening a bug report:

1. Ensure the issue is reproducible on the latest version
2. Search existing issues to avoid duplicates

Please include:
- EagleRecon version
- OS and architecture (x86_64, ARM64, Raspberry Pi model)
- Configuration used
- Logs or error messages
- Expected vs actual behavior

---

## Feature Requests

Feature requests should:
- Be compatible with low-resource environments
- Avoid unnecessary complexity

Please explain:
- The problem you are trying to solve
- Why existing features are insufficient
- How you envision the solution

---

## Steps
1. Fork the repository
2. Create a feature or fix branch from `dev`
3. Commit your changes (see commit rules below)
4. Open a Pull Request targeting `dev`

---

## Code Standards

### Rust
- Follow standard Rust idioms
- Run `cargo fmt` before committing
- Avoid `unsafe` unless strictly necessary
- Prefer explicit error handling (`Result`, `thiserror`, `anyhow`)
- No hardcoded secrets or tokens

### Architecture
- Keep modules small and focused
- Avoid tight coupling between collectors, correlation, and storage
- New collectors must implement the common IOC interface

---

## Tests

- All new features should include tests when applicable
- Bug fixes should include regression tests
- Run before submitting:
```bash
cargo fmt
cargo clippy
cargo test
```
