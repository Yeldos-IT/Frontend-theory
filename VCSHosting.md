# Advanced GitHub Features

## 1. GitHub Actions (CI/CD)
GitHub Actions is a powerful tool for automating workflows, such as building, testing, and deploying projects.

### Example Workflow for Testing:
```yaml
name: Node.js CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Install dependencies
        run: npm install
      - name: Run tests
        run: npm test
```
You can explore thousands of pre-built Actions in the [GitHub Marketplace](https://github.com/marketplace).

---

## 2. GitHub Pages
GitHub Pages provides free hosting for static websites directly from your repositories.

### How to Enable:
1. Go to **Settings → Pages** in your repository.
2. Choose a branch (e.g., `main` or `gh-pages`) to host your website.
3. Your website will be accessible at: `https://<username>.github.io/<repo>`.

---

## 3. Project Boards
GitHub Project Boards offer a Kanban-style view to plan and manage tasks within your repository.

### Features:
- Add **Issues** or **Pull Requests** as cards on the board.
- Use columns like `To Do`, `In Progress`, and `Done` to track progress.
- Customize workflows with automation rules.

---

## 4. Advanced Pull Request Features
- **Draft Pull Requests:** Create PRs that are not ready for review or merging yet.
- **Automatic Merging:** Set conditions (e.g., passing tests) for PRs to merge automatically.

---

## 5. Insights and Analytics
GitHub provides tools to monitor and analyze your repository:
- **Contributors:** View detailed statistics about contributions.
- **Community Health:** Assess repository health (e.g., presence of README, CONTRIBUTING.md).

---

## 6. Secrets Management
- Store sensitive data like API tokens or credentials securely in your repository.
- Use these secrets in GitHub Actions workflows without exposing them.

---

## 7. Dependabot
Dependabot helps keep your dependencies secure and up-to-date by automatically creating pull requests for updates.

---
