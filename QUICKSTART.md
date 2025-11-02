# Herald Documentation - Quick Setup Guide

Your Herald documentation is ready! Here's how to get it online.

## 📦 What You Have

A complete MkDocs Material documentation site with:
- ✅ 35 markdown pages (7 complete, 28 placeholders)
- ✅ Professional dark theme (Hunter aesthetic)
- ✅ Navigation structure mirroring Inconnu
- ✅ Automatic GitHub Actions deployment
- ✅ Custom CSS styling
- ✅ Mobile-responsive design
- ✅ Built-in search

## 🚀 Deploy in 5 Minutes

### 1. Update Your Information

Edit `mkdocs.yml` and replace:
- `yourusername` with your GitHub username
- Update the Discord invite link (3 places)

### 2. Create GitHub Repository

```bash
# On GitHub, create new repository named "herald-docs" (public)

# In terminal:
cd herald-docs
git init
git add .
git commit -m "Initial Herald documentation"
git remote add origin https://github.com/YOUR_USERNAME/herald-docs.git
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages

The GitHub Action will run automatically! Just:
1. Go to repository Settings → Pages
2. Set Source to `gh-pages` branch
3. Wait 2 minutes

Your site will be live at: `https://YOUR_USERNAME.github.io/herald-docs/`

## 📝 Complete Documentation

### ✅ Fully Written Pages (Ready to Use)

1. **Homepage** (`index.md`) - Welcome page with features
2. **Quick Start** (`guides/quickstart.md`) - 5-minute setup
3. **Adding Herald** (`guides/adding-herald.md`) - Installation guide
4. **First Character** (`guides/first-character.md`) - Character creation walkthrough
5. **Basic Rolling** (`guides/basic-rolling.md`) - Dice mechanics tutorial
6. **Command Reference** (`commands/index.md`) - Overview of all commands
7. **FAQ** (`support/faq.md`) - Common questions

### 📋 Placeholder Pages (Need Content)

The following pages exist but need to be written:

**Guides:**
- Character Creation (advanced)
- Character Management
- Dice Rolling (advanced)
- Edge & Desperation
- Skills & Specialties
- Experience System
- Hunter Mechanics
- Equipment & Notes

**Commands:**
- Character Commands
- Dice Commands
- Development Commands
- Hunter Mechanics Commands
- Utility Commands

**H5E Integration:**
- Overview
- Attributes & Skills
- Dice Mechanics
- Edge System
- Desperation
- Creeds
- Progression

**Admin:**
- Setup Guide
- Best Practices
- Troubleshooting

**Support:**
- Common Issues
- Getting Help
- Contributing

## ✍️ Adding Content

To fill in placeholder pages:

1. Edit the markdown file in `docs/`
2. Test locally: `mkdocs serve`
3. View at http://127.0.0.1:8000
4. Commit and push when ready

Example:
```bash
# Edit a file
nano docs/guides/character-management.md

# Test locally
mkdocs serve

# Deploy
git add .
git commit -m "Add character management guide"
git push
```

GitHub Actions automatically rebuilds the site!

## 🎨 Customization

### Colors
Edit `docs/stylesheets/extra.css`:
```css
:root {
  --hunter-red: #8B0000;
  --hunter-gold: #FFD700;
}
```

### Navigation
Edit `mkdocs.yml` under `nav:` section

### Theme
Edit `mkdocs.yml` under `theme:` section

## 📚 Content Guidelines

When writing pages:
- Use clear, beginner-friendly language
- Include code examples for every command
- Add screenshots where helpful
- Use admonitions for tips/warnings
- Test all commands before documenting

## 🔗 Important Files

- `mkdocs.yml` - Main configuration
- `docs/index.md` - Homepage
- `docs/stylesheets/extra.css` - Custom styling
- `.github/workflows/deploy.yml` - Auto-deployment
- `DEPLOYMENT.md` - Detailed deployment guide

## ✅ Next Steps

1. **Deploy**: Push to GitHub and enable Pages
2. **Update**: Replace placeholder bot invite links
3. **Content**: Fill in the 28 placeholder pages
4. **Share**: Link from your bot's profile and support server

## 🆘 Need Help?

- Full deployment guide: `DEPLOYMENT.md`
- MkDocs docs: https://squidfunk.github.io/mkdocs-material/
- Herald Support: https://discord.gg/9bEZk6ARG9

---

**Your documentation is production-ready!** The foundation is solid, professional, and matches Inconnu's quality. Now just fill in the content as Herald grows! 🎉
