# ✅ SETUP CHECKLIST

**Simple step-by-step checklist to get your website live**

Print this out or keep it open while you work through the setup!

---

## 📦 PART 1: GitHub Repository Setup

- [ ] Create GitHub account (if you don't have one)
      → Go to github.com and sign up
      
- [ ] Create new repository
      → Click "+" icon → "New repository"
      → Name: `belltorres.com`
      → Make it Public
      → Don't initialize with README
      → Click "Create repository"
      
- [ ] Upload all website files
      → Click "uploading an existing file"
      → Drag ALL folders and files
      → Commit message: "Initial website setup"
      → Click "Commit changes"
      → ⏱️ Wait for upload to complete

---

## 🌐 PART 2: Enable GitHub Pages

- [ ] Go to repository Settings
      → Click "Settings" tab at top
      
- [ ] Navigate to Pages section
      → Click "Pages" in left sidebar
      
- [ ] Configure source
      → Source: "Deploy from a branch"
      → Branch: "main"
      → Folder: "/ (root)"
      → Click "Save"
      
- [ ] Wait for deployment
      → Refresh page after 1-2 minutes
      → Look for "Your site is live at..." message
      
- [ ] Test your site
      → Click the URL (https://yourusername.github.io)
      → Verify homepage loads
      → Check all pages work
      → Test on mobile device

**✅ YOUR SITE IS LIVE!** (even before custom domain)

---

## 🎨 PART 3: Initial Customization

### Update Site Configuration
- [ ] Edit `_config.yml`
      → Update site title and description
      → Add your email
      → Add social media handles
      → Change colors (optional)
      
### Update Family Information
- [ ] Edit `_data/family.yml`
      → Update family member bios
      → Update interests and hobbies
      → Update family story
      
### Replace Photos
- [ ] Upload your photos to `assets/images/` folders
      → Hero image: `assets/images/hero-family.jpg`
      → Family portraits: `assets/images/family/`
      → Gallery photos: `assets/images/gallery/`
      
- [ ] Update photo references
      → Edit `_data/gallery.yml` with your photo info
      → Edit `_data/travels.yml` with your travel photos
      
### Update Content
- [ ] Update travel destinations in `_data/travels.yml`
- [ ] Update hobbies information in `_data/hobbies.yml`
- [ ] Delete example blog posts (optional)
- [ ] Write your first blog post (optional)

**⏱️ After each change, wait 1-2 minutes for site to rebuild**

---

## 🌍 PART 4: Connect Custom Domain (belltorres.com)

### At Your Domain Registrar
- [ ] Log in to your domain registrar
      → Where you bought belltorres.com
      → Find DNS settings
      
- [ ] Add A records
      → Add 4 A records pointing to:
      → 185.199.108.153
      → 185.199.109.153
      → 185.199.110.153
      → 185.199.111.153
      
- [ ] Add CNAME record
      → Type: CNAME
      → Host: www
      → Points to: yourusername.github.io
      
- [ ] Save DNS changes
      → ⏱️ Wait 24-48 hours for propagation

### In GitHub
- [ ] Add custom domain
      → Go to Settings → Pages
      → Custom domain: belltorres.com
      → Click "Save"
      → Wait for DNS check to pass
      
- [ ] Enable HTTPS (after DNS works)
      → Check "Enforce HTTPS"
      → May need to wait a few hours for this option

### Verify Domain Works
- [ ] Test all URLs:
      - [ ] http://belltorres.com
      - [ ] https://belltorres.com
      - [ ] http://www.belltorres.com
      - [ ] https://www.belltorres.com

**✅ YOUR CUSTOM DOMAIN IS LIVE!**

---

## 🔍 PART 5: Testing & Verification

### Desktop Testing
- [ ] Test on Chrome/Safari/Firefox
- [ ] Click all navigation links
- [ ] Test gallery filtering
- [ ] Read a blog post
- [ ] Check images load

### Mobile Testing
- [ ] Test on your phone
- [ ] Open mobile menu
- [ ] Scroll through pages
- [ ] Check image galleries
- [ ] Verify responsiveness

### SEO & Performance
- [ ] Check site appears in Google (takes a few days)
- [ ] Test with Google PageSpeed Insights
- [ ] Verify social media preview works

---

## 📝 PART 6: Optional Enhancements

- [ ] Add Google Analytics
      → Get tracking ID
      → Add to `_config.yml`
      
- [ ] Set up RSS feed reader
      → Your blog has an automatic RSS feed
      → Located at /feed.xml
      
- [ ] Share with family and friends
      → Send them the link!
      
- [ ] Create posting schedule
      → Plan monthly blog updates
      → Schedule photo uploads
      
- [ ] Backup your content
      → GitHub is your backup!
      → Download local copy occasionally

---

## 🎯 30-Day Maintenance Plan

### Week 1: Initial Setup
- [ ] Complete Parts 1-4 above
- [ ] Upload core family photos
- [ ] Write first blog post

### Week 2: Content Addition
- [ ] Add more gallery photos
- [ ] Update hobby details
- [ ] Add travel stories

### Week 3: Refinement
- [ ] Adjust colors/styling if needed
- [ ] Add more blog posts
- [ ] Get feedback from family

### Week 4: Promotion
- [ ] Share on social media
- [ ] Email friends and family
- [ ] Consider SEO optimization

---

## 🆘 Quick Troubleshooting

### Site not loading?
- [ ] Wait 3 minutes and refresh
- [ ] Clear browser cache
- [ ] Check GitHub Actions tab for errors

### Images not showing?
- [ ] Check file paths in YAML files
- [ ] Verify filenames match exactly
- [ ] Ensure images are uploaded

### Domain not working?
- [ ] Wait 24-48 hours for DNS
- [ ] Check DNS with dnschecker.org
- [ ] Verify DNS records are correct

### Need help?
- [ ] Check README.md for detailed instructions
- [ ] Review DEPLOYMENT.md for setup steps
- [ ] Check GitHub Pages documentation

---

## 📅 Ongoing Maintenance Checklist

### Monthly:
- [ ] Write 1-2 blog posts
- [ ] Add new photos to gallery
- [ ] Update any changed family info
- [ ] Check all links still work

### Quarterly:
- [ ] Review and update About page
- [ ] Add new travel destinations
- [ ] Backup website files
- [ ] Check site performance

### Yearly:
- [ ] Update family photos
- [ ] Review and refresh design
- [ ] Add year in review post
- [ ] Clean up old/outdated content

---

## ✅ Success Criteria

You'll know you're done when:
- [✓] Site loads at yourusername.github.io
- [✓] Site loads at belltorres.com
- [✓] All pages are accessible
- [✓] Images display correctly
- [✓] Mobile version works well
- [✓] Blog posts are readable
- [✓] Gallery filtering works
- [✓] Family is excited about it!

---

## 🎉 CONGRATULATIONS!

When you've checked all these boxes, your family website is complete and live!

**Now the real fun begins** - sharing your stories, adding photos, and keeping your family and friends updated on your adventures!

---

**Need detailed instructions?** See README.md and DEPLOYMENT.md

**Questions during setup?** Refer to the Troubleshooting sections in the documentation

**Ready to start?** Begin with Part 1 above!

---

Built with ❤️ for the Bell-Torres Family
