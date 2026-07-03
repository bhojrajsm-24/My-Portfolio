# Portfolio Customization Guide

This guide will help you personalize your portfolio website with your own information, images, and styling preferences.

## Quick Start Checklist

- [ ] Replace profile image
- [ ] Add project screenshots
- [ ] Upload your resume
- [ ] Update contact information
- [ ] Modify personal details
- [ ] Adjust colors (optional)
- [ ] Update achievement numbers
- [ ] Add/remove projects
- [ ] Test responsiveness
- [ ] Deploy online

## Step-by-Step Customization

### 1. Personal Information

Open `index.html` and update:

**Hero Section** (Line ~50-70):
```html
<h1 class="hero-title">Your Name</h1>
<p class="hero-subtitle">Your Major/Field</p>
<p class="hero-subtitle-sub">Your Career Goal</p>
```

**Typing Animation** (script.js, Line ~50):
```javascript
const texts = [
    'Your Role 1',
    'Your Role 2',
    'Your Role 3',
    'Your Role 4'
];
```

**About Section** (Line ~100-130):
- Update the bio paragraphs with your story
- Modify the highlight cards to match your strengths

### 2. Contact Information

**Email Address** (multiple locations):
```html
<!-- Hero social links -->
<a href="mailto:your.email@example.com">

<!-- Contact section -->
<a href="mailto:your.email@example.com" class="contact-item">
```

**Social Media Links**:
```html
<!-- GitHub -->
<a href="https://github.com/yourusername" target="_blank">

<!-- LinkedIn -->
<a href="https://linkedin.com/in/yourprofile" target="_blank">
```

### 3. Skills Section

**Adjust Skill Percentages** (Line ~150-230):
```html
<div class="skill-item">
    <div class="skill-header">
        <span class="skill-name">Skill Name</span>
        <span class="skill-percent">XX%</span>  <!-- Update this -->
    </div>
    <div class="skill-bar">
        <div class="skill-progress" data-progress="XX"></div>  <!-- And this -->
    </div>
</div>
```

**Add New Skills**:
Copy an existing skill-item block and modify the name and percentage.

**Remove Skills**:
Delete the entire skill-item div block.

### 4. Projects Section

**Update Project Details** (Line ~250-400):

For each project, modify:

```html
<div class="project-card">
    <div class="project-image">
        <img src="assets/images/your-project.jpg" alt="Your Project">
        <div class="project-overlay">
            <div class="project-links">
                <a href="YOUR_GITHUB_REPO_URL">
                <a href="YOUR_LIVE_DEMO_URL">
```

**Add New Project**:
1. Copy an entire project-card div
2. Update image source
3. Change title and description
4. Update GitHub and demo URLs
5. Modify tech tags

**Remove Project**:
Delete the entire project-card div block.

### 5. Education Section

**Update Institution** (Line ~420-450):
```html
<div class="timeline-date">Your Years</div>
<h3 class="timeline-title">Your Degree</h3>
<p class="timeline-subtitle">Your Major</p>
<p class="timeline-institution">Your Institution</p>
<p class="timeline-description">Your experience description</p>
<div class="timeline-cgpa">
    <span>Current CGPA:</span>
    <strong>X.X/10</strong>  <!-- Update this -->
</div>
```

**Add Multiple Degrees**:
Copy the timeline-item div and add your additional education.

### 6. Achievements Section

**Update Numbers** (Line ~470-510):
```html
<div class="achievement-count" data-target="YOUR_NUMBER">0</div>
<p class="achievement-label">Your Achievement</p>
```

Change both the `data-target` attribute and the label text.

**Add Achievement**:
Copy an achievement-card div and update the icon, number, and label.

### 7. Images

**Profile Image**:
- File: `assets/images/profile.jpg`
- Recommended size: 400x400px
- Format: JPG or PNG
- Keep it professional

**Project Images**:
- Files: `assets/images/project1.jpg` through `project6.jpg`
- Recommended size: 800x600px
- Format: JPG or PNG
- Use actual screenshots or mockups

**Tips for Good Project Images**:
- Use high-quality screenshots
- Crop to show the most important features
- Maintain consistent aspect ratio
- Compress images for faster loading
- Consider using tools like TinyPNG

### 8. Resume

**Add Resume**:
- Place your resume as `assets/resume.pdf`
- Make sure the download link is updated in index.html:
```html
<a href="assets/resume.pdf" class="btn btn-secondary" download>
```

### 9. Color Customization

Edit CSS variables in `style.css` (Line 5-20):

