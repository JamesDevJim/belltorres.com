# Complete Deployment Guide for Bell-Torres Family Website

This guide will walk you through deploying your website to GitHub Pages and connecting your custom domain (belltorres.com).

## Prerequisites

- GitHub account
- Domain name (belltorres.com) purchased from a domain registrar
- All website files downloaded to your computer

---

## Part 1: GitHub Repository Setup

### Step 1: Create a New Repository

1. Log in to [GitHub](https://github.com)
2. Click the **"+"** icon in the top right corner
3. Select **"New repository"**
4. Configure your repository:
   - **Repository name:** `belltorres.com` (or `yourusername.github.io`)
   - **Description:** "Bell-Torres Family Website"
   - **Visibility:** Public (required for free GitHub Pages)
   - **Do NOT** check "Initialize this repository with a README"
5. Click **"Create repository"**

### Step 2: Upload Your Files

#### Option A: Using GitHub Web Interface (Easiest)

1. On your new repository page, click **"uploading an existing file"** link
2. Drag and drop ALL files and folders from the `belltorres-website` directory
3. Make sure to include:
   - All folders (`_data`, `_layouts`, `_includes`, `_posts`, `assets`, `pages`)
   - All files (`index.html`, `_config.yml`, `README.md`, `CNAME`, etc.)
4. Add commit message: "Initial website setup"
5. Click **"Commit changes"**

⏱️ **Wait 5-10 minutes** for files to upload if you have many images.

#### Option B: Using Git Command Line (Advanced)

```bash
# Open Terminal (Mac/Linux) or Git Bash (Windows)

# Navigate to where you downloaded the website files
cd path/to/belltorres-website

# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial website setup"

# Add your GitHub repository as remote (replace with your actual repo URL)
git remote add origin https://github.com/yourusername/belltorres.com.git

# Push to GitHub
git branch -M main
git push -u origin main
```

---

## Part 2: Enable GitHub Pages

### Step 1: Configure GitHub Pages

1. In your repository, click **"Settings"** (top navigation)
2. Scroll down and click **"Pages"** in the left sidebar
3. Under **"Source"**:
   - Select **"Deploy from a branch"**
   - Branch: **"main"**
   - Folder: **"/ (root)"**
4. Click **"Save"**

### Step 2: Wait for Deployment

1. GitHub will display a message: "Your site is ready to be published at https://yourusername.github.io"
2. Wait **1-2 minutes** for the initial build
3. Refresh the Settings → Pages screen
4. When you see "Your site is live at...", click the URL to test your site

🎉 **Your website is now live** at `https://yourusername.github.io`!

---

## Part 3: Connect Custom Domain (belltorres.com)

### Step 1: Configure DNS Records at Your Domain Registrar

You need to add DNS records at wherever you purchased belltorres.com (e.g., GoDaddy, Namecheap, Google Domains, Cloudflare, etc.).

#### Find Your DNS Settings

Each registrar is different, but look for:
- "DNS Management"
- "DNS Settings"
- "Nameservers and DNS"
- "Advanced DNS"
- "Domain Settings"

#### Add These DNS Records

**For Root Domain (belltorres.com):**

Add **FOUR A records** pointing to GitHub's IP addresses:

| Type | Name/Host | Value/Points To      | TTL   |
|------|-----------|----------------------|-------|
| A    | @         | 185.199.108.153      | 3600  |
| A    | @         | 185.199.109.153      | 3600  |
| A    | @         | 185.199.110.153      | 3600  |
| A    | @         | 185.199.111.153      | 3600  |

**For WWW Subdomain (www.belltorres.com):**

Add **ONE CNAME record**:

| Type  | Name/Host | Value/Points To              | TTL   |
|-------|-----------|------------------------------|-------|
| CNAME | www       | yourusername.github.io       | 3600  |

**Replace `yourusername` with your actual GitHub username!**

#### Common Registrar-Specific Instructions

<details>
<summary><b>GoDaddy</b></summary>

1. Log in to GoDaddy
2. Go to "My Products" → "Domains"
3. Click the three dots next to your domain → "Manage DNS"
4. Scroll to "Records" section
5. Click "Add" for each record
6. Fill in Type, Name, Value, TTL
7. Click "Save"
</details>

<details>
<summary><b>Namecheap</b></summary>

1. Log in to Namecheap
2. Go to "Domain List" → Click "Manage" next to your domain
3. Click "Advanced DNS" tab
4. Click "Add New Record"
5. Add each DNS record
6. Click the green checkmark to save
</details>

<details>
<summary><b>Google Domains</b></summary>

1. Log in to Google Domains
2. Click your domain
3. Click "DNS" in left menu
4. Scroll to "Custom records"
5. Click "Manage custom records"
6. Add each record
7. Click "Save"
</details>

<details>
<summary><b>Cloudflare</b></summary>

1. Log in to Cloudflare
2. Select your domain
3. Go to "DNS" section
4. Click "Add record"
5. Add each record
6. Make sure the proxy status (cloud icon) is orange (proxied) or gray (DNS only)—both work
7. Click "Save"
</details>

### Step 2: Configure Custom Domain in GitHub

1. Go back to your repository **Settings → Pages**
2. Under **"Custom domain"**, enter: `belltorres.com`
3. Click **"Save"**
4. Wait for DNS check (may show "DNS check unsuccessful" initially—this is normal)
5. After 24-48 hours, check the box **"Enforce HTTPS"** (you might need to wait for this option to become available)

### Step 3: Wait for DNS Propagation

⏱️ **DNS changes take time to propagate:**
- Minimum: 15 minutes to 1 hour
- Typical: 4-8 hours
- Maximum: 24-48 hours

**Check DNS propagation status:**
- Visit [DNS Checker](https://dnschecker.org/)
- Enter `belltorres.com`
- Select "A" record type
- You should see the four GitHub IP addresses

### Step 4: Verify Your Domain Works

After DNS propagates, test these URLs:
- ✅ `http://belltorres.com`
- ✅ `https://belltorres.com`
- ✅ `http://www.belltorres.com`
- ✅ `https://www.belltorres.com`

All should redirect to the secure HTTPS version of your site.

---

## Part 4: Troubleshooting

### Site Not Loading

**Check:**
1. Are your files uploaded to GitHub? Check the repository file list.
2. Is GitHub Pages enabled? Check Settings → Pages.
3. Is the site built successfully? Check Actions tab for any errors.
4. Wait 5 minutes and refresh—sometimes takes time.

### Custom Domain Not Working

**Check:**
1. Are DNS records correct? Double-check all IP addresses.
2. Did you enter the domain correctly in GitHub (no `https://` or trailing slash)?
3. Has enough time passed for DNS propagation? Wait 24-48 hours.
4. Use [DNS Checker](https://dnschecker.org/) to verify DNS records are live globally.
5. Try clearing your browser cache or using incognito mode.

### Images Not Showing

**Check:**
1. Are images uploaded to the correct folder? (`assets/images/`)
2. Are the file paths in YAML files correct?
3. Are filenames exact matches? (Case-sensitive!)
4. Check browser console (F12) for 404 errors.

### Site Looks Broken

**Check:**
1. Did you upload ALL files and folders?
2. Is the `_config.yml` file present?
3. Check the Actions tab for build errors.
4. Look at browser console (F12) for CSS or JavaScript errors.

### "HTTPS Not Available" or SSL Errors

**Fix:**
1. Make sure DNS is fully propagated (wait 24-48 hours)
2. In Settings → Pages, uncheck then recheck "Enforce HTTPS"
3. Wait 10 minutes and try again
4. Clear browser cache

### GitHub Pages Not Building

**Check:**
1. Go to repository → Actions tab
2. Look for failed builds (red X)
3. Click on the failed build for error details
4. Common issues:
   - Syntax error in `_config.yml`
   - Missing dependencies in `Gemfile`
   - Liquid syntax errors in HTML files

---

## Part 5: Maintenance and Updates

### How to Update Content

#### Method 1: Edit on GitHub (Easiest)

1. Go to your repository on GitHub
2. Navigate to the file you want to edit
3. Click the pencil icon (Edit)
4. Make your changes
5. Scroll down → Add commit message
6. Click "Commit changes"
7. Wait 1-2 minutes for site to rebuild

#### Method 2: Upload New Files

1. Go to the appropriate folder in your repository
2. Click "Add file" → "Upload files"
3. Drag and drop your files
4. Click "Commit changes"

#### Method 3: Git Command Line

```bash
# Pull latest changes
git pull origin main

# Make your changes to files

# Stage changes
git add .

# Commit with a message
git commit -m "Updated blog post"

# Push to GitHub
git push origin main
```

### Common Updates

**Add a Blog Post:**
1. Create new file in `_posts/` folder
2. Name it: `YYYY-MM-DD-title-of-post.md`
3. Use the blog post template from README

**Add Photos:**
1. Upload to `assets/images/gallery/`
2. Update `_data/gallery.yml` with new photo info

**Update Family Info:**
1. Edit `_data/family.yml`

**Change Colors:**
1. Edit `_config.yml` (color variables at top)

---

## Part 6: Advanced Features (Optional)

### Enable Google Analytics

1. Create Google Analytics account
2. Get your tracking ID (format: UA-XXXXXXXXX-X or G-XXXXXXXXXX)
3. Edit `_config.yml`:
   ```yaml
   google_analytics: "YOUR-TRACKING-ID"
   ```

### Add Social Media Links

1. Edit `_config.yml` under `social:` section
2. Add your handles/URLs
3. Links will automatically appear in footer

### Install Locally for Testing (Advanced)

```bash
# Install Ruby and Jekyll (see jekyllrb.com/docs/installation/)

# In your website directory:
bundle install

# Run local server:
bundle exec jekyll serve

# View at: http://localhost:4000
```

---

## Need Help?

### Resources
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [DNS Checker Tool](https://dnschecker.org/)
- [Website README](README.md) - Full editing guide

### Common Issues & Solutions

Issue found? Check the main README.md file's Troubleshooting section.

---

## Checklist: Complete Setup

- [ ] GitHub repository created
- [ ] All files uploaded to GitHub
- [ ] GitHub Pages enabled
- [ ] Site accessible at yourusername.github.io
- [ ] DNS records added at domain registrar
- [ ] Custom domain configured in GitHub
- [ ] DNS propagated (checked with DNS Checker)
- [ ] Site accessible at belltorres.com
- [ ] HTTPS enforced
- [ ] All pages loading correctly
- [ ] Images displaying
- [ ] Navigation working
- [ ] Mobile responsive
- [ ] Social links added (optional)
- [ ] Google Analytics added (optional)

🎉 **Congratulations! Your website is live!**

---

**Last Updated:** November 2025
