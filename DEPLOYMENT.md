# Deployment Guide

This guide covers multiple ways to deploy your portfolio online for free.

## Option 1: GitHub Pages (Recommended)

### Prerequisites
- GitHub account
- Git installed on your computer

### Steps

1. **Create GitHub Repository**
   ```bash
   # Navigate to your portfolio folder
   cd portfolio
   
   # Initialize git
   git init
   
   # Add all files
   git add .
   
   # Commit
   git commit -m "Initial portfolio commit"
   ```

2. **Create Repository on GitHub**
   - Go to github.com
   - Click "New Repository"
   - Name it `portfolio` or `yourusername.github.io`
   - Don't initialize with README (you already have files)
   - Click "Create repository"

3. **Push to GitHub**
   ```bash
   git branch -M main
   git remote add origin https://github.com/yourusername/portfolio.git
   git push -u origin main
   ```

4. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to "Pages" section
   - Source: Select "main" branch
   - Click "Save"
   - Wait 1-2 minutes

5. **Access Your Site**
   - URL: `https://yourusername.github.io/portfolio/`
   - Or: `https://yourusername.github.io/` (if repo named correctly)

### Update Your Site
```bash
git add .
git commit -m "Update portfolio"
git push
```

Changes appear live in 1-2 minutes.

---

## Option 2: Netlify

### Method A: Drag and Drop (Easiest)

1. Go to [netlify.com](https://netlify.com)
2. Sign up (free)
3. Click "Add new site" → "Deploy manually"
4. Drag your portfolio folder
5. Done! You get a URL like `random-name-123.netlify.app`

### Method B: Connect GitHub

1. Push code to GitHub (see Option 1, steps 1-3)
2. Go to netlify.com
3. Click "Add new site" → "Import from Git"
4. Connect to GitHub
5. Select your repository
6. Click "Deploy"
7. Automatic deploys on every push!

### Custom Domain (Optional)
1. Go to "Domain settings"
2. Click "Add custom domain"
3. Follow DNS configuration steps

---

## Option 3: Vercel

### Steps

1. Push code to GitHub (see Option 1, steps 1-3)
2. Go to [vercel.com](https://vercel.com)
3. Sign up with GitHub
4. Click "Import Project"
5. Select your portfolio repository
6. Click "Deploy"
7. Done! Get URL like `portfolio-username.vercel.app`

### Automatic Deployments
- Every push to main branch auto-deploys
- Preview deployments for pull requests

---

## Option 4: GitLab Pages

### Steps

1. Create account on [gitlab.com](https://gitlab.com)
2. Create new project
3. Push your code:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://gitlab.com/yourusername/portfolio.git
   git push -u origin main
   ```

4. Create `.gitlab-ci.yml`:
   ```yaml
   pages:
     stage: deploy
     script:
       - mkdir .public
       - cp -r * .public
       - mv .public public
     artifacts:
       paths:
         - public
     only:
       - main
   ```

5. Wait for pipeline to complete
6. Access at `https://yourusername.gitlab.io/portfolio/`

---

## Option 5: Cloudflare Pages

### Steps

1. Push code to GitHub
2. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
3. Sign up/login
4. Click "Create a project"
5. Connect to GitHub
6. Select repository
7. Build settings:
   - Framework preset: None
   - Build command: (leave empty)
   - Build output directory: `/`
8. Click "Save and Deploy"

---

## Option 6: Render

### Steps

1. Push code to GitHub
2. Go to [render.com](https://render.com)
3. Sign up
4. Click "New" → "Static Site"
5. Connect GitHub repository
6. Settings:
   - Build Command: (leave empty)
   - Publish Directory: `.`
7. Click "Create Static Site"

---

## Option 7: Firebase Hosting

### Prerequisites
- Node.js installed
- Firebase CLI: `npm install -g firebase-tools`

### Steps

1. **Initialize Firebase**
   ```bash
   firebase login
   firebase init hosting
   ```

2. **Configuration**
   - Select/create project
   - Public directory: `.` (current directory)
   - Single-page app: No
   - Automatic builds: No

3. **Deploy**
   ```bash
   firebase deploy
   ```

4. **Access**
   - URL: `https://your-project.web.app`

---

## Custom Domain Setup

### For GitHub Pages

1. Buy domain (Namecheap, GoDaddy, etc.)
2. Add file `CNAME` to repository root:
   ```
   yourdomain.com
   ```
3. Configure DNS:
   - Type: A
   - Name: @
   - Value: 185.199.108.153
   - Add 3 more A records with:
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
4. For www subdomain:
   - Type: CNAME
   - Name: www
   - Value: yourusername.github.io

### For Netlify/Vercel

1. Go to domain settings in dashboard
2. Add custom domain
3. Follow DNS configuration instructions
4. Wait for DNS propagation (up to 48 hours)

---

## SSL/HTTPS

All platforms mentioned provide free SSL certificates automatically:
- GitHub Pages: Automatic
- Netlify: Automatic (Let's Encrypt)
- Vercel: Automatic
- Cloudflare: Automatic

---

## Performance Optimization Before Deploy

### 1. Optimize Images
```bash
# Use tools like:
- TinyPNG.com
- Squoosh.app
- ImageOptim (Mac)
```

### 2. Minify CSS (Optional)
Use online tools or:
```bash
npm install -g csso-cli
csso style.css -o style.min.css
```

### 3. Minify JavaScript (Optional)
```bash
npm install -g terser
terser script.js -o script.min.js
```

### 4. Enable Compression
Most hosting platforms enable gzip automatically.

---

## Monitoring and Analytics

### Google Analytics

1. Go to [analytics.google.com](https://analytics.google.com)
2. Create property
3. Get tracking ID
4. Add to `index.html` before `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

---

## Troubleshooting

### Site Not Loading
- Wait 5-10 minutes after deployment
- Clear browser cache
- Check build logs for errors
- Verify file paths are correct

### Images Not Showing
- Check paths are relative, not absolute
- Verify image files are committed to Git
- Check file names match (case-sensitive)

### 404 Errors
- Ensure index.html is in root directory
- Check URL spelling
- Verify deployment completed successfully

### Slow Loading
- Compress images
- Use WebP format
- Enable caching
- Minimize CSS/JS files

---

## Recommended: GitHub Pages

**Why?**
- ✅ Free forever
- ✅ Easy to update (just push)
- ✅ Good performance
- ✅ Automatic HTTPS
- ✅ Custom domain support
- ✅ Perfect for portfolios
- ✅ Version control included

**Quick Deploy:**
```bash
git init
git add .
git commit -m "Portfolio"
git remote add origin YOUR_REPO_URL
git push -u origin main
# Then enable Pages in repo settings
```

---

## Post-Deployment Checklist

- [ ] Site loads correctly
- [ ] All images appear
- [ ] Links work (internal and external)
- [ ] Mobile responsive
- [ ] Forms submit properly
- [ ] No console errors
- [ ] Fast load time (<3 seconds)
- [ ] HTTPS enabled
- [ ] Custom domain configured (if desired)
- [ ] Analytics tracking setup
- [ ] Tested on multiple browsers
- [ ] Shared with friends for feedback

---

## Updating Your Live Site

### GitHub Pages/GitLab
```bash
# Make changes to files
git add .
git commit -m "Update description"
git push
```

### Netlify/Vercel (Git Connected)
Same as above - automatic deployment

### Netlify (Manual Deploy)
Drag and drop updated folder again

---

Need help? Each platform has excellent documentation and support forums!
