# Deployment Guide for GitHub Pages

This guide will help you publish your DP-700 Study Guide to GitHub Pages.

## Prerequisites

- Git installed on your computer
- A GitHub account
- All study guide files in your local directory

## Step-by-Step Deployment

### 1. Create a New Repository on GitHub

1. Go to [GitHub](https://github.com)
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository (e.g., `dp700-study-guide`)
5. Choose "Public" visibility
6. **Do NOT** initialize with README, .gitignore, or license (we already have these)
7. Click "Create repository"

### 2. Initialize Git and Push Your Files

Open a terminal/command prompt in your project directory and run:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit the files
git commit -m "Initial commit - DP-700 Study Guide"

# Rename branch to main
git branch -M main

# Add your GitHub repository as remote (replace with your actual URL)
git remote add origin https://github.com/YOUR_USERNAME/dp700-study-guide.git

# Push to GitHub
git push -u origin main
```

**Note:** Replace `YOUR_USERNAME` and `dp700-study-guide` with your actual GitHub username and repository name.

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings" tab
3. Scroll down to "Pages" in the left sidebar
4. Under "Source":
   - Select "Deploy from a branch"
   - Choose "main" branch
   - Select "/ (root)" folder
   - Click "Save"

### 4. Access Your Published Site

After a few minutes, your site will be available at:

```
https://YOUR_USERNAME.github.io/dp700-study-guide/
```

You can find the exact URL in the GitHub Pages section of your repository settings.

## Updating Your Site

Whenever you make changes to your study guide:

```bash
# Add changed files
git add .

# Commit changes
git commit -m "Update study guide content"

# Push to GitHub
git push
```

GitHub Pages will automatically rebuild and deploy your site within a few minutes.

## Custom Domain (Optional)

If you want to use a custom domain:

1. Purchase a domain from a domain registrar
2. In your repository settings, under GitHub Pages, add your custom domain
3. Configure DNS settings with your domain registrar:
   - Add a CNAME record pointing to `YOUR_USERNAME.github.io`
   - Or add A records pointing to GitHub's IP addresses

## Troubleshooting

### Site Not Loading

- Wait 5-10 minutes after enabling GitHub Pages
- Check that your repository is public
- Verify that `index.html` is in the root directory
- Check the Actions tab for any build errors

### Changes Not Appearing

- Clear your browser cache
- Wait a few minutes for GitHub to rebuild
- Check that you pushed your changes to the main branch

### 404 Error

- Ensure `index.html` exists in the root directory
- Check that the file names match exactly (case-sensitive)
- Verify the branch and folder settings in GitHub Pages

## Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)

## Support

If you encounter issues:
1. Check the [GitHub Pages documentation](https://docs.github.com/en/pages)
2. Visit [GitHub Community](https://github.community/)
3. Review your repository's Actions tab for build logs

---

Good luck with your deployment and your DP-700 exam preparation!

