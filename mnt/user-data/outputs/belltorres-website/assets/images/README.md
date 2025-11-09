# Images Directory

This folder contains all images for the Bell-Torres family website.

## Directory Structure

```
assets/images/
├── hero-family.jpg          # Main hero image on homepage
├── favicon.png              # Website favicon
├── family/                  # Family member photos
│   ├── james.jpg
│   ├── namibia.jpg
│   ├── dax.jpg
│   └── baby-placeholder.jpg
├── gallery/                 # Photo gallery images
│   ├── family-portrait-1.jpg
│   ├── dax-beach-1.jpg
│   └── ... (add more here)
├── travel/                  # Travel destination photos
│   ├── bigsur-hero.jpg
│   ├── bigsur-1.jpg
│   └── ... (add more here)
├── hobbies/                 # Hobby-related photos
│   ├── coffee-brewing.jpg
│   ├── tennis.jpg
│   ├── kiteboarding.jpg
│   └── ... (add more here)
└── blog/                    # Blog post images
    ├── bigsur-sunset.jpg
    ├── coffee-pouring.jpg
    └── ... (add more here)
```

## How to Add Images

### Method 1: Using GitHub Website
1. Go to your repository on GitHub
2. Navigate to the appropriate folder (e.g., `assets/images/gallery/`)
3. Click "Add file" → "Upload files"
4. Drag and drop your images
5. Click "Commit changes"

### Method 2: Using Git Command Line
```bash
# Navigate to your local repository
cd belltorres-website

# Copy your images to the appropriate folder
cp ~/Downloads/my-photo.jpg assets/images/gallery/

# Add and commit
git add assets/images/gallery/my-photo.jpg
git commit -m "Add new gallery photo"
git push
```

## Image Guidelines

### Recommended Sizes
- **Hero Image:** 1920x1080px or larger (landscape)
- **Family Member Photos:** 500x500px (square)
- **Gallery Photos:** 1200x800px or larger
- **Blog Post Images:** 1200x630px (landscape)
- **Travel Destination Images:** 1200x800px or larger

### File Format
- Use JPEG (.jpg) for photos
- Use PNG (.png) for graphics with transparency
- Keep file sizes under 500KB for faster loading (use compression tools like TinyPNG)

### File Naming
- Use lowercase letters
- Use hyphens instead of spaces
- Be descriptive: `james-tennis-match.jpg` not `IMG_1234.jpg`
- Include dates if relevant: `2025-10-family-portrait.jpg`

## Placeholder Images

This website is set up with placeholder image paths. You'll need to:

1. **Replace placeholder images** with your actual photos
2. **Keep the same filenames** OR update the paths in the respective `.yml` files
3. **Maintain the directory structure** for everything to work properly

### Quick Start Photo Checklist

Essential photos to add first:
- [ ] Hero/homepage family photo (`hero-family.jpg`)
- [ ] Individual photos: James, Namibia, Dax (`family/` folder)
- [ ] 3-5 gallery photos to start (`gallery/` folder)
- [ ] Featured travel destination photos (`travel/` folder)
- [ ] Hobby photos (`hobbies/` folder)

### Free Stock Photo Resources (For Placeholders)

If you need temporary placeholder images while preparing your own:
- [Unsplash](https://unsplash.com/) - Free high-quality photos
- [Pexels](https://pexels.com/) - Free stock photos
- [Pixabay](https://pixabay.com/) - Free images and videos

## Optimizing Images

To keep your website loading fast:

1. **Resize** images to appropriate dimensions before uploading
2. **Compress** images using tools like:
   - [TinyPNG](https://tinypng.com/) - Online compression
   - [ImageOptim](https://imageoptim.com/) - Mac app
   - [Squoosh](https://squoosh.app/) - Web-based tool

3. **Use appropriate formats:**
   - JPEG for photos (smaller file size)
   - PNG for graphics with transparency
   - WebP for modern browsers (even smaller file size)

## Need Help?

If you're having trouble with images:
1. Check that the file path in your `.yml` file matches the actual location
2. Ensure the filename matches exactly (case-sensitive!)
3. Verify the image uploaded successfully to GitHub
4. Clear your browser cache and refresh

---

**Remember:** All paths in the website code start with `/assets/images/`, so when you upload an image to `assets/images/gallery/vacation.jpg`, you reference it as `/assets/images/gallery/vacation.jpg` in your YAML files.
