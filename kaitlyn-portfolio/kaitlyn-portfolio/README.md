# Kaitlyn Rawlings — Portfolio Website

Restoration Ecology & GIS Portfolio Site · Built for GitHub Pages

---

## 🚀 How to deploy on GitHub Pages

1. **Create a new GitHub repository**
   - Go to github.com → New repository
   - Name it: `kaitlynrawlings.github.io` (this gives you a free custom URL)
   - Set to **Public** (required for free GitHub Pages)
   - Do NOT initialize with a README

2. **Upload these files**
   - Drag and drop this entire folder into the new repo, OR
   - Use `git push` if you're comfortable with the terminal

3. **Enable GitHub Pages**
   - Go to your repo → Settings → Pages
   - Source: "Deploy from a branch"
   - Branch: `main` / `(root)`
   - Click Save

4. **Your site will be live at:**
   `https://kaitlynrawlings.github.io`
   (takes 1–2 minutes to go live after first deploy)

---

## 🔒 Password

The current password is: `watershed2027`

To change it, open `js/main.js` and edit line 7:
```js
const SITE_PASSWORD = 'your-new-password-here';
```

To **remove** the password gate entirely (when you're ready to go public):
- Open `index.html` and delete the `<!-- PASSWORD GATE -->` block
- Open `js/main.js` and delete lines 1–35 (everything under `PASSWORD GATE`)

---

## 🗂 File Structure

```
kaitlyn-portfolio/
├── index.html          ← Main site file
├── css/
│   └── style.css       ← All styles
├── js/
│   └── main.js         ← Password gate, scroll effects, nav
├── maps/               ← Add your map images here
│   ├── pedestrian-improvements-2026.jpg
│   ├── pavement-suitability-2026.jpg
│   └── quindaro-restoration.jpg
├── assets/
│   └── Kaitlyn_Rawlings_Resume_2026.pdf  ← Add your resume PDF
└── README.md
```

---

## 🗺 Adding Your Map Images

1. Export your maps from ArcGIS Pro as JPG or PNG (recommend 1400px wide minimum)
2. Name them:
   - `pedestrian-improvements-2026.jpg`
   - `pavement-suitability-2026.jpg`
   - `quindaro-restoration.jpg`
3. Drop them in the `maps/` folder
4. In `index.html`, find the three `map-thumb` divs and **uncomment** the `<img>` tag inside each (remove the `<!-- -->`)

Example — find this:
```html
<!-- Replace with: <img src="maps/pedestrian-improvements-2026.jpg" alt="..."> -->
<div class="map-placeholder">
```

Replace with:
```html
<img src="maps/pedestrian-improvements-2026.jpg" alt="2026 Pedestrian Improvement Projects map">
```

---

## 📄 Adding Your Resume PDF

1. Drop your resume PDF into the `assets/` folder
2. Name it `Kaitlyn_Rawlings_Resume_2026.pdf`
3. The "Download Full Resume" button in the CV section will work automatically

---

## ✏️ Personalizing Content

All text content is in `index.html`. Sections to update:
- **Hero tagline / bio** — search for `hero-bio` or `hero-tagline`
- **About text** — search for `about-text`
- **GitHub URL** — search for `github.com/kaitlynrawlings` and update to your real username
- **Project descriptions** — update when you have more detail on the toolbox write-up

---

## 🎨 Changing the Password Color Theme

Colors are defined as CSS variables at the top of `css/style.css`:
```css
:root {
  --sand:  #C8B89A;   /* warm accent */
  --sage:  #7A8C6E;   /* green accent / headings */
  --rust:  #A05C3A;   /* orange-brown / labels */
  --deep:  #181D24;   /* page background */
  --fog:   #E8E2D9;   /* body text */
  --cream: #F2EDE6;   /* heading text */
}
```
