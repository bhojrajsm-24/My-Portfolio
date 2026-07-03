# Quick Reference Card

## 📁 File Structure
```
portfolio/
├── index.html              ← Main HTML file
├── style.css               ← All styling
├── script.js               ← All functionality
├── README.md               ← Project documentation
├── GETTING_STARTED.md      ← Start here!
├── CUSTOMIZATION_GUIDE.md  ← Detailed customization
├── DEPLOYMENT.md           ← How to deploy
└── assets/
    ├── images/
    │   ├── profile.jpg     ← Your photo
    │   └── project1-6.jpg  ← Project screenshots
    └── resume.pdf          ← Your resume
```

## 🎨 Color Variables (style.css)
```css
--bg-primary: #0B0F19      /* Main background */
--primary: #6C63FF         /* Purple accent */
--secondary: #00E5FF       /* Cyan accent */
--accent: #A855F7          /* Purple variant */
```

## 📝 Key Sections to Update (index.html)

| Section | Line | What to Update |
|---------|------|----------------|
| Hero | 50-70 | Name, title, role |
| About | 100-130 | Biography, story |
| Skills | 150-230 | Skill names & percentages |
| Projects | 250-400 | All 6 projects |
| Education | 420-450 | Degree, CGPA, institution |
| Achievements | 470-510 | Numbers & labels |
| Contact | 520-580 | Email, GitHub, LinkedIn |

## 🔧 Common Customizations

### Change Primary Color
```css
/* In style.css line 10 */
--primary: #YOUR_COLOR;
```

### Adjust Animation Speed
```css
/* In style.css line 15 */
--transition: all 0.3s;  /* Change 0.3s */
```

### Modify Typing Text
```javascript
// In script.js line 50
const texts = ['Text 1', 'Text 2', 'Text 3'];
```

### Update Skill Percentage
```html
<!-- In index.html -->
<span class="skill-percent">85%</span>
<div class="skill-progress" data-progress="85"></div>
```

## 🚀 Deployment Commands

### GitHub Pages
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin URL
git push -u origin main
```

### Update Site
```bash
git add .
git commit -m "Update"
git push
```

## 📱 Responsive Breakpoints

| Device | Width | What Changes |
|--------|-------|--------------|
| Desktop | >1024px | Full layout |
| Tablet | 768-1024px | 2 columns → 1 column |
| Mobile | <768px | Mobile menu, stacked layout |

## 🎯 Essential Links to Update

1. **Email** (3 places):
   - Hero section social links
   - Contact section
   - Contact details

2. **GitHub** (4+ places):
   - Hero social
   - Contact details
   - All project cards

3. **LinkedIn** (2 places):
   - Hero social
   - Contact details

## ⚡ Performance Tips

- Compress images: Use TinyPNG
- Recommended sizes:
  - Profile: 400x400px
  - Projects: 800x600px
- Format: JPG or WebP
- Total page size: <2MB

## 🐛 Quick Fixes

### Images Not Loading?
1. Check filename matches exactly
2. Verify file in `assets/images/`
3. Check path spelling

### Animations Not Working?
1. Open Console (F12)
2. Look for errors
3. Refresh browser

### Mobile Menu Stuck?
1. Clear cache (Ctrl+Shift+Delete)
2. Check on real mobile device

## 📊 Testing Checklist

Before deploying:
- [ ] All images load
- [ ] All links work
- [ ] Mobile menu functions
- [ ] Form validates
- [ ] No console errors (F12)
- [ ] Fast loading (<3s)
- [ ] Works on Chrome, Firefox, Safari
- [ ] Responsive on all sizes

## 🔗 Useful Resources

- **Icons**: fontawesome.com
- **Fonts**: fonts.google.com
- **Colors**: coolors.co
- **Images**: unsplash.com
- **Compress**: tinypng.com
- **Test Mobile**: responsively.app
- **Deploy**: github.com/pages

## 💡 Pro Tips

1. **Update regularly**: Refresh every 3 months
2. **Real content**: Use actual project screenshots
3. **Proofread**: No typos!
4. **Mobile first**: Most traffic is mobile
5. **Keep it fast**: Optimize images
6. **Be honest**: Don't exaggerate skills
7. **Test thoroughly**: Multiple browsers/devices
8. **Get feedback**: Ask mentors to review

## 📞 Need Help?

1. Check `GETTING_STARTED.md` first
2. Read `CUSTOMIZATION_GUIDE.md` for details
3. See `DEPLOYMENT.md` for going live
4. Open `create-placeholders.html` for image help

## 🎓 Internship-Ready Checklist

- [ ] Professional photo
- [ ] Real project screenshots
- [ ] Working demo links
- [ ] Updated resume
- [ ] Correct contact info
- [ ] No grammar errors
- [ ] Fast loading speed
- [ ] Mobile responsive
- [ ] All links tested
- [ ] HTTPS enabled

---

**Remember**: Quality over quantity. 3 great projects beat 10 mediocre ones!
