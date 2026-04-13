# 📱 Mobile Camera Setup Guide

Camera access on mobile devices requires specific setup. Follow this guide to get your ScanIQ working perfectly on iPhone and Android.

---

## ⚠️ Critical Requirement: HTTPS (Secure Connection)

Mobile browsers **only allow camera access over HTTPS** (secure connections). This is a security requirement by Apple and Google.

### ❌ These won't work:
- `http://localhost` (desktop OK, mobile NO)
- `http://192.168.1.x` (desktop OK, mobile NO)
- Local file (`file:///Users/...`) - NO

### ✅ These will work:
- `https://your-domain.com` (production)
- `https://xxxx-xxxx-xxxx.netlify.app` (Netlify - FREE)
- `http://localhost` on desktop only

---

## 🚀 Quick Deploy to Netlify (5 minutes)

**Netlify automatically gives you HTTPS for free!**

### Step 1: Push to GitHub
```powershell
cd "C:\Users\Umaiorubagan\OneDrive\Desktop\Projects\supermarket project"

git init
git add .
git commit -m "ScanIQ: Mobile-optimized product scanner"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/scaniq-product-scanner.git
git push -u origin main
```

### Step 2: Deploy on Netlify
1. Go to [netlify.com](https://netlify.com)
2. Click **"Add new site"** → **"Import an existing project"**
3. Select GitHub & authorize
4. Choose your `scaniq-product-scanner` repository
5. Click **"Deploy"** (takes 30-60 seconds)
6. ✅ You get a free HTTPS URL! Example: `https://scaniq-xxx.netlify.app`

### Step 3: Test on Mobile
Open the Netlify URL on your phone:
- Safari (iPhone)
- Chrome (Android)
- Should ask for camera permission automatically

---

## 📱 iPhone Camera Setup

### If camera permission is blocked:

1. **Open Settings** → **Find "ScanIQ"** (or Safari if using browser)
2. **Tap to open** the app settings
3. **Scroll down** and toggle **"Camera"** to **ON** (green)
4. Return to app and tap **"Open Camera"** button again

### iOS Tips:
- ✅ Use **Safari browser** (works best)
- ✅ Add to home screen: Tap Share → **"Add to Home Screen"**
- ✅ Ensure you're using `https://` (check address bar)
- ⚠️ Private/Incognito mode may not work

---

## 🤖 Android Camera Setup

### If camera permission is blocked:

1. **Tap three dots ⋮** (menu) at top right
2. **Tap Settings**
3. **Tap Permissions**
4. **Find "Camera"** and tap it
5. **Tap "Allow"** button
6. Go back to the app and try again

### Android Chrome Tips:
- ✅ Make sure you see **"https://"** in address bar
- ✅ Clear cache if still blocked: Settings → Apps → ScanIQ → Storage → Clear Cache
- ✅ Try a different browser if Chrome doesn't work (Firefox, Samsung Internet)

---

## 🔍 Test Checklist

Before going live, test these on your phone:

- [ ] Can open the site on mobile (check URL starts with `https://`)
- [ ] Camera permission prompt appears
- [ ] Can grant permission
- [ ] Camera feed shows in real-time
- [ ] Can take a photo with the camera button
- [ ] Can upload a photo instead (gallery/upload)
- [ ] Can scan a real product label
- [ ] Results display correctly
- [ ] Both English and Tamil work
- [ ] Audio playback works

---

## ❌ Troubleshooting

### "Camera Access Denied"
✅ **Solution:**
1. Open device **Settings** (not app settings)
2. Find **ScanIQ** or **Safari** 
3. Toggle **Camera permission** ON
4. Refresh the web page

### "No camera found"
✅ **Solution:**
- Your device doesn't have a camera (rare)
- Use **Upload Photo** instead (🖼 button)

### "Camera in use by another app"
✅ **Solution:**
1. Close the other app using camera
2. Return to ScanIQ
3. Try again

### "Your browser does not support camera"
✅ **Solution:**
- Try **Safari** on iPhone
- Try **Chrome** on Android
- Ensure you're using the latest browser version

### Still doesn't work?
✅ **Fallback:**
Use **Upload Photo** (🖼 button) instead
- Works anywhere, anytime
- Same accuracy as camera

---

## 📚 For Developers

### Environment Variables (Optional Security)

For production deployment on Netlify, you can store your API key securely:

1. **Netlify Dashboard** → Your Site
2. **Site Settings** → **Build & Deploy** → **Environment**
3. Add: `REACT_APP_OPENROUTER_API_KEY` = your API key
4. Redeploy
5. App will use secure key instead of hardcoded one

---

## 🔐 Security Notes

✅ **Your data is safe:**
- Images are sent ONLY to Anthropic's Claude
- NO storage on servers
- NO tracking or logging
- Results deleted immediately after display
- Works completely offline if you save your API key

---

## 💡 Pro Tips

1. **Best lighting:** Well-lit, clear product label
2. **Best angle:** Direct overhead, fill the frame
3. **Best distance:** 20-30cm from label
4. **Flip camera:** Use the 🔄 button to switch cameras
5. **Upload as backup:** Always have the 🖼 option

---

**Need help?** Check GitHub issues or contact support.
