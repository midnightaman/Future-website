# Future — Favicon & App Icon Set

Generated from the Future logo mark (the "F" glyph), sized for every browser tab,
iOS home screen, and Android/Chrome context.

## Files in this folder

| File | Used for |
|---|---|
| `favicon.ico` | Classic browser tab icon (16/32/48 combined) |
| `favicon-16x16.png`, `favicon-32x32.png`, `favicon-48x48.png` | Modern browser tabs |
| `apple-touch-icon.png` (180×180) | iOS home screen icon (default lookup) |
| `apple-touch-icon-120x120.png` | iPhone (older retina) |
| `apple-touch-icon-152x152.png` | iPad |
| `apple-touch-icon-167x167.png` | iPad Pro |
| `android-chrome-192x192.png`, `android-chrome-512x512.png` | Android home screen / PWA |
| `maskable-icon-192x192.png`, `maskable-icon-512x512.png` | Android adaptive icon (safe-zone padded so it's not clipped by circle/squircle/rounded masks) |
| `mstile-150x150.png` | Windows Start tile |
| `safari-pinned-tab.svg` | Safari pinned-tab monochrome icon |
| `site.webmanifest` | PWA manifest pointing to the Android icons |
| `browserconfig.xml` | Windows tile config |

## 1. Upload to GitHub

Push this whole `icons/` folder to the root of your site's static assets, e.g.:

```
public/
└── icons/
    ├── favicon.ico
    ├── favicon-16x16.png
    ├── ... (all files above)
```

`favicon.ico` should also be copied to your site root (`/favicon.ico`) since some
browsers still look there by default regardless of what `<head>` says.

## 2. Add this to your HTML `<head>`

```html
<link rel="icon" href="/favicon.ico" sizes="any">
<link rel="icon" type="image/png" sizes="16x16" href="/icons/favicon-16x16.png">
<link rel="icon" type="image/png" sizes="32x32" href="/icons/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="48x48" href="/icons/favicon-48x48.png">

<link rel="apple-touch-icon" sizes="180x180" href="/icons/apple-touch-icon.png">
<link rel="apple-touch-icon" sizes="120x120" href="/icons/apple-touch-icon-120x120.png">
<link rel="apple-touch-icon" sizes="152x152" href="/icons/apple-touch-icon-152x152.png">
<link rel="apple-touch-icon" sizes="167x167" href="/icons/apple-touch-icon-167x167.png">

<link rel="mask-icon" href="/icons/safari-pinned-tab.svg" color="#0B0B0C">
<link rel="manifest" href="/icons/site.webmanifest">
<meta name="msapplication-config" content="/icons/browserconfig.xml">
<meta name="msapplication-TileColor" content="#0B0B0C">
<meta name="theme-color" content="#0B0B0C">
```

That covers: the browser tab icon ("the globe" in the address bar gets replaced
by this once it loads), the iOS "Add to Home Screen" icon, Android/Chrome's
install icon (including adaptive/maskable shapes), Safari's pinned tab, and
Windows Start tiles.
