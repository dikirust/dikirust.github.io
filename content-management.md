# Content Management Guide - Diki Rustian Portfolio

## Overview

This guide provides step-by-step instructions for updating your portfolio content without technical expertise. The portfolio is built with modular sections that can be easily customized.

## 📁 File Structure

```
dikirust.github.io/
├── index.html                 # Main portfolio page
├── assets/
│   ├── css/
│   │   ├── main.css          # Core styles
│   │   ├── portfolio.css     # Portfolio-specific styles
│   │   ├── theme.css         # Dark theme and colors
│   │   └── animations.css    # Motion effects
│   ├── js/
│   │   └── main.js          # Interactive functionality
│   └── img/                 # Images and assets
└── cv-content.txt           # CV content reference
```

## 🎯 Quick Content Updates

### 1. Personal Information

**Location:** `index.html` - Hero Section (lines ~55-85)

**What to update:**

- Name and title
- Location
- Contact information
- Professional summary

**How to update:**

```html
<!-- Find this section and modify -->
<h1>Your Name</h1>
<p>Your Professional Title</p>
<p>Location: Your City, Country</p>
```

### 2. Professional Summary

**Location:** `index.html` - About Section (lines ~120-140)

**Update the paragraph describing your background:**

```html
<p>Update this with your current professional summary...</p>
```

### 3. Statistics Counter

**Location:** `index.html` - Hero Stats (lines ~85-115)

**Update achievement numbers:**

```html
<div class="stat-item">
  <span class="counter" data-target="5">0</span>+
  <p>Years Experience</p>
</div>
```

### 4. Skills Section

**Location:** `index.html` - Skills Section (lines ~200-280)

**Add/remove skills:**

```html
<div class="progress">
  <span class="skill"> <span>Python</span> <i class="val">95%</i> </span>
  <div class="progress-bar-wrap">
    <div
      class="progress-bar"
      role="progressbar"
      aria-valuenow="95"
      aria-valuemin="0"
      aria-valuemax="100"
      style="width: 95%"
    ></div>
  </div>
</div>
```

### 5. Portfolio Projects

**Location:** `index.html` - Portfolio Section (lines ~400-550)

**To add a new project:**

```html
<div class="col-lg-4 col-md-6 portfolio-item isotope-item filter-app">
  <div class="portfolio-content h-100">
    <div class="project-icon-container">
      <i class="bi bi-your-icon project-icon"></i>
    </div>
    <h4><a href="portfolio-details.html">Project Name</a></h4>
    <p>Project description...</p>
    <div class="tech-stack">
      <span class="tech-badge tech-python">Python</span>
      <span class="tech-badge tech-ai">AI/ML</span>
    </div>
    <a href="portfolio-details.html" class="details-link">
      <i class="bi bi-link-45deg"></i>
    </a>
  </div>
</div>
```

**Available Bootstrap Icons for Projects:**

- `bi-palette-fill` - Design/Creative projects
- `bi-globe` - Web development
- `bi-camera-fill` - Computer vision/AI
- `bi-gear-fill` - Engineering/Technical
- `bi-newspaper` - Content/Media
- `bi-graph-up-arrow` - Analytics/BI
- `bi-cart-fill` - E-commerce
- `bi-chat-square-dots-fill` - Communication/Chat
- `bi-shield-check-fill` - Security/Quality

### 6. Work Experience

**Location:** `index.html` - Resume Section (lines ~300-400)

**Add new position:**

```html
<div class="resume-item">
  <h4>Job Title</h4>
  <h5>Start Date - End Date</h5>
  <p><em>Company Name, Location</em></p>
  <ul>
    <li>Achievement or responsibility 1</li>
    <li>Achievement or responsibility 2</li>
    <li>Achievement or responsibility 3</li>
  </ul>
</div>
```

## 🎨 Styling Customization

### Color Scheme

**Location:** `assets/css/theme.css` - CSS Variables (lines 1-20)

**To change accent colors:**

```css
:root {
  --accent-primary: #149ddd; /* Main blue */
  --accent-secondary: #1a8bb8; /* Secondary blue */
  /* Change these hex values to your preferred colors */
}
```

### Portfolio Project Themes

**Location:** `assets/css/portfolio.css` - Gradient Themes (lines 50-120)

