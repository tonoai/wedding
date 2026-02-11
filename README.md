# 💒 Wedding Invitation Website

Beautiful wedding invitation site based on CineLove Template 39.

## 🎯 Quick Start

1. **Start the server:**
   ```bash
   python3 serve.py
   ```

2. **Open in browser:**
   - Main site: http://localhost:5173
   - Diagnostics: http://localhost:5173/test-replacements.html

3. **Make changes:**
   - Edit `wedding.custom.js` for names, images, text
   - Edit `wedding.custom.css` for styling
   - Hard refresh browser: `Cmd+Shift+R` (Mac) or `Ctrl+Shift+R` (Windows)

## ✨ Current Configuration

### Names
- **Bride:** Quỳnh Nga (born 20.08.2001)
- **Groom:** Tôn Oai (born 06.05.1998)

### Event Details
- **Date:** January 13, 2026, 11:45 AM
- **Venue:** Khách sạn Mường Thanh Luxury Quảng Ninh
- **Location:** Phường Bãi Cháy, tỉnh Quảng Ninh

### Images Configured
- Hero photo: `TANH9717.JPG`
- Gallery photos: `TANH0059.JPG`, `TANH9908.JPG`, `TANH0282.JPG`, `TANH0359.JPG`
- Bride photo: `TANH9908.JPG`
- Groom photo: `TANH0282.JPG`

## 🛠️ Customization

### Change Names, Dates, Venue

Edit `wedding.custom.js`:

```javascript
textReplacements: {
  "Thanh Hằng": "Your Bride Name",
  "THANH HẰNG": "YOUR BRIDE NAME",
  "Minh Trí": "Your Groom Name",
  "MINH TRÍ": "YOUR GROOM NAME",
}
```

### Change Images

1. **Add your photos** to the `images/` folder
2. **Find the node ID:**
   - Set `enableNodeIdClickDebugger: true` in `wedding.custom.js`
   - Refresh page and click on the image
   - Check browser console for the node ID
3. **Update mapping:**
   ```javascript
   imageReplacements: {
     "gtx1PNzpRD": "./images/your-photo.jpg",
   }
   ```

### Change Styling

Edit `wedding.custom.css` to override any styles.

## 📁 Project Structure

```
wedding/
├── index.html                 # Main HTML (exported from CineLove)
├── wedding.custom.js          # ⭐ YOUR CUSTOMIZATIONS (names, images)
├── wedding.custom.css         # ⭐ YOUR STYLES
├── serve.py                   # Development server
├── test-replacements.html     # Diagnostic tool
├── TROUBLESHOOTING.md         # Complete troubleshooting guide
├── START-SERVER.md            # Server usage guide
├── images/                    # ⭐ YOUR PHOTOS
│   ├── TANH9717.JPG
│   ├── TANH0059.JPG
│   └── ... (40 photos)
└── vendor/                    # Next.js files (don't modify)
    ├── framework-*.js
    ├── main-*.js
    ├── font.css
    └── ... (120 files)
```

## 🎨 Features

- ✅ **Exact original design** - Same UI, animations, fonts
- ✅ **Fully customizable** - Names, images, text via config
- ✅ **Mobile responsive** - 417px card width
- ✅ **Scroll animations** - Fade in effects
- ✅ **Calendar widget** - Interactive date display
- ✅ **Photo galleries** - Multiple photo sections
- ✅ **Event details** - Date, time, venue, map
- ✅ **Family info** - Bride & groom families
- ✅ **Music support** - Background music option
- ✅ **No external dependencies** - All files local

## 🚨 Troubleshooting

### Still seeing old names/images?

1. **Hard refresh browser:** `Cmd+Shift+R` or `Ctrl+Shift+R`
2. **Try incognito mode** to rule out cache
3. **Check diagnostics:** http://localhost:5173/test-replacements.html
4. **See full guide:** `TROUBLESHOOTING.md`

### 404 Errors in Console?

The improved `serve.py` server handles these automatically. If you see 404s:
1. Make sure you're using `python3 serve.py` (not simple HTTP server)
2. The site will still work - these are Next.js internal requests

### Changes not applying?

1. Check file is saved
2. Check browser console (F12) for errors
3. Verify syntax in `wedding.custom.js` (no missing commas, quotes)
4. Wait 2-3 seconds after page load

## 📝 Common Tasks

### Add More Photos

1. Copy photo to `images/` folder
2. Click on existing image with debugger enabled
3. Get node ID from console
4. Add to `imageReplacements` in `wedding.custom.js`

### Change Event Details

Edit the HTML directly, or add text replacements:

```javascript
textReplacements: {
  "Khách sạn Mường Thanh": "Your Venue Name",
  "Quảng Ninh": "Your City",
}
```

### Add Background Music

```javascript
musicUrl: "./music.mp3",  // Place music.mp3 in wedding folder
```

### Change Colors/Fonts

Edit `wedding.custom.css`:

```css
/* Example: Change primary text color */
.text-box-component div {
  color: #your-color !important;
}
```

## 🌐 Deployment

### Deploy to Vercel (Recommended)

1. Install Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

3. Follow prompts

### Deploy to Netlify

1. Drag and drop the `wedding` folder to Netlify
2. Site will be live immediately
3. Custom domain available

### Deploy to Any Host

Just upload all files:
- ✅ `index.html`
- ✅ `wedding.custom.js`
- ✅ `wedding.custom.css`
- ✅ `images/` folder
- ✅ `vendor/` folder

No server-side code needed - it's all static!

## 🎯 Best Practices

1. ✅ **Always test locally** before deploying
2. ✅ **Use high-quality images** (current: ~15-20MB each)
3. ✅ **Hard refresh** after making changes
4. ✅ **Keep backups** of your customized files
5. ✅ **Test on mobile** devices
6. ✅ **Check browser compatibility** (Chrome, Safari, Firefox)

## 📚 Documentation

- **`TROUBLESHOOTING.md`** - Complete troubleshooting guide
- **`START-SERVER.md`** - How to run the dev server
- **`test-replacements.html`** - Visual diagnostic tool
- **`wedding.custom.js`** - Inline documentation for all settings

## 🤝 Need Help?

1. Check `TROUBLESHOOTING.md` first
2. Visit diagnostic page: http://localhost:5173/test-replacements.html
3. Open browser console (F12) for errors
4. Verify all files exist and are saved

## 📄 License

Template from CineLove.me - customized for personal use.

---

**🎉 Enjoy your beautiful wedding invitation website!**
