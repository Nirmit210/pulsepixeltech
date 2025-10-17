# GitHub Setup Commands

After creating your GitHub repository, run these commands:

```bash
# Add your GitHub repository as remote (replace with your actual repository URL)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Example (replace with your actual details):
```bash
git remote add origin https://github.com/yourusername/pulsepixeltech-ecommerce.git
git branch -M main
git push -u origin main
```

## If you get authentication errors:
1. Use GitHub CLI: `gh auth login`
2. Or use Personal Access Token instead of password
3. Or use SSH key authentication

## After successful push:
Your repository will be available at:
https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME

Then you can proceed with Vercel deployment using the GitHub repository!