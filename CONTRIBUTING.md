# Contributing Guide For eslint-plugin-aura

This page lists the operational governance model of this project, as well as the recommendations and requirements for how to best contribute to eslint-plugin-aura. We strive to obey these as best as possible. As always, thanks for contributing – we hope these guidelines make it easier and shed some light on our approach and processes.

# Governance Model

## Published but not supported

The intent and goal of open sourcing this project is because it may contain useful or interesting code/concepts that we wish to share with the larger open source community. Although occasional work may be done on it, we will not be looking for or soliciting contributions.

# Issues, requests & ideas

Use GitHub Issues page to submit issues, enhancement requests and discuss ideas.

### Bug Reports and Fixes

- If you find a bug, please search for it in the [Issues](https://github.com/forcedotcom/eslint-plugin-aura/issues), and if it isn't already tracked,
  [create a new issue](https://github.com/forcedotcom/eslint-plugin-aura/issues/new). Fill out the "Bug Report" section of the issue template. Even if an Issue is closed, feel free to comment and add details, it will still
  be reviewed.
- Issues that have already been identified as a bug (note: able to reproduce) will be labelled `bug`.
- If you'd like to submit a fix for a bug, [send a Pull Request](#creating_a_pull_request) and mention the Issue number.
- Include tests that isolate the bug and verifies that it was fixed.

### New Features

- If you'd like to add new functionality to this project, describe the problem you want to solve in a [new Issue](https://github.com/forcedotcom/eslint-plugin-aura/issues/new).
- Issues that have been identified as a feature request will be labelled `enhancement`.
- If you'd like to implement the new feature, please wait for feedback from the project
  maintainers before spending too much time writing the code. In some cases, `enhancement`s may
  not align well with the project objectives at the time.

### Tests, Documentation, Miscellaneous

- If you'd like to improve the tests, you want to make the documentation clearer, you have an
  alternative implementation of something that may have advantages over the way its currently
  done, or you have any other change, we would be happy to hear about it!
- If its a trivial change, go ahead and [send a Pull Request](#creating_a_pull_request) with the changes you have in mind.
- If not, [open an Issue](https://github.com/forcedotcom/eslint-plugin-aura/issues/new) to discuss the idea first.

If you're new to our project and looking for some way to make your first contribution, look for
Issues labelled `good first contribution`.

# Development Setup

## Prerequisites

- Node.js >= 12.0.0
- npm

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/forcedotcom/eslint-plugin-aura.git
   cd eslint-plugin-aura
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Install git hooks:
   ```bash
   npm run prepare
   ```

## Available Scripts

- `npm run lint` - Run ESLint on the codebase
- `npm run format` - Format code using Prettier
- `npm run format:check` - Check if code is properly formatted
- `npm test` - Run the test suite using Mocha

## Project Structure

- `lib/` - Main source code
  - `rules/` - ESLint rules for Aura
  - `locker/` - Lightning Locker specific rules
  - `configs/` - ESLint configurations
  - `index.js` - Plugin entry point
  - `util.js` - Utility functions
- `test/` - Test files
- `docs/` - Rule documentation

# Contribution Checklist

- [x] Clean, simple, well styled code
- [x] Commits should be atomic and messages must be descriptive. Related issues should be mentioned by Issue number.
- [x] Comments
  - Module-level & function-level comments.
  - Comments on complex blocks of code or algorithms (include references to sources).
- [x] Tests
  - The test suite must be complete and pass (`npm test`)
  - Increase code coverage, not decrease it.
  - Follow the existing test patterns in the `test/` directory.
- [x] Code Quality
  - Code must pass linting (`npm run lint`)
  - Code must be properly formatted (`npm run format:check`)
- [x] Dependencies
  - Minimize number of dependencies.
  - Prefer Apache 2.0, BSD3, MIT, ISC and MPL licenses.
- [x] Reviews
  - Changes must be approved via peer code review

# Creating a Pull Request

1. **Ensure the bug/feature was not already reported** by searching on GitHub under Issues. If none exists, create a new issue so that other contributors can keep track of what you are trying to add/fix and offer suggestions (or let you know if there is already an effort in progress).
2. **Fork** the repository on GitHub.
3. **Clone** the forked repo to your machine.
4. **Create** a new branch to contain your work (e.g. `git checkout -b fix-issue-11`)
5. **Make your changes** and ensure all tests pass:
   ```bash
   npm test
   npm run lint
   npm run format:check
   ```
6. **Commit** changes to your own branch with descriptive commit messages.
7. **Push** your work back up to your fork.
8. **Submit** a Pull Request against the `main` branch and refer to the issue(s) you are fixing. Try not to pollute your pull request with unintended changes. Keep it simple and small.
9. **Sign** the Salesforce CLA (you will be prompted to do so when submitting the Pull Request)

> **NOTE**: Be sure to [sync your fork](https://help.github.com/articles/syncing-a-fork/) before making a pull request.

# Contributor License Agreement ("CLA")

In order to accept your pull request, we need you to submit a CLA. You only need
to do this once to work on any of Salesforce's open source projects.

Complete your CLA here: <https://cla.salesforce.com/sign-cla>

# Issues

We use GitHub issues to track public bugs. Please ensure your description is
clear and has sufficient instructions to be able to reproduce the issue.

# Code of Conduct

Please follow our [Code of Conduct](CODE_OF_CONDUCT.md).

# License

By contributing your code, you agree to license your contribution under the terms of our project [LICENSE](LICENSE) and to sign the [Salesforce CLA](https://cla.salesforce.com/sign-cla)
