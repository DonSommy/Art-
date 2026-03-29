# Luminary Gallery — Static HTML Site

A luxury fine art gallery website built with pure HTML, CSS, and JavaScript.  
**No server required** — deploys instantly to Vercel or any static host.

---

## 🚀 Deploy to Vercel (5 minutes)

### Step 1 — Push to GitHub

```bash
# Create a new repo on github.com, then:
git init
git add .
git commit -m "Initial commit — Luminary Gallery"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/luminary-gallery.git
git push -u origin main
```

### Step 2 — Deploy on Vercel

1. Go to [vercel.com](https://vercel.com) and sign in with GitHub
2. Click **"Add New Project"**
3. Import your `luminary-gallery` repository
4. Leave all settings as default — Vercel auto-detects static HTML
5. Click **"Deploy"** ✓

Your site will be live at `https://luminary-gallery.vercel.app` (or your custom domain).

---

## ✨ Features

- **12 artworks** with full details, images, and pricing
- **Category filters** (Abstract, Landscape, Seascape, Figurative, etc.)
- **Live search** by title, artist, or style
- **Artwork detail modal** with full specs
- **Pre-order form** — marks artwork as Reserved, saves order to localStorage
- **Contact form** with subject selector
- **Scroll-reveal animations** and toast notifications
- **Fully responsive** — mobile, tablet, desktop
- All data persisted via **localStorage** (no backend needed for testing)

---

## 📁 Files

```
luminary-gallery/
├── index.html      ← Entire site (HTML + CSS + JS, self-contained)
├── vercel.json     ← Vercel deployment config
└── README.md       ← This file
```

---

## 🎨 Customise

**Change gallery name:** Search for `Luminary Gallery` in `index.html` and replace.

**Add/edit artworks:** Find the `ARTWORKS_SEED` array in the `<script>` block:
```javascript
const ARTWORKS_SEED = [
  { id:1, title:'Your Title', artist:'Artist Name', price:5000, ... },
  // add more here
];
```

**Change colors:** Edit CSS variables at the top of the `<style>` block:
```css
:root {
  --gold:     #b8963e;   /* accent color */
  --charcoal: #1c1917;   /* dark color */
  --ivory:    #faf7f2;   /* background */
}
```

**Contact details:** Search for `12 Artisan Quarter` and `contact@luminarygallery.com` to update.

---

## 🔄 When You're Ready for a Real Backend

When you're happy with the design and want to go live with real orders:
- Connect the pre-order form to a service like **Formspree**, **Netlify Forms**, or **EmailJS**
- Or swap back to the PHP/MySQL version for full database support
- All form HTML is already in place — just change the `submit` handler in the JS

---

## 📝 Notes

- Pre-orders and artwork status changes are saved to **localStorage** — they persist across browser sessions on the same device but are not shared across users (this is expected for a prototype/demo)
- To reset all data: open browser DevTools → Application → Local Storage → delete `luminary_artworks_v1` and `luminary_orders_v1`
