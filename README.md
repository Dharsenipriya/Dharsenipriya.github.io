# Dharseni Priya - Professional Portfolio

A modern, responsive, and interactive portfolio website showcasing AI/ML expertise, digital marketing skills, and innovative projects.

## 🌟 Features

- **Modern Design**: Clean, professional layout with gradient backgrounds and smooth animations
- **Responsive**: Fully mobile-friendly with hamburger navigation
- **Dark/Light Mode**: Toggle between themes with persistent preference
- **Interactive Elements**: 
  - Animated skill progress bars
  - Project filtering by category
  - Smooth scrolling navigation
  - Contact form with validation
  - Email copy functionality
- **Performance Optimized**: Throttled scroll events and lazy loading
- **Accessibility**: Semantic HTML and keyboard navigation support

## 📁 File Structure

```
port/
├── index.html          # Main HTML structure
├── styles.css          # All CSS styles and animations
├── script.js           # JavaScript functionality
└── README.md           # This file
```

## 🚀 Quick Start

1. **Open the portfolio**: Simply open `index.html` in your web browser
2. **Local development**: Use a local server for best experience:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using PHP
   php -S localhost:8000
   ```

## 🎨 Customization Guide

### Personal Information
Update the following sections in `index.html`:

#### Hero Section
```html
<h1 class="hero-title">Your Name</h1>
<h2 class="hero-subtitle">Your Title</h2>
<p class="hero-description">Your tagline</p>
```

#### About Section
```html
<h3>Hello! I'm Your Name</h3>
<p>Your bio and background information</p>
```

#### Contact Information
```html
<p id="email-text">your.email@example.com</p>
<p>+1 234 567 8900</p>
<a href="your-linkedin-url">Your LinkedIn</a>
```

### Projects
Add or modify projects in the projects section:

```html
<div class="project-card" data-category="ai">
    <div class="project-image">
        <div class="project-placeholder">
            <i class="fas fa-project-icon"></i>
        </div>
    </div>
    <div class="project-content">
        <h3>Project Name</h3>
        <p>Project description</p>
        <div class="project-tech">
            <span>Technology 1</span>
            <span>Technology 2</span>
        </div>
        <div class="project-features">
            <ul>
                <li>Feature 1</li>
                <li>Feature 2</li>
            </ul>
        </div>
    </div>
</div>
```

### Skills
Update skill percentages in `index.html`:

```html
<div class="skill-item">
    <div class="skill-info">
        <span>Skill Name</span>
        <span>85%</span>
    </div>
    <div class="skill-bar">
        <div class="skill-progress" data-width="85"></div>
    </div>
</div>
```

### Experience
Modify the timeline items in the experience section:

```html
<div class="timeline-item">
    <div class="timeline-content">
        <div class="timeline-header">
            <h3>Job Title</h3>
            <span class="company">Company Name</span>
            <span class="duration">Duration</span>
        </div>
        <ul>
            <li>Responsibility 1</li>
            <li>Responsibility 2</li>
        </ul>
    </div>
</div>
```

## 🎨 Styling Customization

### Colors
Update the CSS custom properties in `styles.css`:

```css
:root {
    --primary-color: #667eea;      /* Main brand color */
    --secondary-color: #764ba2;    /* Secondary brand color */
    --accent-color: #f093fb;       /* Accent color */
    --text-primary: #2d3748;       /* Primary text color */
    --text-secondary: #718096;     /* Secondary text color */
    --bg-primary: #ffffff;         /* Primary background */
    --bg-secondary: #f7fafc;       /* Secondary background */
}
```

### Fonts
Change fonts by updating the Google Fonts link in `index.html`:

```html
<link href="https://fonts.googleapis.com/css2?family=YourFont:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

Then update the CSS variables:

```css
:root {
    --font-heading: 'YourFont', sans-serif;
    --font-body: 'YourFont', sans-serif;
}
```

### Animations
Modify animation durations and effects in `styles.css`:

```css
:root {
    --transition-fast: 0.3s ease;
    --transition-medium: 0.5s ease;
    --transition-slow: 0.8s ease;
}
```

