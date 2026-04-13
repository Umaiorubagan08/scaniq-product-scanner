# ✅ Pre-Deployment Checklist

Use this checklist before deploying ScanIQ to production.

---

## 📋 Development Phase

### Code Ready
- [ ] `product_supermarket.html` finalized
- [ ] No console errors in browser
- [ ] All features tested locally
- [ ] API key configured
- [ ] No hardcoded secrets in code (except fallback key)

### Features Verified
- [ ] Camera starts instantly
- [ ] Photo capture works
- [ ] Upload fallback works (🖼 button)
- [ ] AI analysis returns results (3-5 seconds)
- [ ] Both English & Tamil display correctly
- [ ] Audio playback works in both languages
- [ ] Tab navigation works (Overview, Nutrition, Pros & Cons, Who Can Use)
- [ ] "Scan Again" button resets UI properly
- [ ] Language toggle switches all text

### Performance Checked
- [ ] Page loads in <2 seconds
- [ ] Camera starts in <1 second (after permission)
- [ ] No memory leaks (open DevTools → Performance)
- [ ] Smooth 30 FPS video feed
- [ ] Button clicks are responsive

---

## 🌐 Deployment Phase

### Netlify Setup
- [ ] GitHub account created
- [ ] Repository pushed to GitHub
- [ ] Netlify account created (netlify.com)
- [ ] Site imported from GitHub
- [ ] Auto deployment enabled
- [ ] Build completes successfully
- [ ] Preview URL works (`https://xxxx-xxxx.netlify.app`)

### Configuration
- [ ] Environment variable `REACT_APP_OPENROUTER_API_KEY` set (optional)
- [ ] Custom domain configured (if applicable)
- [ ] HTTPS enabled (automatic on Netlify)
- [ ] Browser caching configured

### DNS & Domain
- [ ] Domain points to Netlify (if custom domain)
- [ ] SSL certificate valid (should be automatic)
- [ ] DNS propagated (24 hours usually)

---

## 📱 Mobile Testing Phase

### iPhone (Safari)
- [ ] Can open the HTTPS URL
- [ ] Camera permission prompt appears
- [ ] Can grant permission
- [ ] Camera feed shows
- [ ] Can capture photo
- [ ] Can upload from gallery
- [ ] AI analysis works
- [ ] Results display correctly
- [ ] Audio plays
- [ ] Both languages work
- [ ] No crash on orientation change
- [ ] Safe area respected (iPad notch, etc.)

### Android (Chrome)
- [ ] Can open the HTTPS URL
- [ ] Camera permission prompt appears
- [ ] Can grant permission
- [ ] Camera feed shows
- [ ] Can capture photo
- [ ] Can upload from gallery
- [ ] AI analysis works
- [ ] Results display correctly
- [ ] Audio plays
- [ ] Both languages work
- [ ] No crash on orientation change

### Firefox/Edge
- [ ] Camera access works
- [ ] All features functional
- [ ] No browser-specific issues

### Landscape Mode
- [ ] Layout adapts properly
- [ ] Buttons still accessible
- [ ] Video fills screen appropriately
- [ ] Safe area respected

---

## 🔒 Security Phase

### API Key Safety
- [ ] Never commit API key to GitHub (use Netlify env vars)
- [ ] Local storage only for user-entered keys
- [ ] No sensitive data in error messages
- [ ] Camera permissions scoped correctly

### Permissions
- [ ] Only camera permission requested
- [ ] Microphone NOT requested
- [ ] Geolocation NOT requested
- [ ] Storage NOT accessed

### Data Privacy
- [ ] No images stored on server
- [ ] No user tracking
- [ ] No cookies (except optional API key in localStorage)
- [ ] HTTPS enforced
- [ ] Analysis results not logged

---

## 📊 Performance Phase

### Metrics (use Lighthouse)
- [ ] Performance score: >90
- [ ] Accessibility score: >90
- [ ] Best Practices: >90
- [ ] SEO score: >85

### Load Testing
- [ ] Page loads on 4G
- [ ] Page loads on 3G (should be <3 seconds)
- [ ] Handles 100+ concurrent requests (OpenRouter)
- [ ] No memory leaks over time

