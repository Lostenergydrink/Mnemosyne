# The Raymond Tatum Dolly Archive

> *"Southern Belle walked into the Smithsonian"*

A refined, museum-style GitHub Pages site hosting restored photographs and animated memories of Raymond Tatum's lifelong devotion to Dolly Parton. Each exhibit is treated with the dignity of a gallery piece—elegant, tasteful, and designed for both digital viewing and physical QR code access.

---

## 🎨 Design Philosophy

This archive embodies **Dolly's authentic aesthetic**: refined Southern glamour meets museum curation. The design uses her signature color palette—cream, soft blush, champagne gold, and light rose—with minimal sparkle accents and elegant typography.

### Color Palette
- **Cream** (#FAF8F4) - Primary background
- **Soft Blush** (#F7D7E2) - Accent highlights
- **Champagne Gold** (#D9C8A0) - Borders and sparkles
- **Light Rose** (#F3C4CD) - Title accents
- **Charcoal** (#333333) - Primary text

### Typography
- **Headings**: Georgia, Playfair Display, Cormorant (serif)
- **Body**: System sans-serif stack

---

## 📁 Project Structure

```
e:/Mnemosyne/
├── index.html                  # Main landing page (museum lobby)
├── exhibits/
│   ├── exhibit-1.html          # Individual exhibit page
│   ├── exhibit-2.html
│   └── exhibit-3.html
├── assets/
│   ├── css/
│   │   └── styles.css          # Complete stylesheet
│   ├── images/
│   │   ├── exhibit-1.jpg       # Still photographs (add your files here)
│   │   ├── exhibit-2.jpg
│   │   └── exhibit-3.jpg
│   └── videos/
│       ├── exhibit-1.mp4       # Animated restorations (add your files here)
│       ├── exhibit-2.mp4
│       └── exhibit-3.mp4
├── .gitignore
└── README.md                   # This file
```

---

## 🚀 Quick Start

### 1. Adding Media Files

Replace the placeholder paths with your actual files:

**For Images** (`.jpg`, `.png` recommended):
1. Place your restored photo in `assets/images/`
2. Name it descriptively: `exhibit-1.jpg`, `exhibit-2.jpg`, etc.
3. Recommended specs: 1920px wide max, optimized for web (<500KB ideal)

**For Videos** (`.mp4` recommended):
1. Place your animated restoration in `assets/videos/`
2. Name it to match: `exhibit-1.mp4`, `exhibit-2.mp4`, etc.
3. Recommended specs: H.264 codec, 30fps, 1080p or 720p, <10MB ideal
   - **Archive convention**: the live site currently uses a single consolidated clip per exhibit named `vid-a.mp4`, `vid-b.mp4`, etc. Keep those filenames exact (including lowercase) so the HTML references stay in sync on case-sensitive hosts.

### 2. Creating a New Exhibit

To add **Exhibit No. 4**:

#### Step A: Update `index.html`
Add a new card to the exhibits grid:

```html
<article class="exhibit-card">
  <div class="exhibit-number">Exhibit No. 4</div>
  <h3>Your Exhibit Title</h3>
  <p class="exhibit-description">
    Brief description of the exhibit (2-3 sentences).
  </p>
  <a href="exhibits/exhibit-4.html" class="view-exhibit-link">View Exhibit</a>
</article>
```

#### Step B: Create `exhibits/exhibit-4.html`
Duplicate an existing exhibit HTML file and update:

1. **Title tags** in `<head>`
2. **Exhibit header** (title and subtitle)
3. **Video source**: `../assets/videos/exhibit-4.mp4`
4. **Image source**: `../assets/images/exhibit-4.jpg`
5. **Alt text** for accessibility
6. **Caption text** with the story behind the photo

#### Step C: Add Media Files
- Place `exhibit-4.jpg` in `assets/images/`
- Place `exhibit-4.mp4` in `assets/videos/`

---

## 🌐 Deploying to GitHub Pages

### Initial Setup

1. **Create a new GitHub repository**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Raymond Tatum Dolly Archive"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   git push -u origin main
   ```

2. **Enable GitHub Pages**
   - Go to your repo → **Settings** → **Pages**
   - Under "Source", select **Deploy from a branch**
   - Choose **main** branch and **/ (root)**
   - Click **Save**

3. **Wait 2-5 minutes**, then visit:
   ```
   https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
   ```

### Updating the Site

```bash
# After making changes
git add .
git commit -m "Add exhibit 4: [Title]"
git push
```

GitHub Pages will automatically rebuild in 1-2 minutes.

---

## 📱 QR Code Integration

Each exhibit page has a dedicated URL perfect for QR codes:

```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/exhibits/exhibit-1.html
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/exhibits/exhibit-2.html
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/exhibits/exhibit-3.html
```

### Recommended QR Code Generators
- [QR Code Generator](https://www.qr-code-generator.com/) (free, customizable)
- [QRCode Monkey](https://www.qrcode-monkey.com/) (free, no watermark)

**Pro Tip**: Print QR codes on elegant cardstock that matches the cream/gold aesthetic.

---

## ✨ Design Details

### The "Dolly Sparkle" Implementation
- Tiny `✦` characters (1-2 per page max)
- Champagne gold (#D9C8A0) at 40% opacity
- Positioned in corners or as dividers
- **Never** overdone—this is refined elegance, not a craft fair

### Frame Effect on Media
- 8px pearl white border
- Soft drop shadow with layered depth
- Subtle inner border in champagne gold
- Creates the effect of a real picture frame

### Hover Interactions
- Cards lift 2px on hover with gold shadow
- Links underline smoothly on hover
- All animations respect `prefers-reduced-motion`

---

## 🛠️ Technical Standards

### Best Practices Implemented
- ✅ **100% Static**: No build tools, no JavaScript frameworks
- ✅ **Semantic HTML5**: Proper use of `<article>`, `<section>`, `<header>`, `<footer>`
- ✅ **Accessible**: ARIA labels, proper alt text, keyboard navigation
- ✅ **Responsive**: Mobile-first design with breakpoints
- ✅ **Performance**: Optimized CSS, no external dependencies
- ✅ **SEO**: Meta descriptions, meaningful page titles

### Browser Support
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

---

## 📝 Maintenance Guide

### Regular Tasks
1. **Add new exhibits** as restoration work is completed
2. **Optimize media** before uploading (compress images/videos)
3. **Test on mobile** after significant updates
4. **Update captions** as more historical context is discovered

### File Size Guidelines
- **Images**: <500KB ideal, 1MB max
- **Videos**: <10MB ideal, 20MB max
- Use tools like [TinyPNG](https://tinypng.com/) for images
- Use [HandBrake](https://handbrake.fr/) for video compression

### Accessibility Checklist
- [ ] All images have descriptive alt text
- [ ] Heading hierarchy is logical (H1 → H2 → H3)
- [ ] Color contrast meets WCAG AA standards (currently exceeds)
- [ ] All interactive elements have focus styles
- [ ] Videos have captions or transcripts (if spoken content exists)

---

## 🎭 About the Aesthetic

This site walks the line between:
- **Too understated** ❌ (boring museum catalog)
- **Just right** ✅ (refined Southern belle elegance)
- **Too sparkly** ❌ (craft store explosion)

**North Star**: Dolly's *White Limozeen* album art meets a modern Smithsonian brochure.

---

## 📄 License

For private, non-commercial use. All photographs and videos remain the property of Raymond Tatum and are shared here as a personal archive and tribute.

---

## 🤝 Credits

- **Concept & Curation**: Raymond Tatum's devotion to Dolly Parton
- **Design Philosophy**: "Southern Belle walked into the Smithsonian"
- **Technical Implementation**: Static HTML/CSS with museum-grade presentation

---

**Questions?** This is a self-contained static site. No server required, no dependencies, no complexity. Just elegant, timeless presentation of cherished memories.
