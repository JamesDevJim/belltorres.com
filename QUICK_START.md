# 🚀 QUICK START GUIDE - Bell-Torres Family Website

**Your complete personal website is ready to deploy!**

This guide will get you from zero to a live website in under 30 minutes.

---

## ⚡ 5-Minute Setup (Minimal)

### Step 1: Upload to GitHub (5 minutes)
1. Create account at [GitHub.com](https://github.com) (if needed)
2. Create new repository named `belltorres.com`
3. Upload all website files (drag and drop)
4. Go to Settings → Pages
5. Enable Pages: Source = "main" branch
6. ✅ Your site is live at `https://yourusername.github.io`

### Step 2: Add Your Photos (Later)
- Upload photos to `assets/images/` folders
- Update `_data/` YAML files with your info
- Site updates automatically in 1-2 minutes

---

## 📋 What You Have

### Complete Website Includes:
- ✅ **Homepage** with hero section and family intro
- ✅ **About Us** page with family bios and stats
- ✅ **Travel** page with destination showcases
- ✅ **Hobbies** page highlighting your interests
- ✅ **Photo Gallery** with category filtering
- ✅ **Blog** with 3 example posts
- ✅ Modern, mobile-responsive design
- ✅ Clean, maintainable code
- ✅ Easy-to-edit data files

### Documentation:
- 📖 **README.md** - Complete editing guide
- 📖 **DEPLOYMENT.md** - Step-by-step deployment
- 📖 **This file** - Quick start summary

---

## 🎯 Your Next Steps

### Immediate (Do First):
1. **Deploy to GitHub** (see DEPLOYMENT.md)
2. **Test the site** at your GitHub Pages URL
3. **Replace placeholder photos** with your actual images

### Soon (First Week):
1. **Update family information** in `_data/family.yml`
2. **Add your travel photos** and update `_data/travels.yml`
3. **Customize colors** in `_config.yml` (if desired)
4. **Connect custom domain** belltorres.com (see DEPLOYMENT.md Part 3)

### Ongoing (Monthly):
1. **Add blog posts** about your adventures
2. **Upload new photos** to gallery
3. **Update family milestones** (baby arrival!)
4. **Share with friends and family**

---

## 📂 File Structure Overview

```
belltorres-website/
├── README.md              ← 📖 Main editing guide - READ THIS FIRST
├── DEPLOYMENT.md          ← 📖 Deployment instructions
├── _config.yml            ← ⚙️ Site settings, colors, navigation
├── _data/                 ← 📝 Your content (easy to edit!)
│   ├── family.yml         ← Family member info
│   ├── gallery.yml        ← Photo gallery data
│   ├── travels.yml        ← Travel destinations
│   └── hobbies.yml        ← Your hobbies
├── _posts/                ← ✍️ Blog posts go here
├── assets/
│   ├── css/style.css      ← 🎨 All styling
│   ├── js/main.js         ← ⚡ Interactive features
│   └── images/            ← 📸 ALL PHOTOS GO HERE
├── pages/                 ← 📄 About, Travel, Hobbies, Gallery, Blog
├── index.html             ← 🏠 Homepage
└── ... (other files)
```

---

## 🎨 Customization Quick Reference

### Change Colors
Edit `_config.yml`:
```yaml
primary_color: "#2C5F7C"    # Deep blue
secondary_color: "#F4A261"  # Orange
accent_color: "#E76F51"     # Coral
```

### Update Family Info
Edit `_data/family.yml`:
```yaml
members:
  - name: "James Bell-Torres"
    bio: "Your bio here..."
```

### Add Blog Post
1. Create file: `_posts/2025-11-09-my-post.md`
2. Add frontmatter (see examples)
3. Write in Markdown
4. Commit to GitHub

### Add Photos
1. Upload to `assets/images/gallery/`
2. Add entry to `_data/gallery.yml`
3. Commit to GitHub

---

## 🔧 Essential Files to Edit

### Must Edit Soon:
- `_config.yml` - Site title, description, social links
- `_data/family.yml` - All family information
- `_data/gallery.yml` - Photo gallery entries
- Replace photos in `assets/images/`

### Can Edit Later:
- `_data/travels.yml` - Travel destination details
- `_data/hobbies.yml` - Hobby information
- Blog posts in `_posts/`
- Page content in `pages/`

### Usually Don't Need to Edit:
- `_layouts/` - HTML templates
- `_includes/` - Header/footer
- `assets/css/style.css` - Styling (unless you know CSS)
- `assets/js/main.js` - JavaScript

---

## 📸 Photo Requirements

### Recommended Sizes:
- **Hero Image**: 1920x1080px (landscape)
- **Family Photos**: 500x500px (square)
- **Gallery Photos**: 1200x800px
- **Blog Images**: 1200x630px (landscape)

### Where to Add:
```
assets/images/
├── hero-family.jpg        ← Main homepage photo
├── family/                ← Individual portraits
├── gallery/               ← Photo gallery
├── travel/                ← Travel destination photos
├── hobbies/               ← Hobby photos
└── blog/                  ← Blog post images
```

### Quick Tips:
- ✅ Use descriptive filenames: `james-tennis-2025.jpg`
- ✅ Compress images: Use [TinyPNG.com](https://tinypng.com)
- ✅ Keep under 500KB per image
- ✅ Use JPG for photos, PNG for graphics

---

## 🆘 Common Issues

### Site Not Loading?
- Wait 2-3 minutes after uploading
- Check GitHub → Actions tab for errors
- Clear browser cache (Ctrl+Shift+R)

### Images Not Showing?
- Verify file path: `/assets/images/gallery/photo.jpg`
- Check filename matches exactly (case-sensitive)
- Ensure image is uploaded to GitHub

### Custom Domain Not Working?
- DNS changes take 24-48 hours
- Verify DNS records are correct
- Check [DNSChecker.org](https://dnschecker.org)

### Page Looks Broken?
- Ensure ALL files were uploaded
- Check `_config.yml` for syntax errors
- View browser console (F12) for errors

**Full troubleshooting → See README.md**

---

## 📚 Documentation Guide

### For Quick Answers:
- **This file (QUICK_START.md)** - Fast reference

### For Setup:
- **DEPLOYMENT.md** - Complete deployment guide

### For Editing:
- **README.md** - Comprehensive editing guide

### For Specific Tasks:
- **assets/images/README.md** - Image management
- **Comments in YAML files** - Field descriptions

---

## 🎓 Learning Resources

### Never Used GitHub?
- [GitHub Hello World Guide](https://guides.github.com/activities/hello-world/)
- [GitHub Pages Guide](https://pages.github.com/)

### Want to Learn Jekyll?
- [Jekyll Step-by-Step Tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/)
- [Jekyll Documentation](https://jekyllrb.com/docs/)

### Need Markdown Help?
- [Markdown Guide](https://www.markdownguide.org/basic-syntax/)
- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

---

## ✅ 30-Minute Setup Checklist

### GitHub Setup (10 min):
- [ ] Create GitHub account
- [ ] Create repository
- [ ] Upload all files
- [ ] Enable GitHub Pages
- [ ] Verify site loads

### Initial Customization (10 min):
- [ ] Update site title in `_config.yml`
- [ ] Add social media links
- [ ] Update family info in `_data/family.yml`
- [ ] Replace hero image

### Testing (10 min):
- [ ] Test all page links
- [ ] Check mobile responsiveness
- [ ] Verify navigation works
- [ ] Test gallery filtering
- [ ] Check blog posts display

---

## 🚀 Ready to Launch?

### Your Path to a Live Website:

**Phase 1: Deploy** (Today)
→ Follow DEPLOYMENT.md steps 1-2
→ Get site live on GitHub Pages

**Phase 2: Customize** (This Week)
→ Replace photos
→ Update family info
→ Adjust colors (optional)

**Phase 3: Connect Domain** (When Ready)
→ Follow DEPLOYMENT.md Part 3
→ Point belltorres.com to site
→ Enable HTTPS

**Phase 4: Maintain** (Ongoing)
→ Add blog posts
→ Upload new photos
→ Share with family

---

## 💬 Final Notes

### This Website Is:
- ✅ Modern and mobile-responsive
- ✅ Fast and lightweight
- ✅ Easy to update
- ✅ Free to host
- ✅ SEO-friendly
- ✅ Fully customizable

### You Can:
- ✅ Edit everything easily
- ✅ Add unlimited photos
- ✅ Write blog posts in Markdown
- ✅ Change colors and styling
- ✅ Add new pages
- ✅ Track visitors (with Google Analytics)

### You Don't Need:
- ❌ Coding experience
- ❌ Web hosting fees
- ❌ Database setup
- ❌ SSL certificates (GitHub provides)
- ❌ Complicated CMS

---

## 🎉 You're All Set!

Your complete family website is ready to go. Just follow the steps in DEPLOYMENT.md and you'll be live in minutes.

**Questions?** Check the full documentation in README.md and DEPLOYMENT.md.

**Ready to deploy?** Start with DEPLOYMENT.md Part 1.

**Want to customize?** Jump into the YAML files in `_data/`.

---

**Welcome to your new family website!** 🏡

The Bell-Torres Family Website
Built with Jekyll • Powered by GitHub Pages • Made with ❤️
