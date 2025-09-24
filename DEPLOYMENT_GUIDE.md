# GitHub Pages Deployment Guide

This guide will walk you through deploying your VC Partners website to GitHub Pages for free hosting.

## Prerequisites

- A GitHub account (free)
- Git installed on your computer
- The website files ready in your local directory

## Step-by-Step Deployment

### Step 1: Create GitHub Repository

1. **Go to GitHub.com** and sign in to your account
2. **Click the "+" icon** in the top-right corner
3. **Select "New repository"**
4. **Repository settings:**
   - Repository name: `vcpartners-website` (or your preferred name)
   - Description: "VC Partners - Vietnam's Leading Venture Capital Firm"
   - Visibility: **Public** (required for free GitHub Pages)
   - **DO NOT** check "Add a README file"
   - **DO NOT** check "Add .gitignore"
   - **DO NOT** check "Choose a license"
5. **Click "Create repository"**

### Step 2: Connect Local Repository to GitHub

Run these commands in your terminal (make sure you're in the `/Users/raymond/Projects/vcp_website` directory):

```bash
# Add the GitHub repository as remote origin
git remote add origin https://github.com/YOUR_USERNAME/vcpartners-website.git

# Rename the default branch to 'main' (if needed)
git branch -M main

# Push your code to GitHub
git push -u origin main
```

**Replace `YOUR_USERNAME` with your actual GitHub username.**

### Step 3: Enable GitHub Pages

1. **Go to your repository on GitHub**
2. **Click the "Settings" tab** (at the top of the repository page)
3. **Scroll down to "Pages"** in the left sidebar
4. **Under "Source":**
   - Select "Deploy from a branch"
   - Branch: "main"
   - Folder: "/ (root)"
5. **Click "Save"**
6. **Wait 5-10 minutes** for GitHub to build and deploy your site

### Step 4: Access Your Live Website

Your website will be available at:
```
https://YOUR_USERNAME.github.io/vcpartners-website/
```

**Replace `YOUR_USERNAME` with your actual GitHub username.**

## Alternative Method: Upload via GitHub Web Interface

If you prefer not to use Git commands:

### Step 1: Create Repository (same as above)

### Step 2: Upload Files via Web Interface

1. **In your new repository, click "Add file"**
2. **Select "Upload files"**
3. **Drag and drop these files:**
   - `index.html`
   - `styles.css`
   - `script.js`
   - `README.md`
4. **Add commit message:** "Initial commit - VC Partners website"
5. **Click "Commit changes"**

### Step 3: Enable GitHub Pages (same as above)

## Updating Your Website

### Method 1: Using Git Commands

```bash
# Make your changes to the files
# Then commit and push:

git add .
git commit -m "Update website content"
git push origin main
```

### Method 2: Using GitHub Web Interface

1. **Go to your repository on GitHub**
2. **Click on the file you want to edit**
3. **Click the pencil icon** to edit
4. **Make your changes**
5. **Scroll down and click "Commit changes"**

## Custom Domain (Optional)

To use a custom domain like `vcpartners.vn`:

1. **Add a file named `CNAME`** to your repository root with your domain:
   ```
   vcpartners.vn
   ```

2. **Configure DNS settings** with your domain provider:
   - Add a CNAME record pointing to `YOUR_USERNAME.github.io`

3. **In GitHub Pages settings:**
   - Enter your custom domain in the "Custom domain" field
   - Check "Enforce HTTPS"

## Troubleshooting

### Common Issues and Solutions

#### 1. "404 - Page not found"
- **Cause:** GitHub Pages hasn't finished building yet
- **Solution:** Wait 10-15 minutes and try again

#### 2. "Repository not found"
- **Cause:** Repository is private
- **Solution:** Make sure your repository is set to "Public"

#### 3. "Styles not loading"
- **Cause:** Incorrect file paths
- **Solution:** Check that all files are in the root directory

#### 4. "Changes not showing"
- **Cause:** Browser cache or GitHub Pages cache
- **Solution:** 
  - Clear your browser cache
  - Wait 10-15 minutes for GitHub Pages to update
  - Try accessing the site in an incognito/private window

### Checking Deployment Status

1. **Go to your repository on GitHub**
2. **Click the "Actions" tab**
3. **Look for "pages build and deployment"** workflow
4. **Green checkmark** = successful deployment
5. **Red X** = deployment failed (check the logs)

## Performance Optimization

### Before Deployment

1. **Test locally:**
   ```bash
   # Open index.html in your browser
   # Or use a local server:
   python -m http.server 8000
   # Then visit http://localhost:8000
   ```

2. **Check file sizes:**
   - Keep total size under 100MB for GitHub Pages
   - Optimize images if you add any

3. **Validate HTML:**
   - Use [W3C Markup Validator](https://validator.w3.org/)
   - Fix any errors before deploying

## Security Considerations

- **No sensitive data:** Don't put API keys or passwords in your code
- **HTTPS enabled:** GitHub Pages automatically provides HTTPS
- **Public repository:** Remember that your code will be visible to everyone

## Monitoring Your Website

### GitHub Pages Analytics

1. **Go to repository Settings**
2. **Scroll to "Pages" section**
3. **Enable "GitHub Pages insights"** to see visitor statistics

### Custom Analytics

Add Google Analytics or other tracking services by editing the `<head>` section in `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## Support

If you encounter issues:

1. **Check GitHub Pages documentation:** https://docs.github.com/en/pages
2. **GitHub Community Forum:** https://github.community/
3. **GitHub Support:** https://support.github.com/

---

**Your website is now live and ready to showcase VC Partners to the world! 🚀**
