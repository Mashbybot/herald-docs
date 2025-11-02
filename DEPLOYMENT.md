# Deploying Herald Documentation to GitHub Pages

Step-by-step guide to deploy your Herald documentation.

---

## Prerequisites

- GitHub account
- Git installed locally
- MkDocs Material installed (`pip install mkdocs-material`)

---

## Step 1: Update Configuration

Before deploying, update `mkdocs.yml` with your information:

```yaml
# Update these fields:
site_url: https://YOUR_USERNAME.github.io/herald-docs/
repo_name: YOUR_USERNAME/herald
repo_url: https://github.com/YOUR_USERNAME/herald

# In the extra section, update:
extra:
  social:
    - icon: fontawesome/brands/github
      link: https://github.com/YOUR_USERNAME/herald
```

Replace `YOUR_USERNAME` with your GitHub username.

---

## Step 2: Update Bot Invite Link

In these files, replace the placeholder bot invite link:

**Files to update:**
- `docs/guides/adding-herald.md`
- `docs/guides/quickstart.md`

**Replace:**
```
https://discord.com/oauth2/authorize?client_id=YOUR_BOT_ID&permissions=537135104&scope=bot+applications.commands
```

**With your actual bot invite URL** from the Discord Developer Portal.

---

## Step 3: Create GitHub Repository

1. Go to https://github.com/new
2. Name it `herald-docs` (or any name you prefer)
3. Set to **Public** (required for GitHub Pages)
4. Don't initialize with README (we already have one)
5. Click **Create repository**

---

## Step 4: Push Documentation

In your local `herald-docs` directory:

```bash
# Initialize git (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial Herald documentation"

# Add remote (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/herald-docs.git

# Push
git branch -M main
git push -u origin main
```

---

## Step 5: Enable GitHub Pages

### Automatic Deployment (Recommended)

The GitHub Actions workflow is already configured! It will automatically deploy when you push to main.

**To verify:**
1. Go to your repository on GitHub
2. Click **Actions** tab
3. You should see "Deploy Herald Docs" workflow running
4. Wait for it to complete (usually 1-2 minutes)

### Manual Deployment (Alternative)

If you prefer manual deployment:

```bash
# Build and deploy
mkdocs gh-deploy
```

This creates a `gh-pages` branch and pushes the built site.

---

## Step 6: Configure GitHub Pages Settings

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Source", select:
   - Branch: `gh-pages`
   - Folder: `/ (root)`
4. Click **Save**

---

## Step 7: Access Your Documentation

After 1-2 minutes, your documentation will be live at:

```
https://YOUR_USERNAME.github.io/herald-docs/
```

Visit the URL to verify everything works!

---

## Updating Documentation

### Make Changes Locally

1. Edit markdown files in `docs/`
2. Test locally: `mkdocs serve`
3. Preview at http://127.0.0.1:8000

### Deploy Changes

```bash
# Add changes
git add .

# Commit
git commit -m "Update documentation"

# Push
git push

# If using automatic deployment, you're done!
# If using manual deployment:
mkdocs gh-deploy
```

---

## Troubleshooting

### Site Not Showing

**Wait 5-10 minutes** - GitHub Pages can take time to update.

**Check Actions:**
- Go to **Actions** tab
- Verify the workflow completed successfully
- Check for error messages

**Verify Settings:**
- Settings → Pages should show "Your site is published at..."
- Branch should be `gh-pages`

### 404 Error

**Check `site_url` in mkdocs.yml:**
```yaml
site_url: https://YOUR_USERNAME.github.io/herald-docs/
```

Make sure the URL matches exactly.

**Rebuild and deploy:**
```bash
mkdocs gh-deploy --force
```

### CSS Not Loading

**Clear browser cache** or try incognito mode.

### Images Not Showing

Images must be in `docs/` directory:
```
docs/
  images/
    screenshot.png
```

Reference in markdown:
```markdown
![Description](images/screenshot.png)
```

---

## Custom Domain (Optional)

Want `docs.herald.app` instead of `username.github.io/herald-docs`?

### 1. Buy Domain

Purchase a domain from:
- Namecheap
- Google Domains
- Cloudflare
- Any registrar

### 2. Add CNAME File

Create `docs/CNAME`:
```
docs.herald.app
```

### 3. Configure DNS

In your domain registrar, add a CNAME record:

```
Type: CNAME
Name: docs
Value: YOUR_USERNAME.github.io
```

### 4. Update GitHub Pages

1. Go to Settings → Pages
2. Under "Custom domain", enter: `docs.herald.app`
3. Wait 24 hours for DNS propagation
4. Enable "Enforce HTTPS" (recommended)

---

## Best Practices

### Version Control

- Commit often with clear messages
- Use branches for major changes
- Review changes before deploying

### Content Guidelines

- Test links before pushing
- Include code examples
- Add screenshots where helpful
- Keep language clear and beginner-friendly

### Maintenance

- Update regularly with new features
- Fix broken links promptly
- Respond to user feedback
- Keep command examples current

---

## Next Steps

✅ Your documentation is now live!

- Share the link with your community
- Add it to your bot's Discord status
- Include it in bot listings (top.gg, etc.)
- Link from your main Herald repository

---

## Need Help?

- [MkDocs Material Documentation](https://squidfunk.github.io/mkdocs-material/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Herald Support Discord](https://discord.gg/9bEZk6ARG9)

---

*Happy documenting! 📚*