## 📱 Adding Your Photo

1. Replace the placeholder icons with your actual photo:
   ```html
   <!-- Replace this -->
   <div class="profile-placeholder">
       <i class="fas fa-user"></i>
   </div>
   
   <!-- With this -->
   <div class="profile-image">
       <img src="path/to/your/photo.jpg" alt="Your Name">
   </div>
   ```

2. Add corresponding CSS:
   ```css
   .profile-image {
       width: 300px;
       height: 300px;
       border-radius: 50%;
       overflow: hidden;
       border: 3px solid rgba(255, 255, 255, 0.2);
   }
   
   .profile-image img {
       width: 100%;
       height: 100%;
       object-fit: cover;
   }
   ```

## 🔧 Advanced Customization

### Adding New Sections
1. Add the HTML structure in `index.html`
2. Add corresponding CSS in `styles.css`
3. Add any JavaScript functionality in `script.js`

### Custom Animations
Add new keyframe animations in `styles.css`:

```css
@keyframes yourAnimation {
    0% { /* initial state */ }
    100% { /* final state */ }
}

.your-element {
    animation: yourAnimation 1s ease-in-out;
}
```

### Form Integration
To connect the contact form to a backend service:

1. Update the form action in `index.html`:
   ```html
   <form id="contactForm" action="your-backend-url" method="POST">
   ```

2. Modify the form handling in `script.js`:
   ```javascript
   function handleContactForm(e) {
       e.preventDefault();
       
       const formData = new FormData(contactForm);
       
       fetch('your-backend-url', {
           method: 'POST',
           body: formData
       })
       .then(response => response.json())
       .then(data => {
           showNotification('Message sent successfully!', 'success');
           contactForm.reset();
       })
       .catch(error => {
           showNotification('Error sending message. Please try again.', 'error');
       });
   }
   ```

## 🌐 Deployment

### GitHub Pages
1. Push your code to a GitHub repository
2. Go to Settings > Pages
3. Select source branch (usually `main`)
4. Your site will be available at `https://username.github.io/repository-name`

### Netlify
1. Drag and drop the `port` folder to Netlify
2. Or connect your GitHub repository
3. Your site will be deployed automatically

### Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in the project directory
3. Follow the prompts

### Custom Domain
1. Purchase a domain from a registrar
2. Update DNS settings to point to your hosting provider
3. Configure your hosting provider to use the custom domain

## 📊 Performance Optimization

### Image Optimization
- Use WebP format for better compression
- Implement lazy loading for images
- Optimize image sizes for different screen resolutions

### Code Optimization
- Minify CSS and JavaScript for production
- Enable gzip compression on your server
- Use a CDN for external resources

## 🔍 SEO Optimization

### Meta Tags
Update meta tags in `index.html`:

```html
<meta name="description" content="Your professional description">
<meta name="keywords" content="your, keywords, here">
<meta name="author" content="Your Name">
<meta property="og:title" content="Your Name - Professional Title">
<meta property="og:description" content="Your description">
<meta property="og:image" content="path/to/your/image.jpg">
```

### Structured Data
Add JSON-LD structured data for better search engine understanding:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Your Name",
  "jobTitle": "Your Title",
  "url": "https://yourwebsite.com",
  "sameAs": [
    "https://linkedin.com/in/yourprofile",
    "https://github.com/yourusername"
  ]
}
</script>
```

## 🐛 Troubleshooting

### Common Issues

1. **Animations not working**: Ensure AOS library is loaded
2. **Mobile menu not working**: Check JavaScript console for errors
3. **Form not submitting**: Verify form action URL and backend setup
4. **Images not loading**: Check file paths and image formats

### Browser Compatibility
- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support
- Mobile browsers: Full support

## 📞 Support

For questions or issues:
- Check the browser console for JavaScript errors
- Verify all file paths are correct
- Ensure all external libraries are loading properly

## 📄 License

This portfolio template is free to use and modify for personal and commercial projects.

---

**Built with ❤️ using HTML, CSS, and JavaScript** 