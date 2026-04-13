# 🚀 ScanIQ Deployment Guide

This guide walks you through deploying your ScanIQ Product Scanner to the internet in **5 minutes**.

## Prerequisites

✅ GitHub account (free at [github.com](https://github.com))  
✅ Netlify account (free at [netlify.com](https://netlify.com))  
✅ OpenRouter API key (free at [openrouter.ai](https://openrouter.ai))  

---

## 🔑 Step 1: Get Your OpenRouter API Key (3 minutes)

1. **Create account** at [openrouter.ai](https://openrouter.ai)
2. **Go to** Settings → API Keys
3. **Copy** your API key (looks like: `sk-or-v1-xxxxxx...`)
4. **Save it somewhere** safe - you'll need it for Netlify

---

## 📤 Step 2: Upload to GitHub (2 minutes)

### In PowerShell:

```powershell
cd "C:\Users\Umaiorubagan\OneDrive\Desktop\Projects\supermarket project"

# Initialize git (if not done already)
git init
git add .
git commit -m "ScanIQ: AI Product Scanner ready for production"
git branch -M main

# Add remote (replace YOUR_USERNAME with your actual GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/scaniq-product-scanner.git

# Push to GitHub
git push -u origin main
```

### If you get an error:
```powershell
# First time? Configure git
git config --global user.email "your-email@example.com"
git config --global user.name "Your Name"

# Then try pushing again
git push -u origin main
```

---

## 🌐 Step 3: Deploy on Netlify (2 minutes)

### Method A: Automatic Deployment (Recommended)

1. **Go to** [netlify.com](https://netlify.com)
2. **Log in** with your GitHub account
3. Click **"Add new site"** → **"Import an existing project"**
4. **Select GitHub**, then authorize Netlify
5. **Choose repository:** `scaniq-product-scanner`
6. **Deploy settings:**
   - Build command: *(leave empty)*
   - Publish directory: `.`
7. Click **"Deploy site"**
8. **Wait 30-60 seconds** for deployment to complete
9. ✅ Your site is LIVE! You'll get a URL like: `https://xxxx-xxxx-xxxx.netlify.app`

### Method B: Manual Deploy (Fastest)

1. Go to [netlify.com](https://netlify.com)
2. **Drag & drop** your entire project folder onto the page
3. ✅ Live in 10 seconds!

---

## 🔐 Step 4: Configure API Key on Netlify (Optional but Recommended)

This keeps your API key secure and separate from code:

1. **In Netlify dashboard**, go to your site
2. Click **"Site settings"** → **"Build & deploy"** → **"Environment"**
3. Click **"Add environment variable"**
4. **Key:** `REACT_APP_OPENROUTER_API_KEY`
5. **Value:** Paste your OpenRouter API key
6. Click **"Save"**
7. **Redeploy:** Go to **"Deploys"** → **"Trigger deploy"** → **"Deploy site"**

✅ Now your app uses the Netlify API key instead of the hardcoded one!

---

## ✅ Verify Your Deployment

### Test the live site:
1. Open the Netlify URL in your browser
2. Grant camera permission when prompted
3. **Try scanning** a real product label
4. Should work instantly without any prompts!

### Troubleshooting:

**Issue:** Camera permission denied
- **Solution:** Check browser settings (Chrome → Settings → Privacy → Camera)

**Issue:** API errors
- **Solution:** Make sure you added the API key to Netlify environment variables

**Issue:** Blank page
- **Solution:** Open DevTools (F12) → Console and check for errors

---

## 🔄 Making Updates

### After any code changes:

```powershell
cd "C:\Users\Umaiorubagan\OneDrive\Desktop\Projects\supermarket project"

git add .
git commit -m "Your change description"
git push origin main
```

**Netlify will automatically redeploy in ~30 seconds!** ✨

---

## 📊 Project Structure

```
supermarket project/
├── product_supermarket.html    # Your main app (all HTML/CSS/JS in one file)
├── README.md                   # Full documentation
├── DEPLOY.md                   # This file
├── .env.example               # Template for environment variables
├── .gitignore                 # Git ignore rules
├── netlify.toml              # Netlify configuration
└── package.json              # Project metadata
```

---

## 🎉 Final Checklist

- [ ] GitHub account created
- [ ] Repository pushed to GitHub
- [ ] Netlify connected to GitHub
- [ ] Site deployed on Netlify
- [ ] OpenRouter API key configured
- [ ] Live URL tested and working
- [ ] Camera permission works
- [ ] Product scanning works

---

## 📱 Share Your App

Your live URL format:
```
https://your-site-name.netlify.app
```

**Share this link!** Anyone can now instantly use your ScanIQ product scanner. 🚀

---

## 🔗 Useful Links

- **Netlify Dashboard:** https://app.netlify.com
- **GitHub:** https://github.com/YOUR_USERNAME/scaniq-product-scanner
- **OpenRouter API:** https://openrouter.io
- **Netlify Docs:** https://docs.netlify.com

---

## 💡 Pro Tips

1. **Custom Domain:** In Netlify → Site settings → Domain management → Add custom domain
2. **Redirects:** Already configured in `netlify.toml`
3. **Build Logs:** Check Netlify dashboard → Deploys → View logs if anything fails
4. **Performance:** HTML file is minified and optimized automatically

---

**🎊 Congratulations! Your app is now live on the internet!**

For more help, check the [README.md](README.md)
