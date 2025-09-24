# 🚀 Deploy base.is-a.dev Now!

## Step 1: Create GitHub Repository
1. Go to [GitHub](https://github.com/new)
2. Create repository named: `FoodGoods.github.io`
3. Make it **public**
4. Don't initialize with README (we already have files)

## Step 2: Push Your Code
```bash
git add .
git commit -m "Initial commit: Base documentation site"
git branch -M main
git remote add origin https://github.com/FoodGoods/FoodGoods.github.io.git
git push -u origin main
```

## Step 3: Deploy to GitHub Pages
```bash
npm run build
npm run deploy
```

## Step 4: Enable GitHub Pages
1. Go to your repository: https://github.com/FoodGoods/FoodGoods.github.io
2. Settings → Pages
3. Source: **Deploy from a branch**
4. Branch: **gh-pages**
5. Folder: **/ (root)**
6. Save

## Step 5: Register Domain
1. **Update email** in `domain-registration/base.json` (replace `YOUR-EMAIL@example.com`)
2. Fork: https://github.com/is-a-dev/register
3. Copy `base.json` to the `domains/` folder in your fork
4. Create Pull Request with title: "Add base.is-a.dev"

## Step 6: Configure Custom Domain (After PR Approval)
1. Wait for PR approval (1-24 hours)
2. Go to repository Settings → Pages
3. Custom domain: `base.is-a.dev`
4. Check **Enforce HTTPS**
5. Save

## 🎉 Done!
Your site will be live at: **https://base.is-a.dev**

## Test Locally First
```bash
npm start
```
Visit: http://localhost:3000

## Need Help?
- Check `SETUP_INSTRUCTIONS.md` for detailed guide
- is-a.dev Discord: https://discord.gg/is-a-dev

---
**⚡ Quick Status Check:**
- [ ] GitHub repo created
- [ ] Code pushed
- [ ] Site deployed
- [ ] Pages enabled
- [ ] Domain registered
- [ ] Custom domain configured