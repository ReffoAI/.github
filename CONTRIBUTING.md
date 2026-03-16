Contributing to Reffo
Thanks for your interest in contributing to Reffo! This guide applies to all repositories in the reffo-ai organization.
Contributor License Agreement
Before your first contribution can be merged, you must agree to our Individual Contributor License Agreement. By submitting a pull request, you confirm that you have read and agree to the CLA. CLA can be found at https://gist.github.com/arcio/4e7e50b2c4a041158f4a126a94aef071
Getting Started

Fork the repository
Clone your fork locally
Create a branch from main using the naming convention below
Make your changes and commit
Push to your fork
Open a Pull Request against main

Branch Naming
Use prefixed branch names:

feat/short-description — New features or enhancements
fix/short-description — Bug fixes
docs/short-description — Documentation changes

Examples: feat/offer-expiration, fix/dht-discovery-timeout, docs/api-auth-guide
Code Style
All JavaScript/TypeScript repositories use a shared linting configuration:

ESLint with the project's .eslintrc config
Prettier for formatting (config in .prettierrc)
Run npm run lint before committing
Run npm run format to auto-fix formatting

PRs that fail linting will not be merged.
Running Tests
bash# Install dependencies
npm install

# Run the test suite
npm test

# Run tests in watch mode
npm run test:watch
Each repo's README has additional setup instructions if needed (e.g., environment variables, local Supabase instance).
Protocol Changes (RFC Process)
Changes to the core protocol (schema, DHT behavior, negotiation flow) require community discussion before implementation.
To propose a protocol change:

Open an issue in the relevant repo with the [RFC] prefix in the title
Use this structure:

Summary — What you're proposing
Motivation — Why this change is needed
Design — How it would work
Tradeoffs — What are the downsides or alternatives considered


Allow at least 7 days for community feedback
A maintainer will label the issue rfc-approved or rfc-declined with reasoning

Do not open a PR for protocol changes without an approved RFC.
Pull Request Guidelines

Keep PRs focused — one feature or fix per PR
Write a clear description of what changed and why
Reference related issues (e.g., Closes #42)
Add or update tests for new functionality
Update documentation if your change affects public APIs or behavior

Reporting Bugs
Open an issue with:

Steps to reproduce
Expected behavior
Actual behavior
Environment details (OS, Node version, beacon version)

Questions?
Open a discussion in the relevant repository or reach out at hello@reffo.ai.