```css
:root {
    /* Background Colors */
    --bg-primary: #0B0F19;        /* Main dark background */
    --bg-secondary: #151922;      /* Secondary background */
    --bg-tertiary: #1a1f2e;       /* Tertiary background */
    
    /* Accent Colors */
    --primary: #6C63FF;           /* Primary purple */
    --secondary: #00E5FF;         /* Cyan accent */
    --accent: #A855F7;            /* Purple accent */
    
    /* Text Colors */
    --text-primary: #ffffff;      /* Main text */
    --text-secondary: #b4b4b4;    /* Secondary text */
    --text-muted: #6b7280;        /* Muted text */
}
```

**Color Scheme Ideas**:


**Blue Theme**:
```css
--primary: #3B82F6;
--secondary: #60A5FA;
--accent: #2563EB;
```

**Green Theme**:
```css
--primary: #10B981;
--secondary: #34D399;
--accent: #059669;
```

**Red/Pink Theme**:
```css
--primary: #EF4444;
--secondary: #F472B6;
--accent: #DC2626;
```

### 10. Typography

**Change Fonts** (index.html, Line 10-15):

1. Go to [Google Fonts](https://fonts.google.com/)
2. Select your fonts
3. Copy the embed code
4. Replace the existing link tag
5. Update CSS variables:

```css
:root {
    --font-primary: 'YourFont', sans-serif;
    --font-secondary: 'YourOtherFont', sans-serif;
}
```

**Popular Font Combinations**:
- Inter + Space Grotesk
- Montserrat + Open Sans
- Raleway + Lato
- Work Sans + Merriweather

### 11. Animation Speed

Adjust animation timing in `style.css`:

```css
:root {
    --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    --transition-smooth: all 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}
```

Change the duration (0.3s, 0.6s) to make animations faster or slower.

### 12. Section Spacing

Adjust padding in `style.css`:

```css
:root {
    --section-padding: 120px 0;  /* Increase or decrease */
}
```

### 13. Form Configuration

To make the contact form functional:

**Using Formspree** (Recommended for beginners):
1. Sign up at [formspree.io](https://formspree.io)
2. Create a new form
3. Copy your form ID
4. Update the form tag in index.html:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" id="contactForm">
```

**Using EmailJS**:
1. Sign up at [emailjs.com](https://www.emailjs.com/)
2. Add EmailJS library to index.html
3. Configure in script.js with your credentials

### 14. SEO Optimization

Update meta tags in `index.html` (Line 5-8):

```html
<meta name="description" content="Your custom description here">
<meta name="keywords" content="your, relevant, keywords">
<meta name="author" content="Your Name">
<title>Your Name | Your Title</title>
```

### 15. Mobile Responsiveness Testing

Test on multiple screen sizes:
- Desktop: 1920px, 1440px, 1024px
- Tablet: 768px, 834px
- Mobile: 375px, 414px, 390px

Use browser DevTools (F12) to test different viewport sizes.

### 16. Performance Optimization

**Image Optimization**:
- Compress images using TinyPNG or Squoosh
- Convert to WebP format for better compression
- Use appropriate image dimensions

**Code Minification** (for production):
- Minify CSS using cssnano or online tools
- Minify JavaScript using Terser
- Remove unused code

### 17. Accessibility Improvements

**Add Alt Text**:
```html
<img src="path/to/image.jpg" alt="Descriptive text">
```

**Ensure Color Contrast**:
Use tools like WebAIM Contrast Checker to verify text is readable.

**Keyboard Navigation**:
Test that all interactive elements can be accessed with Tab key.

## Common Issues & Solutions

### Images Not Loading
- Check file paths are correct
- Verify image files are in assets/images/
- Ensure file extensions match (jpg vs jpeg)

### Animations Not Working
- Check JavaScript console for errors (F12)
- Ensure script.js is loaded correctly
- Verify CSS classes match JavaScript selectors

### Mobile Menu Not Opening
- Check that nav-toggle ID matches JavaScript
- Verify z-index values for proper layering
- Test on actual mobile device, not just DevTools

### Form Not Submitting
- Configure form action with a service like Formspree
- Check browser console for errors
- Ensure all required fields have the 'required' attribute

## Testing Checklist

Before deployment, test:
- [ ] All links work correctly
- [ ] Images load properly
- [ ] Animations run smoothly
- [ ] Form validation works
- [ ] Mobile menu functions
- [ ] Responsive on all screen sizes
- [ ] Cross-browser compatibility
- [ ] Fast loading speed
- [ ] No console errors
- [ ] Accessibility features

## Deployment

Once customized, deploy using:
- **GitHub Pages** (Free, easy)
- **Netlify** (Free, automatic deploys)
- **Vercel** (Free, great for static sites)

Refer to README.md for detailed deployment instructions.

---

Need help? Check the README.md or create an issue on GitHub!
