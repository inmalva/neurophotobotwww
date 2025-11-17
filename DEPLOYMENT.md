# GitHub Pages Deployment Guide

This guide will help you deploy your NeuroPhotoBot static website to GitHub Pages.

## Prerequisites

1. A GitHub account
2. Git installed on your computer
3. The static website files (located in `/static-website/` directory)

## Option 1: Deploy from this Repository (Subfolder)

If you want to host the website from a subfolder of your current repository:

1. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Click on "Settings" tab
   - Scroll down to "Pages" section
   - Under "Source", select "Deploy from a branch"
   - Choose "main" branch and "/static-website" folder
   - Click "Save"

2. **Access your site**:
   - Your site will be available at: `https://ironpercival.github.io/neurofoto/`
   - It may take a few minutes to become live

## Option 2: Deploy to a Dedicated Repository (Recommended)

For a cleaner URL and better organization:

1. **Create a new repository**:
   ```bash
   # Create a new repository on GitHub (e.g., "neurofoto-website")
   ```

2. **Copy files and deploy**:
   ```bash
   # Navigate to your static website directory
   cd /home/anton/repo/neurofoto/static-website
   
   # Initialize git repository
   git init
   
   # Add all files
   git add .
   
   # Commit files
   git commit -m "Initial commit: NeuroPhotoBot static website"
   
   # Add your new repository as remote
   git remote add origin https://github.com/ironpercival/neurofoto-website.git
   
   # Push to GitHub
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to your new repository settings
   - Enable GitHub Pages from "main" branch and "/" folder
   - Your site will be available at: `https://ironpercival.github.io/neurofoto-website/`

## Option 3: Custom Domain (Optional)

If you want to use a custom domain:

1. **Purchase a domain** (e.g., `neurophotobot.com`)

2. **Configure DNS**:
   - Add CNAME record pointing to `ironpercival.github.io`
   - Or add A records pointing to GitHub's IP addresses

3. **Set up custom domain in GitHub**:
   - In repository settings → Pages
   - Add your custom domain
   - Enable "Enforce HTTPS"

## Files Created

Your static website includes:

- **Core Pages**:
  - `index.html` - Landing page with service overview
  - `about.html` - Detailed company and service information
  - `privacy.html` - Privacy Policy (GDPR compliant)
  - `terms.html` - Terms of Service
  - `refund.html` - Refund & Cancellation Policy

- **Styling**:
  - `css/styles.css` - Combined responsive CSS

- **Configuration**:
  - `.nojekyll` - Prevents Jekyll processing
  - `404.html` - Custom 404 error page
  - `robots.txt` - Search engine instructions
  - `sitemap.xml` - Site structure for SEO
  - `README.md` - Documentation

## Features

✅ **Fully Responsive**: Works on mobile, tablet, and desktop  
✅ **SEO Optimized**: Meta tags, sitemap, robots.txt  
✅ **Fast Loading**: Optimized CSS, web fonts  
✅ **Accessibility**: Proper semantic HTML  
✅ **Legal Compliance**: GDPR-compliant privacy policy  
✅ **Professional Design**: Matches your app's design system  

## Customization

To customize the website:

1. **Update URLs**: Replace placeholder URLs in `sitemap.xml` and `robots.txt`
2. **Modify Content**: Edit HTML files directly
3. **Styling**: Update `css/styles.css`
4. **Colors**: Modify CSS variables in `:root` section

## Maintenance

- Update the "Last updated" dates when you modify legal documents
- Keep contact information current
- Monitor for broken links
- Update sitemap when adding new pages

Your website is now ready for deployment to GitHub Pages!