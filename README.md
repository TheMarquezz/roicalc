# ROI Calculator - Progressive Web App

A beautiful, high-performance recruiting ROI calculator that works anywhere—online or offline.

## ✨ Features

- 📊 **Instant Calculations** - Real-time ROI analysis with detailed breakdowns
- 🔌 **Works Offline** - Full functionality without internet connection
- 📱 **Installable App** - Install on desktop, tablet, or mobile home screen
- ⚡ **Blazing Fast** - Optimized for performance with intelligent caching
- 🎨 **Dark Theme** - Beautiful modern interface with orange accents
- 📋 **Copy Reports** - Export calculations as formatted text

## 🚀 Quick Deploy

### Option 1: GitHub + Cloudflare Pages (Recommended)
```bash
# 1. Create repo on GitHub
git clone https://github.com/YOUR-USERNAME/roi-calculator.git
cd roi-calculator

# 2. Copy files
cp -r /path/to/ROI\ CALCUTALOR_HTML/* .

# 3. Push to GitHub
git add .
git commit -m "Initial commit"
git push origin main

# 4. Go to dash.cloudflare.com → Pages → Connect Git → Select repo
# Done! 🎉 Your site is live at roi-calculator.pages.dev
```

### Option 2: Wrangler CLI
```bash
npm install -g wrangler
wrangler login
wrangler pages deploy .
```

See **QUICK_START.md** for detailed steps or **CLOUDFLARE_DEPLOYMENT.md** for full guide.

## 📁 Project Structure

```
.
├── index.html              # Main app (all-in-one PWA)
├── manifest.json           # PWA metadata
├── service-worker.js       # Offline support & caching
├── wrangler.toml          # Cloudflare deployment config
├── .github/workflows/
│   └── deploy.yml         # Auto-deployment workflow
├── PWA_SETUP.md           # PWA technical docs
├── CLOUDFLARE_DEPLOYMENT.md # Hosting guide
└── QUICK_START.md         # 5-minute setup
```

## 🛠️ Technologies

- **Frontend**: HTML5, vanilla JavaScript, CSS3
- **PWA**: Service Workers, Web App Manifest
- **Hosting**: Cloudflare Pages (free, HTTPS, global CDN)
- **Performance**: Optimized caching strategy, ~50KB total

## 📖 Documentation

- **QUICK_START.md** - Deploy in 5 minutes
- **CLOUDFLARE_DEPLOYMENT.md** - Full deployment guide with troubleshooting
- **PWA_SETUP.md** - Technical PWA documentation

## 🌐 Live Demo

Visit your deployed version:
- After GitHub deployment: `https://roi-calculator.pages.dev`
- After custom domain: `https://yourdomain.com`

## 💻 Local Development

```bash
# Start local server
python3 -m http.server 8000

# Visit
http://localhost:8000
```

Test offline:
1. Open DevTools (F12)
2. Application tab
3. Service Workers → Check status
4. Network tab → Toggle "Offline"
5. Refresh → Should still work!

## 🔒 Privacy & Security

- ✅ **No tracking** - Zero analytics or third-party scripts
- ✅ **No servers** - All calculations run locally
- ✅ **HTTPS only** - Automatic on Cloudflare Pages
- ✅ **Offline-first** - Service Worker caches intelligently

## 📱 Installation

### Desktop
1. Visit your PWA URL
2. Click install icon in address bar
3. Choose to install as app
4. Access from Applications or desktop

### iOS
1. Open in Safari
2. Tap Share button
3. Select "Add to Home Screen"
4. Name it and add

### Android
1. Open in Chrome
2. Tap menu (⋮)
3. Select "Install app"
4. Confirm installation

## 🎯 Browser Support

| Feature | Support |
|---------|---------|
| Web App | All modern browsers |
| PWA Install | Chrome, Edge, Firefox, Opera |
| iOS Home Screen | Safari 15.1+ |
| Offline | All modern browsers |
| Service Worker | All modern browsers |

## ⚙️ Configuration

### Change App Name/Colors
Edit `manifest.json`:
```json
{
  "name": "Your App Name",
  "theme_color": "#ff5500",
  "background_color": "#000000"
}
```

### Update After Deploy
1. Make changes to files
2. Increment cache version in `service-worker.js`
3. Push to GitHub (auto-deploys) or run `wrangler pages deploy .`
4. Users get updates on next visit

## 🐛 Troubleshooting

**PWA won't install?**
- Verify HTTPS is enabled (automatic on Cloudflare)
- Check `manifest.json` is valid
- Clear cache and reload

**Offline not working?**
- Service Worker must be registered
- Visit once online first
- Check DevTools → Application → Service Workers

**Updates not showing?**
- Increment `CACHE_NAME` in `service-worker.js`
- Hard refresh (Cmd+Shift+R / Ctrl+Shift+R)

## 📚 Learn More

- [MDN: Building PWAs](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps)
- [Cloudflare Pages Docs](https://developers.cloudflare.com/pages/)
- [Web.dev: PWA Checklist](https://web.dev/pwa-checklist/)

## 📄 License

This project is open source and available for personal and commercial use.

---

**Ready to deploy?** Start with **QUICK_START.md** 🚀
