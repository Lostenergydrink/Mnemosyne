# 🚀 Quick Deploy Guide

Get your Dolly archive live in 5 minutes.

---

## Step 1: Initialize Git Repository

```bash
cd e:/Mnemosyne
git init
git add .
git commit -m "Initial commit: The Raymond Tatum Dolly Archive"
```

---

## Step 2: Create GitHub Repository

1. Go to https://github.com/new
2. **Repository name**: `raymond-tatum-dolly-archive` (or your choice)
3. **Description**: "A museum-style archive of Raymond Tatum's treasured photographs with Dolly Parton"
4. **Visibility**: Choose Public or Private
5. **DO NOT** initialize with README (we already have one)
6. Click **Create repository**

---

## Step 3: Push to GitHub

Copy the commands GitHub shows you, or use these (replace YOUR-USERNAME and YOUR-REPO):

```bash
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git branch -M main
git push -u origin main
```

---

## Step 4: Enable GitHub Pages

1. In your GitHub repo, go to **Settings** (top right)
2. Scroll down to **Pages** (left sidebar)
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
4. Click **Save**
5. Wait 2-5 minutes

---

## Step 5: Visit Your Live Site

Your site will be available at:

```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

Example: `https://johnsmith.github.io/raymond-tatum-dolly-archive/`

---

## Step 6: Add Your Media Files

Replace placeholder paths with real files:

1. Add your images to `assets/images/`
   - `exhibit-1.jpg`
   - `exhibit-2.jpg`
   - `exhibit-3.jpg`

2. Add your videos to `assets/videos/`
   - `exhibit-1.mp4`
   - `exhibit-2.mp4`
   - `exhibit-3.mp4`

3. Update and push:
   ```bash
   git add assets/
   git commit -m "Add exhibit media files"
   git push
   ```

---

## 🎯 Next Steps

- [ ] Upload your restored images and videos
- [ ] Update exhibit captions with real stories
- [ ] Generate QR codes for each exhibit URL
- [ ] Test on mobile devices
- [ ] Share the archive link

---

## 🆘 Troubleshooting

**"git: command not found"**
- Install Git: https://git-scm.com/download/win

**"Permission denied (publickey)"**
- Set up SSH keys or use HTTPS URL instead

**Site not showing after 5 minutes**
- Check GitHub Actions tab for errors
- Verify Pages is enabled in Settings
- Try a hard refresh (Ctrl+Shift+R)

**Videos won't play on iPhone**
- Ensure videos are MP4 format (H.264 codec)
- Check that `muted` attribute is present
- File size should be <20MB

---

## 📱 Generate QR Codes

Once live, create QR codes for each exhibit:

**Exhibit URLs:**
```
https://YOUR-USERNAME.github.io/YOUR-REPO/exhibits/exhibit-1.html
https://YOUR-USERNAME.github.io/YOUR-REPO/exhibits/exhibit-2.html
https://YOUR-USERNAME.github.io/YOUR-REPO/exhibits/exhibit-3.html
```

**Recommended QR Code Generator:**
- https://www.qr-code-generator.com/
- Set error correction to "High"
- Download as PNG or SVG
- Print at minimum 2" × 2" size

---

**Questions?** Check `README.md` for full documentation.