**Available gradient themes:**

- `gradient-ai` - AI/ML projects (blue-purple)
- `gradient-web` - Web development (green-blue)
- `gradient-data` - Data analytics (orange-red)
- `gradient-iot` - IoT projects (purple-pink)
- `gradient-mobile` - Mobile apps (teal-blue)

**To assign a theme to a project:**

```html
<div class="project-icon-container gradient-ai">
  <!-- Project content -->
</div>
```

### Technology Badges

**Location:** `assets/css/portfolio.css` - Tech Badge Styles (lines 120-180)

**Available tech badge styles:**

- `tech-python` - Python (blue)
- `tech-ai` - AI/ML (purple)
- `tech-web` - Web tech (green)
- `tech-data` - Data (orange)
- `tech-mobile` - Mobile (teal)

## 📱 Adding New Sections

### 1. Create Section Structure

```html
<section id="new-section" class="new-section section">
  <div class="container section-title" data-aos="fade-up">
    <h2>Section Title</h2>
    <p>Section description</p>
  </div>

  <div class="container" data-aos="fade-up" data-aos-delay="100">
    <!-- Section content here -->
  </div>
</section>
```

### 2. Add to Navigation

**Location:** `index.html` - Navigation Menu (lines ~45-55)

```html
<li><a href="#new-section">Section Name</a></li>
```

## 🖼️ Image Management

### Profile Images

**Location:** `assets/img/`

- `my-profile-img.jpg` - Main profile photo
- `hero-bg.jpg` - Hero background (optional)

**Recommended sizes:**

- Profile image: 400x400px (square)
- Hero background: 1920x1080px (landscape)

### Portfolio Images

**Location:** `assets/img/portfolio/`

**To add project images:**

1. Upload image to `assets/img/portfolio/`
2. Update project HTML:

```html
<img
  src="assets/img/portfolio/your-project.jpg"
  class="img-fluid"
  alt="Project Name"
/>
```

## 🔧 Technical Tips

### 1. Testing Changes

1. Save your changes
2. Open `index.html` in a browser
3. Use Ctrl+F5 to hard refresh (clear cache)

### 2. Common Issues

- **Changes not showing:** Clear browser cache (Ctrl+F5)
- **Layout broken:** Check for missing closing tags `</div>`
- **Animations not working:** Ensure `data-aos` attributes are present

### 3. Animation Control

**To disable animations on mobile:**

```css
@media (max-width: 768px) {
  .animation-class {
    animation: none !important;
  }
}
```

## 📋 Content Checklist

### Before Publishing:

- [ ] Update personal information
- [ ] Verify all links work
- [ ] Check mobile responsiveness
- [ ] Spell-check all content
- [ ] Optimize images (compress large files)
- [ ] Test contact form (if applicable)

### Regular Updates:

- [ ] Add new projects
- [ ] Update work experience
- [ ] Refresh skills section
- [ ] Update achievement counters
- [ ] Add new testimonials (if applicable)

## 🚀 Deployment

### GitHub Pages Setup:

1. Commit changes to GitHub
2. Go to repository Settings
3. Scroll to Pages section
4. Select source: "Deploy from a branch"
5. Select branch: "main"
6. Save settings

### Custom Domain (Optional):

1. Add `CNAME` file with your domain
2. Update DNS settings at your domain provider
3. Enable HTTPS in GitHub Pages settings

## 📞 Support

For technical assistance or advanced customizations:

- Create an issue in the GitHub repository
- Include screenshots of any problems
- Describe what you're trying to achieve

## 📚 Resources

### Learning Materials:

- **HTML/CSS Basics:** [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)
- **Bootstrap Documentation:** [Bootstrap 5.3](https://getbootstrap.com/docs/5.3/getting-started/introduction/)
- **AOS Animations:** [AOS Library](https://michalsnik.github.io/aos/)

### Tools:

- **Code Editor:** [Visual Studio Code](https://code.visualstudio.com/)
- **Image Optimization:** [TinyPNG](https://tinypng.com/)
- **Color Palette:** [Coolors.co](https://coolors.co/)

---

**Last Updated:** August 2025  
**Version:** 2.0  
**Maintainer:** Diki Rustian Portfolio
