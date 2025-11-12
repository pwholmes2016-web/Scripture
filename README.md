# Daily Scripture Memory - Progressive Web App (PWA)

A Progressive Web App for memorizing Bible verses with offline support, audio playback, and installable on any device.

## 🌟 PWA Features

### What's New in the PWA Version:

1. **Installable** - Add to your home screen on mobile or desktop for app-like experience
2. **Offline Access** - Works without internet connection once installed
3. **Native Feel** - Opens in its own window without browser UI
4. **Fast Loading** - Cached resources load instantly
5. **Cross-Platform** - Works on iOS, Android, Windows, Mac, and Linux

## 📱 Installation Instructions

### On Mobile (iOS/Android):

#### iOS (Safari):
1. Open the app in Safari
2. Tap the Share button (square with arrow)
3. Scroll down and tap "Add to Home Screen"
4. Tap "Add"

#### Android (Chrome):
1. Open the app in Chrome
2. Tap the three-dot menu
3. Tap "Add to Home Screen" or "Install App"
4. Tap "Add" or "Install"

### On Desktop:

#### Chrome/Edge:
1. Open the app in your browser
2. Look for the install icon (⊕) in the address bar
3. Click it and select "Install"
4. Or: Click the three-dot menu → "Install Daily Scripture Memory"

#### Safari (Mac):
1. Open the app in Safari
2. File → Add to Dock

## 🚀 Hosting the PWA

To make your PWA accessible online, you need to host it on a web server with HTTPS. Here are some options:

### Option 1: GitHub Pages (Free)
1. Create a GitHub repository
2. Upload all files from the `scripture-pwa` folder
3. Enable GitHub Pages in repository settings
4. Access at: `https://yourusername.github.io/repository-name`

### Option 2: Netlify (Free)
1. Sign up at netlify.com
2. Drag and drop the `scripture-pwa` folder
3. Get instant HTTPS URL

### Option 3: Vercel (Free)
1. Sign up at vercel.com
2. Import your project
3. Deploy with one click

### Option 4: Firebase Hosting (Free tier available)
1. Install Firebase CLI: `npm install -g firebase-tools`
2. Run `firebase init hosting`
3. Run `firebase deploy`

## 📂 Files Included

- `index.html` - Main app file with PWA registration
- `manifest.json` - PWA configuration (name, icons, theme)
- `service-worker.js` - Handles offline caching
- `icon-192.png` - App icon (192x192)
- `icon-512.png` - App icon (512x512)

## 🔧 Technical Details

### Service Worker Features:
- **Cache Strategy**: Cache-first with network fallback
- **Cached Resources**:
  - HTML, CSS, JavaScript
  - External libraries (React, Tailwind, Lucide icons)
  - App icons
- **Automatic Updates**: Old caches cleaned on activation
- **Offline Support**: App works completely offline after first visit

### Browser Compatibility:
- ✅ Chrome/Edge (Desktop & Mobile)
- ✅ Safari (iOS 11.3+, macOS)
- ✅ Firefox (Desktop & Mobile)
- ✅ Samsung Internet
- ✅ Opera

## 💾 Data Storage

The app uses localStorage for data persistence:
- All Scripture passages stored locally
- Data syncs automatically across the same device
- To share data between devices: use Export/Import feature

## 🎨 Customization

### Change Theme Colors:
Edit `manifest.json`:
```json
"background_color": "#fffbeb",  // Background color
"theme_color": "#d97706"        // Status bar color
```

### Update App Name:
Edit `manifest.json`:
```json
"name": "Your App Name",
"short_name": "Short Name"
```

### Replace Icons:
- Replace `icon-192.png` and `icon-512.png` with your custom icons
- Icons should be square and solid color background recommended

## 🐛 Troubleshooting

### Service Worker Not Updating:
1. Clear browser cache
2. Unregister old service worker:
   - Chrome DevTools → Application → Service Workers → Unregister
3. Hard refresh (Ctrl+Shift+R or Cmd+Shift+R)

### App Not Installing:
1. Make sure you're accessing via HTTPS (required for PWA)
2. Check that manifest.json is valid
3. Ensure icons are accessible
4. Try different browser

### Offline Mode Not Working:
1. Visit the app once while online (to cache resources)
2. Check Service Worker is registered (DevTools → Application)
3. Verify cached resources (DevTools → Application → Cache Storage)

## 📝 Notes

- **HTTPS Required**: PWAs require HTTPS (except localhost for testing)
- **First Visit**: App needs one online visit to cache resources
- **Updates**: Service Worker automatically updates when you deploy changes
- **Local Testing**: Use `python3 -m http.server 8000` for local testing

## 🎯 Next Steps

1. Test the app locally
2. Choose a hosting provider
3. Deploy your PWA
4. Share the URL with users
5. Users can install it on their devices

Enjoy your Scripture Memory PWA! 📖
