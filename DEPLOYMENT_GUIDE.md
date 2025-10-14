# 🚀 GitHub Pages Deployment Guide

Follow these steps to publish your Hugo website to GitHub Pages:

## Step 1: Create GitHub Repository

1. **Go to [GitHub.com](https://github.com)** and sign in
2. **Click the "+" icon** in the top right corner
3. **Select "New repository"**
4. **Repository name**: `mohtasimhafiz.github.io` (exactly this name!)
5. **Make it Public** (required for free GitHub Pages)
6. **Don't initialize** with README, .gitignore, or license
7. **Click "Create repository"**

## Step 2: Push Your Code

After creating the repository, run these commands in your terminal:

```bash
# Navigate to your website directory
cd /Users/mohtasimhafiz/my-website

# Add the GitHub remote (replace with your actual GitHub username)
git remote add origin https://github.com/mohtasimhafiz/mohtasimhafiz.github.io.git

# Push your code to GitHub
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. **Go to your repository** on GitHub
2. **Click "Settings"** tab
3. **Scroll down to "Pages"** in the left sidebar
4. **Under "Source"**, select **"GitHub Actions"**
5. **Save the settings**

## Step 4: Automatic Deployment

Once you push your code, GitHub Actions will automatically:

1. **Build your Hugo site**
2. **Deploy it to GitHub Pages**
3. **Make it available at**: `https://mohtasimhafiz.github.io`

## Step 5: Monitor Deployment

1. **Go to the "Actions" tab** in your repository
2. **Watch the deployment progress**
3. **Wait for the green checkmark** (usually takes 2-5 minutes)

## Step 6: Access Your Live Website

Your website will be available at:
**https://mohtasimhafiz.github.io**

## 🔄 Future Updates

To update your website:

1. **Make changes** to your content
2. **Commit and push**:
   ```bash
   git add .
   git commit -m "Update website content"
   git push
   ```
3. **GitHub Actions will automatically rebuild and deploy**

## 📁 Repository Structure

Your repository should contain:
- ✅ `.github/workflows/hugo.yml` (GitHub Actions workflow)
- ✅ `config.toml` (with correct baseURL)
- ✅ `content/` (your website content)
- ✅ `themes/blowfish/` (Hugo theme)
- ✅ All other Hugo files

## 🛠️ Troubleshooting

### If deployment fails:
1. **Check the Actions tab** for error messages
2. **Verify your repository name** is exactly `mohtasimhafiz.github.io`
3. **Ensure the repository is public**
4. **Check that GitHub Pages is enabled** in Settings

### If the site doesn't load:
1. **Wait 5-10 minutes** after deployment
2. **Check the Actions tab** for successful deployment
3. **Verify the baseURL** in `config.toml` matches your GitHub Pages URL

## 🎉 Success!

Once deployed, your website will be live at:
**https://mohtasimhafiz.github.io**

You can share this URL with anyone, and it will work worldwide!

## 📝 Custom Domain (Optional)

If you want to use a custom domain later:
1. **Add a CNAME file** to your repository
2. **Configure DNS** with your domain provider
3. **Update baseURL** in `config.toml`

---

**Need help?** Check the GitHub Actions logs in the "Actions" tab of your repository.
