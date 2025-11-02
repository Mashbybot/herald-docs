# Herald Documentation Deployment Checklist

Use this checklist to deploy your documentation to GitHub Pages.

## Pre-Deployment Checklist

### ✅ Step 1: Update Configuration

- [ ] Open `mkdocs.yml`
- [ ] Replace `yourusername` with your actual GitHub username (3 places):
  - `site_url: https://yourusername.github.io/herald-docs/`
  - `repo_name: yourusername/herald`
  - `repo_url: https://github.com/yourusername/herald`
- [ ] Update social link in `extra.social` section

### ✅ Step 2: Update Bot Invite Links

- [ ] Get your bot invite URL from Discord Developer Portal
- [ ] Replace `YOUR_BOT_ID` in these files:
  - [ ] `docs/guides/adding-herald.md` (line ~12)
  - [ ] `docs/guides/quickstart.md` (line ~10)
- [ ] Use this format: `https://discord.com/oauth2/authorize?client_id=YOUR_BOT_ID&permissions=537135104&scope=bot+applications.commands`

### ✅ Step 3: Verify Local Build

```bash
cd herald-docs
pip install mkdocs-material
mkdocs serve
```

- [ ] Open http://127.0.0.1:8000
- [ ] Check homepage loads
- [ ] Test navigation links
- [ ] Verify search works
- [ ] Check mobile view (resize browser)

## Deployment Checklist

### ✅ Step 4: Create GitHub Repository

- [ ] Go to https://github.com/new
- [ ] Repository name: `herald-docs`
- [ ] Visibility: **Public** (required for free GitHub Pages)
- [ ] Do NOT initialize with README
- [ ] Click "Create repository"

### ✅ Step 5: Push to GitHub

```bash
cd herald-docs
git init
git add .
git commit -m "Initial Herald documentation"
git remote add origin https://github.com/YOUR_USERNAME/herald-docs.git
git branch -M main
git push -u origin main
```

- [ ] All files pushed successfully
- [ ] Repository shows all files on GitHub
- [ ] GitHub Actions workflow appears in Actions tab

### ✅ Step 6: Enable GitHub Pages

- [ ] Go to repository Settings → Pages
- [ ] Source: Deploy from a branch
- [ ] Branch: `gh-pages` / (root)
- [ ] Click Save
- [ ] Wait 2-5 minutes for deployment

### ✅ Step 7: Verify Deployment

- [ ] Visit `https://YOUR_USERNAME.github.io/herald-docs/`
- [ ] Homepage loads correctly
- [ ] Navigation works
- [ ] Search functions
- [ ] All styles applied
- [ ] Mobile view works

## Post-Deployment Checklist

### ✅ Step 8: Update Herald Bot

- [ ] Add docs link to bot's Discord status
- [ ] Update bot profile with docs link
- [ ] Post announcement in support server
- [ ] Add to bot listing sites (top.gg, etc.)

### ✅ Step 9: Test User Journey

- [ ] Try Quick Start guide from scratch
- [ ] Verify all command examples work
- [ ] Check that links to Discord server work
- [ ] Test search for common queries

### ✅ Step 10: Plan Content Updates

- [ ] List which placeholder pages to write first
- [ ] Gather screenshots needed
- [ ] Note any outdated information
- [ ] Set up content update schedule

## Ongoing Maintenance Checklist

### Weekly:
- [ ] Check for broken links
- [ ] Review user questions in Discord
- [ ] Update FAQ based on common issues

### When Herald Updates:
- [ ] Update command documentation
- [ ] Add new features to guides
- [ ] Update screenshots if UI changed
- [ ] Test all command examples

### Monthly:
- [ ] Review analytics (if added)
- [ ] Update Quick Start if needed
- [ ] Improve based on user feedback
- [ ] Expand placeholder pages

## Troubleshooting Checklist

### Site Not Loading?
- [ ] Wait 5-10 minutes (GitHub Pages can be slow)
- [ ] Check Actions tab for deployment errors
- [ ] Verify gh-pages branch exists
- [ ] Check Settings → Pages is enabled
- [ ] Try incognito/private browsing

### CSS Not Applied?
- [ ] Clear browser cache
- [ ] Check `extra.css` is in `docs/stylesheets/`
- [ ] Verify `extra_css` in `mkdocs.yml`
- [ ] Rebuild: `mkdocs build --clean`

### Links Broken?
- [ ] Check file paths are correct
- [ ] Verify markdown links use `.md` extension
- [ ] Test with `mkdocs serve` locally
- [ ] Check for typos in navigation

### GitHub Action Failed?
- [ ] Check workflow file syntax
- [ ] Verify Python version compatibility
- [ ] Check for missing dependencies
- [ ] Review error logs in Actions tab

## Quick Reference

### Build Locally:
```bash
mkdocs serve
```

### Deploy Manually:
```bash
mkdocs gh-deploy
```

### Update Content:
```bash
# Edit files in docs/
git add .
git commit -m "Update documentation"
git push
```

## Success Criteria

Your deployment is successful when:

- ✅ Site loads at your GitHub Pages URL
- ✅ All navigation links work
- ✅ Search returns results
- ✅ Mobile view displays correctly
- ✅ Quick Start guide works end-to-end
- ✅ Discord links are correct
- ✅ No console errors in browser

## Need Help?

- **Setup issues**: See `DEPLOYMENT.md`
- **Content questions**: See `PROJECT_SUMMARY.md`
- **Quick start**: See `QUICKSTART.md`
- **MkDocs help**: https://squidfunk.github.io/mkdocs-material/
- **GitHub Pages**: https://docs.github.com/en/pages

---

## Final Check

Before marking complete, verify:

- [ ] All pre-deployment steps done
- [ ] All deployment steps done
- [ ] Site is live and accessible
- [ ] All post-deployment steps done
- [ ] Bookmark for future updates

---

**Once this checklist is complete, your documentation is live!** 🎉

Print or save this checklist for reference during deployment.
