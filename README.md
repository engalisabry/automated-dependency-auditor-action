# 🔍 Automated Dependency Auditor GitHub Action

Easily audit your `package.json` dependencies in your GitHub project and generate a clean, readable Markdown report that shows outdated packages and their latest versions. Perfect for maintaining healthy dependencies and staying secure!

📦 **Published on GitHub Marketplace:**  
👉 [View on GitHub Marketplace](https://github.com/marketplace/actions/automated-dependency-auditor)

---

## ✨ Features

- 📄 Generates a clear Markdown report of outdated dependencies
- ✅ Differentiates between up-to-date and outdated packages
- 📊 Shows progress percentage while generating the report
- 🧹 Auto-formats the report into easy-to-read columns
- 🪄 Zero setup once integrated into your workflow

---

## 🚀 Usage

### 1. Add to your workflow

Add the following to `.github/workflows/dependency-audit.yml`:

```yaml
name: Dependency Audit

on:
  schedule:
    - cron: '0 0 * * 0' # Every Sunday at midnight
  workflow_dispatch:

jobs:
  audit:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Use Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'

      - name: Run Dependency Auditor
        uses: engalisabry/automated-dependency-auditor-action@v1.0.0

