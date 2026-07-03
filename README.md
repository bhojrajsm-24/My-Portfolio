# Bhojraj Mahajan - Portfolio Website

A modern, premium portfolio website showcasing skills, projects, and achievements with smooth animations and responsive design.

## Features

- **Premium Dark Theme** with gradient accents and glass morphism effects
- **Animated Background** with floating gradient blobs and cursor glow
- **Smooth Animations** including typing effect, skill bars, and counter animations
- **Fully Responsive** design for mobile, tablet, and desktop
- **Intersection Observer** for scroll-triggered animations
- **SEO Optimized** with semantic HTML and meta tags
- **Accessible** with ARIA labels and keyboard navigation support

## Tech Stack

- HTML5
- CSS3 (Custom Properties, Flexbox, Grid, Animations)
- Vanilla JavaScript (ES6+)
- Font Awesome Icons
- Google Fonts (Poppins, Outfit)

## Project Structure

```
portfolio/
│
├── index.html          # Main HTML file
├── style.css           # All styles and animations
├── script.js           # Interactive functionality
├── README.md           # Project documentation
│
└── assets/
    ├── images/         # Image files
    │   ├── profile.jpg
    │   ├── project1.jpg
    │   ├── project2.jpg
    │   ├── project3.jpg
    │   ├── project4.jpg
    │   ├── project5.jpg
    │   └── project6.jpg
    │
    └── resume.pdf      # Your resume
```

## Setup Instructions

1. **Clone or download** this repository
2. **Replace placeholder images** in `assets/images/` folder:
   - `profile.jpg` - Your professional photo (400x400px recommended)
   - `project1.jpg` to `project6.jpg` - Your project screenshots (800x600px recommended)
3. **Add your resume** as `assets/resume.pdf`
4. **Update contact information** in `index.html`:
   - Email addresses
   - GitHub URL
   - LinkedIn URL
5. **Customize content**:
   - Update CGPA in the Education section
   - Modify achievement numbers
   - Add/remove projects as needed
6. **Open `index.html`** in your browser

## Customization Guide

### Colors

Edit CSS variables in `style.css`:

```css
:root {
    --bg-primary: #0B0F19;      /* Main background */
    --primary: #6C63FF;          /* Primary accent color */
    --secondary: #00E5FF;        /* Secondary accent color */
    --accent: #A855F7;           /* Accent color */
}
```

### Typography

Change fonts by modifying the Google Fonts import in `index.html` and updating variables in `style.css`:

```css
:root {
    --font-primary: 'Poppins', sans-serif;
    --font-secondary: 'Outfit', sans-serif;
}
```

### Sections

To add or remove sections:
1. Update the HTML in `index.html`
2. Add corresponding navigation link in the navbar
3. Style in `style.css`
4. Add scroll detection in `script.js` if needed

### Projects

Each project card follows this structure:

```html
<div class="project-card">
    <div class="project-image">
        <img src="assets/images/projectX.jpg" alt="Project Name">
        <div class="project-overlay">
            <div class="project-links">
                <a href="GITHUB_URL" class="project-link" target="_blank">
                    <i class="fab fa-github"></i>
                </a>
                <a href="DEMO_URL" class="project-link" target="_blank">
                    <i class="fas fa-external-link-alt"></i>
                </a>
            </div>
        </div>
    </div>
    <div class="project-content">
        <h3 class="project-title">Project Title</h3>
        <p class="project-description">Description</p>
        <div class="project-tech">
            <span class="tech-tag">Technology</span>
        </div>
    </div>
</div>
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Performance

- Minimal dependencies (no frameworks)
- Optimized animations with CSS transforms
- Lazy loading for images
- Efficient JavaScript with event delegation
- Expected Lighthouse score: 95+

## Deployment

### GitHub Pages
1. Push to GitHub repository
2. Go to Settings > Pages
3. Select main branch
4. Your site will be live at `https://yourusername.github.io/repository-name`

### Netlify
1. Drag and drop the folder to Netlify
2. Or connect your GitHub repository
3. Site deploys automatically

### Vercel
1. Import GitHub repository
2. Deploy with one click
3. Automatic deployments on push

## Accessibility Features


- Semantic HTML elements
- ARIA labels where appropriate
- Keyboard navigation support
- Focus indicators for interactive elements
- Sufficient color contrast ratios
- Responsive text sizing

## SEO Optimization

- Meta tags for description and keywords
- Semantic HTML structure
- Alt text for images
- Fast loading times
- Mobile-friendly design

## Contact Form

The contact form includes basic validation and shows an alert on submission. To make it functional:

### Option 1: Formspree
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Option 2: EmailJS
Add EmailJS library and configure with your credentials

### Option 3: Backend API
Connect to your own backend service

## Animation Details

- **Preloader**: Animated logo with loading bar
- **Typing Effect**: Rotates through multiple roles
- **Skill Bars**: Animate on scroll into view
- **Counter Animation**: Numbers count up when visible
- **Fade In**: Cards fade in as you scroll
- **Hover Effects**: Smooth transitions on interactive elements
- **Parallax**: Profile image moves with mouse cursor
- **Floating Animation**: Profile image floats continuously

## Credits

- **Fonts**: Google Fonts (Poppins, Outfit)
- **Icons**: Font Awesome 6.4.0
- **Design Inspiration**: Awwwards, Linear, Vercel, Apple, Framer, Stripe

## License

This project is open source and available for personal and commercial use. Feel free to customize it for your needs.

## Support

If you find any issues or have suggestions, please create an issue in the repository.

## Author

**Bhojraj Mahajan**
- GitHub: [github.com/bhojraj](https://github.com/bhojraj)
- LinkedIn: [linkedin.com/in/bhojrajmahajan](https://linkedin.com/in/bhojrajmahajan)

---

Made with passion and clean code ✨
