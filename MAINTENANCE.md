# Maintenance & Content Guidelines

Quick reference for maintaining The Raymond Tatum Dolly Archive.

---

## Adding a New Exhibit (Quick Steps)

1. **Prepare your media files**
   - Optimize image: max 1920px wide, <500KB
   - Optimize video: H.264, max 1080p, <10MB
   - Name consistently: `exhibit-N.jpg` and `exhibit-N.mp4`

2. **Add to `index.html`**
   ```html
   <article class="exhibit-card">
     <div class="exhibit-number">Exhibit No. N</div>
     <h3>Title Here</h3>
     <p class="exhibit-description">Description here...</p>
     <a href="exhibits/exhibit-N.html" class="view-exhibit-link">View Exhibit</a>
   </article>
   ```

3. **Duplicate an exhibit page**
   - Copy `exhibits/exhibit-1.html` to `exhibits/exhibit-N.html`
   - Update all titles, paths, and content
   - Write a meaningful caption (2-4 sentences)

4. **Upload media files**
   - `assets/images/exhibit-N.jpg`
   - `assets/videos/exhibit-N.mp4`

5. **Test locally**
   - Open `index.html` in a browser
   - Click through to the new exhibit
   - Check video autoplays (muted)
   - Verify responsive design on mobile

6. **Commit and push**
   ```bash
   git add .
   git commit -m "Add Exhibit N: [Title]"
   git push
   ```

---

## Writing Effective Captions

### Good Caption Structure
1. **Context**: When and where was this taken?
2. **Significance**: Why is this moment important to Ray?
3. **Preservation note**: Brief mention of restoration process

### Example
> "On March 10, 1992, Ray appeared with Dolly on *Good Morning Houston*. This frame has been carefully restored from the original archive, preserving a treasured moment in Ray's lifelong journey as Dolly's most devoted fan."

### Voice Guidelines
- **Respectful and dignified** (museum placard tone)
- **Factual but warm** (not overly sentimental)
- **Brief** (2-4 sentences max)

---

## Style Consistency Checklist

When creating new content, maintain:

- [ ] Exhibit numbering is sequential
- [ ] Titles use en-dash (–) not hyphen (-)
- [ ] All videos have: `controls autoplay loop muted playsinline`
- [ ] All images have descriptive alt text
- [ ] Footer text is identical across all pages
- [ ] "Back to Archive" link uses proper relative path

---

## Media Optimization Tools

### For Images
- **TinyPNG**: https://tinypng.com/
- **Squoosh**: https://squoosh.app/
- **ImageOptim** (Mac): https://imageoptim.com/

### For Videos
- **HandBrake**: https://handbrake.fr/
  - Preset: "Web" or "Fast 1080p30"
  - Format: MP4 (H.264)
  - Quality: RF 22-24
- **FFmpeg** (command line):
  ```bash
  ffmpeg -i input.mp4 -vcodec libx264 -crf 24 -preset slow -vf scale=1920:-1 output.mp4
  ```

---

## Color Reference (CSS Variables)

Located in `assets/css/styles.css`:

```css
--cream: #FAF8F4;          /* Background */
--soft-blush: #F7D7E2;     /* Accent highlights */
--champagne-gold: #D9C8A0; /* Borders, sparkles */
--light-rose: #F3C4CD;     /* Title accents */
--charcoal: #333333;       /* Primary text */
```

**Do not modify these colors** without considering the overall aesthetic coherence.

---

## QR Code Best Practices

1. **Test before printing**
   - Verify URL works on mobile
   - Check exhibit loads properly
   - Test video autoplay on iOS Safari

2. **Print specifications**
   - Minimum size: 2" × 2" (5cm × 5cm)
   - White background essential for scanning
   - Matte finish cardstock recommended

3. **Suggested frame placement**
   - Bottom right corner of frame
   - Or on museum-style placard beneath frame

---

## Troubleshooting

### Videos won't autoplay on mobile
- Ensure `muted` attribute is present
- Check file format is MP4 (H.264)
- iOS requires `playsinline` attribute

### Images look blurry
- Ensure original is at least 1920px wide
- Check compression settings
- Verify file wasn't double-compressed

### Site not updating on GitHub Pages
- Wait 2-5 minutes after push
- Hard refresh browser (Ctrl+Shift+R)
- Check GitHub Actions for build errors

### Exhibits grid looks broken
- Verify closing tags on all `<article>` elements
- Check for missing classes
- Validate HTML at https://validator.w3.org/

---

## Future Expansion Ideas

- **Timeline view**: Chronological display option
- **Search functionality**: Simple JS filter (if needed)
- **Print stylesheets**: Optimized for physical printing
- **High-res downloads**: Link to full-resolution originals (password protected)

---

## Content Backup Strategy

Recommended workflow:
1. Keep original unprocessed files in a separate backup location
2. Commit only web-optimized versions to Git
3. Document restoration process notes separately
4. Maintain a spreadsheet of exhibit metadata

---

**Last Updated**: November 2025
