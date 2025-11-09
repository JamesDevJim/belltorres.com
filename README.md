# Bell-Torres Family Website

A modern, clean personal website for the Bell-Torres family, built with Jekyll and hosted on GitHub Pages.

## 🚀 Quick Start Guide

### Initial Setup (One-Time)

#### 1. Create GitHub Repository
1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon → "New repository"
3. Name it: `belltorres.com` (or `yourusername.github.io`)
4. Set to **Public**
5. Do NOT initialize with README (we're uploading files)
6. Click "Create repository"

#### 2. Upload Website Files
1. Download all files from this project
2. On your new repository page, click "uploading an existing file"
3. Drag and drop ALL files and folders
4. Scroll down, add commit message: "Initial website setup"
5. Click "Commit changes"

#### 3. Enable GitHub Pages
1. In your repository, click **Settings**
2. Scroll to **Pages** in left sidebar
3. Under "Source", select **main** branch
4. Click **Save**
5. Your site will be live at `https://yourusername.github.io` in 1-2 minutes

#### 4. Connect Custom Domain (belltorres.com)
1. Go to your domain registrar (where you bought belltorres.com)
2. Find DNS settings
3. Add these DNS records:
   ```
   Type: A     Name: @    Value: 185.199.108.153
   Type: A     Name: @    Value: 185.199.109.153
   Type: A     Name: @    Value: 185.199.110.153
   Type: A     Name: @    Value: 185.199.111.153
   Type: CNAME Name: www  Value: yourusername.github.io
   ```
4. In GitHub Settings → Pages, enter `belltorres.com` in "Custom domain"
5. Check "Enforce HTTPS" (wait 10 minutes if not available yet)
6. DNS changes take 24-48 hours to fully propagate

---

## 📝 How to Edit Your Website

### Editing Family Information

#### Update Family Bios
**File:** `_data/family.yml`

```yaml
members:
  - name: "James Bell-Torres"
    role: "Sustainability Expert & Engineer"
    bio: "Edit this text to update James's bio..."
    interests:
      - "Coffee Brewing"
      - "Tennis"
```

Just edit the text between the quotes!

#### Update Homepage Welcome Message
**File:** `index.html`

Find this section (around line 10):
```html
<h1>Welcome to Our Family</h1>
<p class="subtitle">Edit this welcoming message here</p>
```

#### Change Colors
**File:** `_config.yml`

```yaml
# Color Palette
primary_color: "#2C5F7C"    # Deep blue
secondary_color: "#F4A261"  # Warm orange
accent_color: "#E76F51"     # Coral red
```

Change the hex color codes to your preference.

---

## 📸 Adding Photos

### Add Photos to Gallery
1. Add your photo files to the `assets/images/gallery/` folder
2. Open `_data/gallery.yml`
3. Add a new entry:

```yaml
- image: "/assets/images/gallery/your-photo.jpg"
  caption: "Description of the photo"
  category: "family"  # Options: family, travel, dax, hobbies
  date: "2025-11-01"
```

### Add Travel Photos
1. Add photos to `assets/images/travel/`
2. Open `_data/travels.yml`
3. Add destination:

```yaml
- location: "Paris, France"
  date: "October 2025"
  image: "/assets/images/travel/paris.jpg"
  description: "Amazing trip to Paris!"
  photos:
    - "/assets/images/travel/paris-1.jpg"
    - "/assets/images/travel/paris-2.jpg"
```

### Replace Homepage Hero Image
1. Add your family photo to `assets/images/`
2. Name it `hero-family.jpg` (or update the filename in `index.html`)

---

## ✍️ Adding Blog Posts

### Create a New Blog Post
1. Go to the `_posts/` folder
2. Create a new file named: `YYYY-MM-DD-title-of-post.md`
   - Example: `2025-11-09-weekend-adventures.md`
3. Copy this template:

```markdown
---
layout: post
title: "Your Post Title"
date: 2025-11-09
author: "James & Namibia"
categories: [family, travel]
image: "/assets/images/blog/your-image.jpg"
---

Write your blog post content here using Markdown.

## You can use headers

- And bullet points
- Like this

![Photo description](/assets/images/blog/photo.jpg)

**Bold text** and *italic text* work too!
```

4. Save the file and commit to GitHub

---

## 🔄 Publishing Changes

### Method 1: GitHub Website (Easiest)
1. Go to your repository on GitHub
2. Navigate to the file you want to edit
3. Click the pencil icon (Edit)
4. Make your changes
5. Scroll down → "Commit changes" → Add description → "Commit changes"
6. Wait 1-2 minutes for the site to rebuild

### Method 2: Upload Files
1. Go to your repository
2. Click "Add file" → "Upload files"
3. Drag your new photos or files
4. Commit changes

### Method 3: Git Command Line (Advanced)
```bash
git clone https://github.com/yourusername/belltorres.com.git
cd belltorres.com
# Make your changes
git add .
git commit -m "Updated family photos"
git push
```

---

## 📁 File Structure

```
belltorres.com/
├── _config.yml           # Main configuration (colors, site name, etc.)
├── _data/
│   ├── family.yml        # Family member information
│   ├── gallery.yml       # Photo gallery data
│   ├── travels.yml       # Travel destinations
│   └── hobbies.yml       # Hobbies information
├── _layouts/
│   ├── default.html      # Main page template
│   ├── post.html         # Blog post template
│   └── page.html         # General page template
├── _posts/               # Blog posts go here (YYYY-MM-DD-title.md)
├── _includes/
│   ├── header.html       # Website header/navigation
│   └── footer.html       # Website footer
├── assets/
│   ├── css/
│   │   └── style.css     # All styling
│   ├── js/
│   │   └── main.js       # Interactive features
│   └── images/           # All photos go here
│       ├── gallery/
│       ├── travel/
│       ├── blog/
│       └── family/
├── pages/
│   ├── about.html        # About Us page
│   ├── travel.html       # Travel page
│   ├── hobbies.html      # Hobbies page
│   ├── gallery.html      # Photo Gallery page
│   └── blog.html         # Blog listing page
├── index.html            # Homepage
└── README.md             # This file!
```

---

## 🎨 Customization Tips

### Change Fonts
Edit `assets/css/style.css`, find the `@import` line at the top:
```css
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&family=Merriweather:wght@300;400&display=swap');
```
Visit [Google Fonts](https://fonts.google.com/) to choose new ones.

### Adjust Spacing/Layout
In `assets/css/style.css`, look for these variables at the top:
```css
:root {
  --spacing-unit: 2rem;
  --max-width: 1200px;
}
```

### Add New Pages
1. Create file in `pages/` folder: `your-page.html`
2. Add this at the top:
```html
---
layout: page
title: Your Page Title
permalink: /your-page/
---
```
3. Add link to navigation in `_includes/header.html`

---

## 🆘 Troubleshooting

### Site Not Updating
- Wait 2-3 minutes after committing changes
- Check GitHub Actions tab for build errors
- Clear your browser cache (Ctrl+Shift+R or Cmd+Shift+R)

### Images Not Showing
- Check file path starts with `/assets/images/`
- Ensure image file is actually uploaded
- Check for typos in filename

### Page Not Found (404)
- Check permalink in page front matter
- Ensure file is in correct location
- Verify navigation link is correct

### Custom Domain Not Working
- Wait 24-48 hours after setting DNS
- Verify DNS records are correct (use [DNS Checker](https://dnschecker.org/))
- Ensure HTTPS is enabled in GitHub Pages settings

---

## 📱 Mobile Optimization

The site is fully responsive! It automatically adapts to:
- Desktop (1200px+)
- Tablet (768px - 1199px)
- Mobile (320px - 767px)

Test on your phone after publishing changes.

---

## 💡 Content Ideas

### Blog Post Ideas
- Monthly family updates
- Travel stories and tips
- DIY projects and home improvements
- Recipes and cooking adventures
- Dax's adventures
- Pregnancy journey and baby updates
- Coffee brewing experiments
- Tennis tournament experiences

### Photo Gallery Categories
- Family portraits
- Travel adventures
- Dax being adorable
- Home and DIY projects
- Food and coffee
- Nature and outdoors
- Special occasions

---

## 🔗 Useful Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Help](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)
- [Google Fonts](https://fonts.google.com/)
- [Unsplash](https://unsplash.com/) - Free stock photos for placeholders
- [Coolors](https://coolors.co/) - Color palette generator

---

## ✅ Maintenance Checklist

### Monthly
- [ ] Update blog with family news
- [ ] Add new photos to gallery
- [ ] Check all links still work
- [ ] Review and update "About Us" if needed

### As Needed
- [ ] Add travel stories after trips
- [ ] Update baby section when baby arrives
- [ ] Add new hobby projects
- [ ] Respond to any contact form submissions (if added)

---

## 📞 Need Help?

If you get stuck:
1. Check the Troubleshooting section above
2. Search GitHub's documentation
3. Ask ChatGPT or Claude for specific help
4. Check Jekyll documentation for advanced features

---

**Built with ❤️ for the Bell-Torres Family**
