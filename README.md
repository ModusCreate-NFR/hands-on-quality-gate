# Hands-on Quality Gate

This repository contains a sample project to demonstrate the use of GitHub Actions for code quality checks.

## Workflows

### JSCPD Code Duplication Check

The `jscpd.yml` workflow is a reusable workflow that checks for code duplication using JSCPD.

#### Inputs

- `threshold`: The threshold value for code duplication. Default is 2.

#### Usage

To use the `jscpd.yml` workflow in your repository, add the following to your workflow file:

```yaml
jobs:
  jscpd:
    name: JSCPD
    uses: ModusCreate-NFR/hands-on-quality-gate/.github/workflows/jscpd.yml
    with:
      threshold: 2
```

### Lint

The `lint.yml` workflow runs the MegaLinter and JSCPD checks on pull requests to the `main` branch.

## Legal

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
