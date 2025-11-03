# GitHub Universe 2025 - Conference Highlights

My highlights from GitHub Universe 2025, presented as interactive slides.

## 🎯 View Slides

**Live Presentation:** [https://mirestrepo.github.io/github-universe-25/](https://mirestrepo.github.io/github-universe-25/)

## 📝 Topics Covered

- Agent HQ & Claude Integration
- Copilot Features & Plan Mode
- Agentic Code Review & Workflows
- Security Campaigns & Code Quality
- Model Context Protocol (MCP)
- Multi-Agent Orchestration
- GitHub Engineering Practices
- Community Impact & Accessibility

## 🛠️ Local Development

### Prerequisites
- Node.js 18+ and npm

### Setup

```bash
# Install dependencies
npm install

# Start development server with live preview
npm run dev

# Build slides to HTML
npm run build

# Watch mode (auto-rebuild on changes)
npm run watch

# Build PDF version
npm run build:pdf
```

### Preview Locally

After running `npm run build`, open `index.html` in your browser to view the slides.

## 📂 Project Structure

```
.
├── slides.md              # Marp markdown source
├── raw-notes.txt          # Original conference notes
├── index.html             # Generated slides (after build)
├── package.json           # Dependencies & scripts
└── .github/workflows/     # Auto-deployment to GitHub Pages
```

## 🚀 Deployment

Slides are automatically deployed to GitHub Pages when changes are pushed to the `main` branch via GitHub Actions.

## 🔧 Technology Stack

- **[Marp](https://marp.app/)** - Markdown Presentation Ecosystem
- **Theme:** Gaia (GitHub-style)
- **Hosting:** GitHub Pages
- **CI/CD:** GitHub Actions

## 📄 License

MIT
