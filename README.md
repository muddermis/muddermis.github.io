# muddermis — App Developer Promo Site

A clean, static promo and support site for iOS apps by muddermis.

## Deploy to GitHub Pages

1. **Create a new repo** named `muddermis.github.io` on GitHub
2. **Push this folder's contents** to the repo:

```bash
cd promopage
git init
git add -A
git commit -m "Initial commit — promo site"
git branch -M main
git remote add origin https://github.com/muddermis/muddermis.github.io.git
git push -u origin main
```

3. GitHub Pages will auto-publish at **https://muddermis.github.io/**

## Update App Store Connect URLs

After deploying, update these URLs in App Store Connect:

| App | Field | New URL |
|---|---|---|
| FRZR | Support URL | `https://muddermis.github.io/apps/frzr/` |
| FRZR | Privacy Policy URL | `https://muddermis.github.io/apps/frzr/privacy.html` |
| FRZR | Marketing URL | `https://muddermis.github.io/` |
| DailyFeels | Support URL | `https://muddermis.github.io/apps/dailyfeels/` |
| DailyFeels | Privacy Policy URL | `https://muddermis.github.io/apps/dailyfeels/privacy.html` |
| DailyFeels | Marketing URL | `https://muddermis.github.io/` |

## app-ads.txt

The `app-ads.txt` file is at the root so Google AdMob can find it at:
`https://muddermis.github.io/app-ads.txt`

Make sure the Marketing URL in App Store Connect points to `https://muddermis.github.io/` for AdMob to verify your authorized sellers.

## Adding a New App

1. Add a new app card in `index.html` (see the commented template in the Apps section)
2. Create a new folder: `apps/your-app-slug/`
3. Add these files (copy from an existing app and modify):
   - `index.html` — Support hub
   - `privacy.html` — Privacy Policy
   - `faq.html` — FAQ
   - `terms.html` — Terms of Use (if needed)
4. Add the app icon to `assets/your-app-icon.svg` (or `.png`)
5. Update footer links as needed

## Replacing Placeholder Icons

Replace these SVG placeholders with your actual app icons:
- `assets/frzr-icon.svg` → Replace with actual FRZR icon (PNG or SVG, any size ≥ 200px)
- `assets/dailyfeels-icon.svg` → Replace with actual DailyFeels icon

If using PNG files, update the `src` attributes in the HTML files from `.svg` to `.png`.

## Tech Stack

- Plain HTML/CSS/JS — no build step, no dependencies
- CSS custom properties for theming (light/dark mode)
- Responsive, mobile-first design
- System font stack (-apple-system)
