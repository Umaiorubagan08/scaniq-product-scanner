# ScanIQ - AI Product Scanner

A mobile-first web app that uses AI to analyze product labels and provide instant nutrition, allergen, and health information.

## Features

✨ **AI-Powered Analysis** - Uses OpenRouter's free Llama 3.2 model  
📱 **Mobile Responsive** - Works perfectly on iOS & Android  
🎥 **Live Camera** - Real-time product scanning  
🔐 **Privacy-First** - No data stored, analysis happens client-side  
🌍 **Multilingual** - English & Tamil support  
💚 **Free Forever** - Uses completely free OpenRouter API  

## Quick Start

### Local Development

1. **Clone or open the project**
   ```
   cd "path/to/supermarket project"
   ```

2. **Create `.env` file** (optional, uses fallback if missing)
   ```
   cp .env.example .env
   ```
   Edit `.env` and add your OpenRouter API key

3. **Open in browser**
   ```powershell
   # Windows PowerShell
   start product_supermarket.html
   ```

4. **Grant camera permission** when prompted
5. **Start scanning!** 📷

### Getting Your OpenRouter API Key

1. Visit [openrouter.ai](https://openrouter.ai)
2. Sign up (free account)
3. Go to **Settings** → **API Keys**
4. Copy your API key (starts with `sk-or-v1-`)

## Deployment

### Option 1: Netlify (Recommended - 5 minutes)

#### Step 1: Push to GitHub
```powershell
cd "C:\Users\Umaiorubagan\OneDrive\Desktop\Projects\supermarket project"

git init
git add .
git commit -m "Initial commit: ScanIQ product scanner"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/scaniq-product-scanner.git
git push -u origin main
```

#### Step 2: Deploy on Netlify
1. Go to [netlify.com](https://netlify.com)
2. Sign up with GitHub
3. Click **"Add new site"** → **"Import an existing project"**
4. Select your GitHub repository
5. **Settings:**
   - Build command: *(leave empty)*
   - Publish directory: `.`
6. Click **"Deploy"**

#### Step 3: Add API Key (Recommended for Security)
1. Go to **Site Settings** → **Build & Deploy** → **Environment**
2. Add variable: `REACT_APP_OPENROUTER_API_KEY` = `your-api-key`
3. Save and redeploy
4. Your site is LIVE! 🚀

### Option 2: Netlify Drag & Drop (Fastest - 2 minutes)
1. Go to [netlify.com](https://netlify.com)
2. Drag & drop the entire project folder
3. Get instant live URL

### Option 3: GitHub Pages
```powershell
# Create gh-pages branch
git branch gh-pages
git checkout gh-pages
git push origin gh-pages
```
Then enable Pages in GitHub repo settings.

## File Structure

```
supermarket project/
├── product_supermarket.html    # Main app (all-in-one file)
├── .env.example               # Environment variable template
├── .gitignore                 # Git ignore rules
├── netlify.toml              # Netlify configuration
└── README.md                 # This file
```

## Environment Variables

Create `.env` file for local development:
```env
REACT_APP_OPENROUTER_API_KEY=sk-or-v1-your-key-here
```

For Netlify, add via **Site Settings** → **Environment** (more secure)

**Fallback Key:** If no env var is found, the app uses a built-in fallback key (works offline)

## API Information

- **Provider:** [OpenRouter.io](https://openrouter.io)
- **Model:** `meta-llama/llama-3.2-3b-instruct:free`
- **Cost:** FREE
- **Tokens:** Unlimited free tier
- **Documentation:** [OpenRouter API Docs](https://openrouter.ai/docs)

## Mobile Support

✅ **iOS** - iPhone 12, 13, 14, 15+  
✅ **Android** - All modern versions  
✅ **Tablets** - iPad, Samsung Tab, etc.  
✅ **Notches** - Safe area support included  
✅ **Orientation** - Portrait & Landscape  

## Troubleshooting

### Camera not working
- Grant camera permission when prompted
- Check browser permissions (Settings → Privacy)
- Use HTTPS (Netlify provides this automatically)

### API errors
- Verify your OpenRouter API key is correct
- Check internet connection
- Visit status.openrouter.io

### Image analysis issues
- Ensure label is well-lit and in focus
- Try a clearer photo
- Make sure text is readable

## Browser Compatibility

| Browser | iOS | Android |
|---------|-----|---------|
| Safari | ✅ 12+ | N/A |
| Chrome | ✅ 12+ | ✅ Latest |
| Firefox | ✅ 12+ | ✅ Latest |
| Samsung Internet | N/A | ✅ Latest |

## Privacy & Security

🔒 **Zero Data Collection** - No images stored  
🔒 **Client-Side Processing** - Analysis happens in your browser  
🔒 **HTTPS Only** - Secure transmission on Netlify  
🔒 **No Tracking** - No analytics or cookies  

## Support & Debug

To check if API is working:
1. Open browser **DevTools** (F12)
2. Go to **Console** tab
3. Scan a product
4. Look for success/error messages

## License

MIT License - Free to use and modify

## Credits

- **AI Model:** Meta Llama 3.2 via OpenRouter
- **UI/UX:** Custom design with Barlow fonts
- **Hosting:** Netlify

---

**Ready to deploy?** Follow the [Netlify steps](#option-1-netlify-recommended---5-minutes) above! 🚀
