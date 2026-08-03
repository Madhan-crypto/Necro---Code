# Necro - Code 🛠️

**Autonomous code rejuvenation for modern engineering teams.**

Necro - Code is an autonomous code health agent designed to eliminate technical debt and optimize repository performance. As codebases scale, they naturally accumulate dead code, legacy anti-patterns, and unreachable logical blocks—wasting up to 30% of engineering velocity on maintenance overhead. While traditional linters merely flag these structural flaws and inflate backlogs, Necro - Code closes the loop by automatically generating the actual fixes.

---

## 🚀 Key Features

* **Continuous Scanning:** Deep static and semantic analysis to map out dead branches and anti-patterns.
* **Context-Aware Refactoring:** Uses a hybrid architecture of Abstract Syntax Tree (AST) parsing and code intelligence to formulate optimal structural improvements.
* **Automated Pull Requests:** Packages fixes into clean, minimal, and fully isolated refactor diffs delivered directly to your workflow.
* **Zero-Hallucination Verification:** Built-in safety boundaries ensure generated refactor diffs never break existing runtime logic.

---

## 📦 Installation

To get started with DiffForge locally or in your development environment:

```bash
# Install the Necro - Code CLI globally via npm
npm install -g @Necro - Code/cli

# Or install via pip if using the Python distribution
pip install necro-code-cli
```

---

## ⚙️ Configuration

Initialize DiffForge in the root directory of your project to create a default configuration file:

```bash
necro-code init
```

This will generate a `.necro-code.json` configuration file:

```json
{
  "languages": ["typescript", "python", "go"],
  "exclude": ["**/node_modules/**", "**/dist/**"],
  "rules": {
    "dead-code": "remove",
    "anti-patterns": "refactor",
    "complexity-threshold": "high"
  },
  "automation": {
    "auto-pr": true,
    "target-branch": "main"
  }
}
```

---

## 🛠️ CI/CD Workflow Integration

Integrate Necro - Code directly into your **GitHub Actions** workflow by adding the following step to your `.github/workflows/main.yml`:

```yaml
name: Continuous Code Rejuvenation

on:
  schedule:
    - cron: '0 0 * * 1' # Run every Monday at midnight
  workflow_dispatch:

jobs:
  rejuvenate:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Code
        uses: actions/checkout@v4

      - name: Run DiffForge Scan & Refactor
        uses: diffforge/action@v1
        with:
          api-key: ${{ secrets.DIFFFORGE_API_KEY }}
          github-token: ${{ secrets.GITHUB_TOKEN }}
```

---

## 🤝 Contributing

We welcome contributions from the developer community! If you would like to help improve DiffForge:

1. **Fork** the repository.
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`).
3. **Commit your changes** (`git commit -m 'Add some amazing feature'`).
4. **Push to the branch** (`git push origin feature/amazing-feature`).
5. **Open a Pull Request** against the `main` branch.

Please ensure your code passes all internal linters and includes appropriate test coverage.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
