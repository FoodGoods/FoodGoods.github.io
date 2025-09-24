# Base.is-a.dev Setup Instructions

## Prerequisites
✅ Docusaurus site created
✅ Git repository initialized
✅ Basic configuration completed

## Next Steps

### 1. GitHub Repository Setup

You need to create a GitHub repository for your site. The repository name should ideally be:
- `yourusername.github.io` (for user pages)
- OR `base-docs` (for project pages)

**Create the repository on GitHub first, then run:**

```bash
# Replace 'yourusername' with your actual GitHub username
git remote add origin https://github.com/yourusername/yourusername.github.io.git

# Or if using project pages:
# git remote add origin https://github.com/yourusername/base-docs.git

git add .
git commit -m "Initial commit: Docusaurus site for base.is-a.dev"
git branch -M main
git push -u origin main
```

### 2. Update Docusaurus Config

Update `docusaurus.config.ts` with your GitHub info:

```typescript
// Replace these values:
organizationName: 'yourusername', // Your GitHub username
projectName: 'yourusername.github.io', // Your repo name (or base-docs)

// Update the GitHub link in navbar:
{
  href: 'https://github.com/yourusername/yourusername.github.io',
  label: 'GitHub',
  position: 'right',
}

// Update edit URLs:
editUrl: 'https://github.com/yourusername/yourusername.github.io/tree/main/',
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Go to Settings → Pages
3. Source: Deploy from a branch
4. Branch: `gh-pages` (will be created automatically)
5. Folder: `/ (root)`

### 4. Deploy Your Site

```bash
npm run build
npm run deploy
```

This creates a `gh-pages` branch and deploys your site.

### 5. Register Domain

Create a file named `base.json` with this content:

```json
{
  "description": "Base documentation website",
  "repo": "https://github.com/yourusername/yourusername.github.io",
  "owner": {
    "username": "yourusername",
    "email": "your-email@example.com"
  },
  "record": {
    "CNAME": "yourusername.github.io"
  }
}
```

### 6. Submit Domain Registration

1. Fork: https://github.com/is-a-dev/register
2. Add your `base.json` file to the `domains/` folder
3. Create a pull request

### 7. Configure Custom Domain (After PR Approval)

1. Wait for PR approval (usually 1-24 hours)
2. Go to your GitHub repo Settings → Pages
3. Custom domain: `base.is-a.dev`
4. Check "Enforce HTTPS"
5. Update `docusaurus.config.ts` if needed
6. Redeploy: `npm run deploy`

## Testing Locally

```bash
npm start
```

Visit http://localhost:3000 to see your site.

## Important Notes

- Use GitHub Pages hosting (required for is-a.dev)
- Don't use Vercel or Netlify (SSL certificate issues)
- Wait up to 24 hours for DNS propagation
- Keep your repository public for GitHub Pages

## Support

- is-a.dev Discord: https://discord.gg/is-a-dev
- GitHub Issues: https://github.com/is-a-dev/register/issues