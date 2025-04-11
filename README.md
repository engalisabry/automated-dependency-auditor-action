# Automated Dependency Auditor Action

This GitHub Action automatically audits your project's dependencies and generates a markdown report with current and latest version information.

## Usage

You can integrate this action into your GitHub workflow as follows:

```yaml
name: Dependency Audit Workflow

on: [push]

jobs:
  audit:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Run Dependency Auditor
        uses: engalisabry/automated-dependency-auditor-action@v1
        with:
          # any inputs (if needed) can be added here