### Analytics (optional)
- [ ] Google Analytics configured (if desired)
- [ ] Error logging setup (if desired)
- [ ] User feedback mechanism (if desired)

---

## 🧪 QA Phase

### Edge Cases
- [ ] Poor lighting conditions → Clear error message
- [ ] Blurry photos → Error with retry option
- [ ] Invalid product → Error with upload option
- [ ] No camera permission → Permission denied screen with steps
- [ ] Internet disconnected → API error message
- [ ] Browser cache cleared → App still works
- [ ] Multiple tabs open → Each works independently
- [ ] Rotate device mid-scan → Handles gracefully

### Accessibility
- [ ] Can tab through buttons
- [ ] All buttons focusable
- [ ] Color contrast sufficient (WCAG AA)
- [ ] Text readable at 200% zoom
- [ ] Screen reader friendly (aria labels present)

### Responsive
- [ ] 320px width (iPhone SE)
- [ ] 375px width (iPhone XS)
- [ ] 414px width (iPhone Max)
- [ ] 600px width (iPad mini)
- [ ] Landscape 568px height (small landscape)
- [ ] Landscape 812px height (large landscape)

---

## 📚 Documentation Phase

- [ ] README.md updated with features
- [ ] DEPLOY.md has clear step-by-step
- [ ] MOBILE_SETUP.md has troubleshooting
- [ ] TECHNICAL_CHANGES.md documents all fixes
- [ ] API key instructions clear
- [ ] Netlify deployment documented
- [ ] GitHub repo has good description
- [ ] License file present (MIT)

---

## 🚀 Launch Phase

### Pre-Launch
- [ ] All checklist items completed
- [ ] No outstanding bugs
- [ ] Security audit complete
- [ ] Performance optimized
- [ ] Mobile testing passed
- [ ] Documentation published

### Launch Day
- [ ] Deploy to production
- [ ] Verify HTTPS URL is live
- [ ] Test from phone (real device)
- [ ] Monitor error logs
- [ ] Be ready to fix issues

### Post-Launch
- [ ] Monitor user feedback
- [ ] Check analytics (if configured)
- [ ] Fix any reported issues immediately
- [ ] Plan future enhancements
- [ ] Gather user testimonials

---

## 🐛 Issue Resolution Template

If something breaks:

1. **Reproduce** — Can you do it consistently?
2. **Identify** — Desktop? Mobile? Which browser?
3. **Isolate** — Is it API related? Camera? UI?
4. **Fix** — Make change to HTML
5. **Test** — Verify fix on both desktop & mobile
6. **Deploy** — Push to GitHub, Netlify auto-deploys
7. **Monitor** — Confirm fix works for all users

---

## 📞 Support & Maintenance

### User Issues
- Camera not working → Direct to MOBILE_SETUP.md
- Results wrong → Advise better lighting/angle
- API errors → Check OpenRouter account status
- Audio issues → Check device volume/permissions

### Regular Maintenance
- Monitor error logs weekly
- Update OpenRouter API key if needed (yearly)
- Test on new iOS/Android versions
- Update browser compatibility as needed
- Gather feedback quarterly

---

## ✨ Success Criteria

Your deployment is **successful** when:

✅ Users can open the app on mobile  
✅ Camera permission works  
✅ Can scan a real product  
✅ Gets accurate results  
✅ Audio plays in both languages  
✅ No crashes or errors  
✅ Works on iOS and Android  
✅ Fast enough for daily use  

---

## 💡 Pro Tips

1. **Test on real devices**, not just browser emulation
2. **Use Test Accounts** → Deploy to staging first
3. **Monitor Errors** → Set up error logging
4. **Get Feedback** → Ask users for feature requests
5. **Iterate Fast** → Deploy updates multiple times/week
6. **Document Everything** → Future you will thank you

---

**Ready to deploy?** 🚀

1. Check all ✅ items above
2. Push to GitHub
3. Verify on Netlify
4. Test on mobile
5. Launch! 🎉

Good luck! 🌟
