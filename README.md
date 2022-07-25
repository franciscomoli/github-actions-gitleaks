# Github Actions: Gitleaks

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/franciscomoli/github-actions-gitleaks)](https://github.com/franciscomoli/github-actions-gitleaks/releases)

Simplified Github action using Gitleaks.

# Example Workflow

```
name: Gitleaks
on: push

jobs:
  snyk:
    runs-on: ubuntu-latest
    steps: 
      - uses: actions/checkout@v2
      - name: Run Gitleaks
        uses: franciscomoli/github-actions-gitleaks@main
        with:
          depth: 1
      - uses: github/codeql-action/upload-sarif@v1
        with:
          sarif_file: gitleaks.sarif
```
