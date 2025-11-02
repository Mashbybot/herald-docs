# Herald Documentation

Official documentation for [Herald](https://github.com/Mashbybot/herald), the Discord bot for Hunter: The Reckoning 5th Edition.

## 🌐 View the Docs

**Live Documentation:** https://Mashbybot.github.io/herald-docs/

## 📝 About

This documentation is built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and automatically deployed to GitHub Pages.

## 🛠️ Local Development

Want to contribute or preview changes locally?

### Prerequisites

- Python 3.8+
- pip

### Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/herald-docs.git
cd herald-docs

# Install dependencies
pip install mkdocs-material

# Serve locally
mkdocs serve
```

Visit `http://127.0.0.1:8000` to view the documentation locally.

### Building

```bash
# Build static site
mkdocs build

# Deploy to GitHub Pages (automatic via GitHub Actions)
mkdocs gh-deploy
```

## 📂 Structure

```
herald-docs/
├── docs/                  # Documentation content
│   ├── index.md          # Homepage
│   ├── guides/           # User guides
│   ├── commands/         # Command reference
│   ├── h5e/              # H5E integration docs
│   ├── admin/            # Server admin guides
│   ├── support/          # Support resources
│   ├── stylesheets/      # Custom CSS
│   └── javascripts/      # Custom JS
├── overrides/            # Theme overrides
├── .github/
│   └── workflows/
│       └── deploy.yml    # Auto-deployment
└── mkdocs.yml            # MkDocs configuration
```

## ✍️ Contributing

Contributions are welcome! To contribute:

1. Fork this repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Test locally with `mkdocs serve`
5. Commit your changes (`git commit -am 'Add new guide'`)
6. Push to the branch (`git push origin feature/improvement`)
7. Create a Pull Request

### Writing Guidelines

- Use clear, concise language
- Include code examples for commands
- Add screenshots where helpful
- Follow the existing structure and style
- Test all command examples before submitting

## 🎨 Theme

The documentation uses MkDocs Material with a custom Hunter: The Reckoning theme:

- Dark mode by default
- Red/black color scheme
- Custom syntax highlighting
- Mobile-responsive design

## 📄 License

This documentation is licensed under MIT License - see the LICENSE file for details.

## 🔗 Links

- **Herald Bot:** https://github.com/Mashbybot/herald
- **Support Server:** https://discord.gg/9bEZk6ARG9
- **MkDocs Material:** https://squidfunk.github.io/mkdocs-material/

## 💬 Support

Need help with the documentation?

- Open an issue on this repository
- Join our [Discord server](https://discord.gg/9bEZk6ARG9)
- Contact the maintainers

---

Built with ❤️ for the Hunter: The Reckoning community
