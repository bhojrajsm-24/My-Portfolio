# Getting Started with Your Portfolio

Welcome! Your premium portfolio website is ready. Follow these simple steps to personalize and launch it.

## 🚀 Quick Start (5 Minutes)

### Step 1: Add Your Images
1. Add your profile photo as `assets/images/profile.jpg`
2. Add 6 project screenshots as `project1.jpg` through `project6.jpg`
3. All images go in the `assets/images/` folder

### Step 2: Add Your Resume
- Place your resume PDF as `assets/resume.pdf`

### Step 3: Update Contact Info
Open `index.html` and find/replace:
- `bhojraj@example.com` → your email
- `github.com/bhojraj` → your GitHub
- `linkedin.com/in/bhojrajmahajan` → your LinkedIn

### Step 4: Test Locally
- Double-click `index.html` to open in browser
- Check all sections load correctly
- Test on mobile (F12 → Device Toolbar)

### Step 5: Deploy Online (Choose One)

#### Option A: GitHub Pages (Recommended)
```bash
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin YOUR_REPO_URL
git push -u origin main
```
Then enable GitHub Pages in repo settings.

#### Option B: Netlify
1. Go to netlify.com
2. Drag and drop your portfolio folder
3. Done! Your site is live

#### Option C: Vercel
1. Go to vercel.com
2. Import your GitHub repository
3. Deploy with one click

## 📝 Essential Customizations

### Update Personal Info
File: `index.html`

**Find and replace:**
- `Bhojraj Mahajan` → Your Name
- `AI & Data Science Engineering Student` → Your Current Status
- `Aspiring Data Analyst` → Your Career Goal

### Update About Section
Around line 100 in `index.html`, rewrite the three paragraphs to tell your story.

### Update Skills
Around line 150-230, adjust the skill percentages:
```html
<span class="skill-percent">85%</span>  <!-- Change this -->
<div class="skill-progress" data-progress="85"></div>  <!-- And this -->
```

### Update Projects
For each project (6 total), update:
- Image source
- Title
- Description
- GitHub URL
- Live demo URL
- Tech tags

### Update Education
Around line 420, update:
- Degree name
- Institution
- Years
- CGPA
- Description

### Update Achievements
Around line 470, update the numbers:
```html
<div class="achievement-count" data-target="YOUR_NUMBER">0</div>
```

## 🎨 Optional Customizations

### Change Colors
Edit `style.css` at the top (line 5-20):
```css
:root {
    --primary: #6C63FF;     /* Your color */
    --secondary: #00E5FF;   /* Your color */
    --accent: #A855F7;      /* Your color */
}
```

### Change Fonts
1. Visit [Google Fonts](https://fonts.google.com/)
2. Select your fonts
3. Replace the Google Fonts link in `index.html`
4. Update CSS variables in `style.css`

### Adjust Animations
In `style.css`, find:
```css
--transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
```
Change `0.3s` to speed up or slow down animations.

## ✅ Pre-Launch Checklist

- [ ] All images added and loading
- [ ] Resume PDF uploaded
- [ ] Contact information updated
- [ ] All personal details customized
- [ ] Skills and percentages accurate
- [ ] All 6 projects updated
- [ ] GitHub/LinkedIn links working
- [ ] Tested on desktop
- [ ] Tested on mobile
- [ ] No console errors (F12)
- [ ] Fast loading speed

## 🐛 Troubleshooting

**Images not showing?**
- Check file names match exactly (case-sensitive)
- Verify files are in `assets/images/` folder
- Check file extensions (.jpg vs .jpeg)

**Animations not working?**
- Open browser console (F12)
- Check for JavaScript errors
- Try a different browser

**Mobile menu not working?**
- Clear browser cache
- Check on actual mobile device
- Verify JavaScript is enabled

**Form not submitting?**
- Configure Formspree or another form service
- See CUSTOMIZATION_GUIDE.md for details

## 📚 Need More Help?

- **Full customization details:** See `CUSTOMIZATION_GUIDE.md`
- **Technical documentation:** See `README.md`
- **Image guidelines:** Open `create-placeholders.html` in browser

## 🎯 Next Steps

After launching your basic portfolio:

1. **Gather Feedback**
   - Share with friends/mentors
   - Ask for honest opinions
   - Iterate on design

2. **Optimize Performance**
   - Compress images (TinyPNG)
   - Test Lighthouse score
   - Improve load times

3. **Enhance Content**
   - Add more projects as you build them
   - Update achievements regularly
   - Keep resume current

4. **Monitor Analytics**
   - Add Google Analytics
   - Track visitor behavior
   - Optimize based on data

5. **Maintain Regularly**
   - Update projects quarterly
   - Refresh design annually
   - Keep technologies current

## 🌟 Pro Tips

1. **Keep it Updated**: Refresh your portfolio every 3-6 months
2. **Quality Over Quantity**: 3 great projects > 10 mediocre ones
3. **Real Screenshots**: Use actual project images, not stock photos
4. **Tell Stories**: Explain the problem you solved, not just tech used
5. **Mobile First**: Most recruiters view on mobile devices
6. **Fast Loading**: Compress images, keep code lean
7. **Proofread**: No typos! Have someone review your content
8. **Be Authentic**: Let your personality show through

## 💼 Making It Internship-Ready

- Use a professional photo
- Proofread all text multiple times
- Ensure all links work
- Add real, working project demos
- Keep descriptions honest and accurate
- Include contact information
- Test on multiple devices
- Get feedback from mentors
- Check for accessibility
- Optimize for speed

---

**Ready to launch?** Start with Step 1 above! 🚀

Questions? Check the other documentation files or create an issue on GitHub.

Good luck with your internship search! 💪
