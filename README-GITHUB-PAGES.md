# Świecowe Love - GitHub Pages Deployment Guide

This guide will help you deploy your Świecowe Love website to GitHub Pages.

## File Structure for Deployment

The following files are required for your website to work on GitHub Pages:

```
├── index.html              # Main website file
├── site-data.json          # Site configuration data
├── posts.json              # Blog posts data
├── products.json           # Products data
├── image/                  # Folder with all images
│   ├── Logo.png
│   ├── tlo.png
│   └── ... (all other images)
├── pomoc.html              # Help page
├── polityka-prywatnosci.html  # Privacy policy
├── regulamin.html          # Terms of service
└── zwroty-reklamacje.html  # Returns and complaints
```

## Step-by-Step Deployment Instructions

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in to your account
2. Click the "+" icon in the top right corner and select "New repository"
3. Name your repository (e.g., `swiecowe-love`)
4. Make sure the repository is set to "Public"
5. Do NOT initialize with a README
6. Click "Create repository"

### Step 2: Prepare Your Files

Make sure you have all the required files in a folder on your computer:
- `index.html`
- `site-data.json`
- `posts.json`
- `products.json`
- `image/` folder with all images
- All HTML pages (`pomoc.html`, `polityka-prywatnosci.html`, etc.)

### Step 3: Upload Files to GitHub

#### Option A: Using GitHub Desktop (Recommended for beginners)

1. Download and install [GitHub Desktop](https://desktop.github.com/)
2. Open GitHub Desktop and sign in with your GitHub account
3. Click "Clone a repository from the Internet"
4. Select your repository and clone it to your computer
5. Copy all your website files into the cloned repository folder
6. In GitHub Desktop:
   - You'll see a list of changed files
   - Write a commit message (e.g., "Initial website upload")
   - Click "Commit to main"
   - Click "Push origin" to upload files to GitHub

#### Option B: Using Command Line (For experienced users)

1. Open Terminal/Git Bash
2. Navigate to your website folder:
   ```
   cd path/to/your/website/folder
   ```
3. Initialize git repository:
   ```
   git init
   ```
4. Add all files:
   ```
   git add .
   ```
5. Commit files:
   ```
   git commit -m "Initial website upload"
   ```
6. Add remote origin (replace `username` with your GitHub username):
   ```
   git remote add origin https://github.com/username/repository-name.git
   ```
7. Push to GitHub:
   ```
   git push -u origin main
   ```

#### Option C: Drag and Drop in Browser (Simplest method)

1. Go to your GitHub repository page
2. Click "Add file" → "Upload files"
3. Drag and drop all your website files
4. Write a commit message (e.g., "Initial website upload")
5. Click "Commit changes"

### Step 4: Enable GitHub Pages

1. Go to your repository page on GitHub
2. Click "Settings" tab
3. In the left sidebar, click "Pages"
4. Under "Source", select "Deploy from a branch"
5. Select "main" branch and "/ (root)" folder
6. Click "Save"
7. Wait a few minutes for GitHub to build your site

### Step 5: Access Your Website

1. After GitHub finishes building (you'll see a green checkmark), your website will be available at:
   ```
   https://username.github.io/repository-name/
   ```
   For example: `https://janekowalski.github.io/swiecowe-love/`

2. You can also set up a custom domain if you have one:
   - In the GitHub Pages settings, enter your custom domain
   - Configure DNS settings with your domain provider

## Updating Your Website

To update your website:

1. Make changes to your files locally
2. Commit and push changes to GitHub (using GitHub Desktop, command line, or drag-and-drop)
3. GitHub Pages will automatically rebuild and deploy your site
4. Changes typically appear within 1-2 minutes

## Troubleshooting

### If your website doesn't appear:

1. Check that your main HTML file is named `index.html`
2. Ensure all file paths are correct (case-sensitive on GitHub)
3. Verify that GitHub Pages is enabled in repository settings
4. Check the "Actions" tab for any build errors

### If images aren't loading:

1. Make sure all images are in the `image/` folder
2. Check that image file names match exactly (including capitalization)
3. Verify that image paths in your HTML and JSON files are correct

### If data isn't loading:

1. Ensure `site-data.json`, `posts.json`, and `products.json` are in the root folder
2. Check that JSON files are properly formatted
3. Verify that the website can access these files via fetch requests

## Managing Content

You can manage your website content by editing the JSON files:

- `site-data.json` - Contains site configuration (titles, descriptions, gallery images)
- `posts.json` - Contains blog posts
- `products.json` - Contains product information

After editing these files, upload them to GitHub to update your website.

## Need Help?

If you encounter any issues:
1. Check the browser console for error messages (F12 → Console)
2. Verify all file paths and names
3. Make sure GitHub Pages is properly configured
4. Contact support if problems persist