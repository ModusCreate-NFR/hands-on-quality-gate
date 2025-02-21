# JSCPD Code Duplication Check GitHub Action

This GitHub Action runs JSCPD (JavaScript Copy/Paste Detector) to check for 
code duplication in your project. It generates reports in console, markdown, 
and SARIF formats and uploads them as artifacts.

Additionally, it comments the results on the pull request.

## Inputs

- `threshold`: The threshold of duplicated code for JSCPD. Default is `2`.

## Example Usage

To use this action in your workflow, add the following to your `.github/workflows` directory:

```yaml
name: JSCPD Code Duplication Check

on:
  pull_request:
    branches:
      - main

jobs:
  jscpd:
    name: "Lint - Copy/Paste Detector"
    uses: ModusCreate-NFR/hand-on-quality-gate/jscpd-action.yml
    with:
      threshold: '5'
```

This example sets the threshold to `5`. You can adjust the threshold value as needed.

## Development

Note that the `node_modules` directory is vendored in the repository intentionally
to make running the action faster. If you update the version of `jscpd` in `package.json`
you must do an `npm install` and commit the updated `node_modules` directory.

## Legal

Copyright 2025 Modus Create. [MIT Licensed](LICENSE).
