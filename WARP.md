# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

This is a static website for VC Partners - Vietnam's leading venture capital firm. The project is built with vanilla HTML5, CSS3, and JavaScript, focusing on performance, responsive design, and professional presentation.

**Key Characteristics:**
- Static website with no build process or dependencies
- Responsive design optimized for all devices
- Modern CSS with animations and interactive elements
- Professional business website with sections: Hero, About, Services, Team, Track Record, ESG, Contact
- Performance-optimized with minimal external dependencies

## Development Commands

### Local Development
```bash
# Start local development server (Python)
python -m http.server 8000

# Alternative: Node.js serve
npx serve .

# Alternative: PHP
php -S localhost:8000
```

### Testing & Validation
```bash
# Test local server access
curl -I http://localhost:8000

# Validate HTML (manual - use W3C Markup Validator online)
# https://validator.w3.org/

# Check for broken links (if linkchecker is installed)
linkchecker http://localhost:8000
```

### Git Operations
```bash
# Check current status
git status

# Add all changes
git add .

# Commit with descriptive message
git commit -m "Update: [describe changes]"

# Push to main branch
git push origin main
```

### Deployment to GitHub Pages
```bash
# Initial setup (if not done)
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git branch -M main
git push -u origin main

# Enable GitHub Pages in repository Settings > Pages
# Source: Deploy from a branch > main > / (root)
```

## Project Architecture

### File Structure
```
vcp_website/
├── index.html          # Main HTML file with all content
├── styles.css          # Complete CSS with responsive design
├── script.js           # JavaScript for interactivity
├── vcp-logo.png       # Company logo
├── background.png     # Hero section background
├── image-*.png        # Team member photos
├── README.md          # Project documentation
├── DEPLOYMENT_GUIDE.md # GitHub Pages deployment guide
└── .gitignore         # Git ignore rules
```

### Core Technologies
- **HTML5**: Semantic structure with accessibility in mind
- **CSS3**: Modern styling with Flexbox, Grid, and animations
- **JavaScript**: Vanilla JS for navigation, form handling, and interactions
- **External**: Google Fonts (Inter), Font Awesome icons

### Key Components

**Navigation System:**
- Fixed navbar with smooth scrolling
- Mobile hamburger menu
- Active link highlighting based on scroll position

**Interactive Elements:**
- Mobile-responsive navigation toggle
- Smooth scroll animations
- Form validation and submission handling
- Intersection Observer for scroll animations
- Counter animations for statistics
- Hover effects on portfolio items and team members

**Responsive Design:**
- Mobile-first approach
- Breakpoints for tablet and desktop
- Flexible grid layouts
- Optimized typography scaling

### CSS Architecture
- Reset/base styles first
- Component-based organization
- Responsive design with media queries
- CSS custom properties for consistent theming
- Performance-optimized animations

### JavaScript Features
- Modern ES6+ syntax
- Event delegation patterns
- Intersection Observer API for performance
- Form handling with validation
- Smooth scrolling navigation
- Mobile menu toggle functionality

## Content Management

### Updating Company Information
- **Hero Section**: Edit title and subtitle in `index.html`
- **About Section**: Update company description and competitive advantages
- **Services**: Modify service offerings and descriptions  
- **Team**: Update team member information and photos
- **Track Record**: Add/modify project details and performance metrics
- **Contact**: Update contact information and form handling

### Image Assets
- **Logo**: `vcp-logo.png` (50px height recommended)
- **Background**: `background.png` (hero section)
- **Team Photos**: High-quality professional headshots
- **Optimization**: Compress images for web performance

### Styling Updates
- **Colors**: Primary blue (#1e3a8a), accent red (#dc2626)
- **Typography**: Inter font family from Google Fonts
- **Responsive**: Mobile-first breakpoints at 768px, 1024px
- **Animations**: CSS transitions and JavaScript-driven counters

## Deployment & Hosting

**Primary Deployment:** GitHub Pages
- Automatic deployment from main branch
- Custom domain support available
- HTTPS enabled by default
- Global CDN distribution

**Alternative Hosting Options:**
- Netlify (drag & drop or Git integration)
- Vercel (Git integration)  
- Any static hosting service

**Performance Considerations:**
- Lighthouse score target: 95+
- Load time target: < 2 seconds on 3G
- Total file size: < 100KB (excluding images)

## Browser Compatibility

**Supported Browsers:**
- Chrome (latest)
- Firefox (latest) 
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

**Progressive Enhancement:**
- Core functionality works without JavaScript
- CSS Grid with Flexbox fallbacks
- Modern features with appropriate fallbacks

## Security & Best Practices

**Static Site Security:**
- No server-side processing
- HTTPS enforced via GitHub Pages
- No sensitive data in repository
- Form submissions require external service integration

**Performance Optimization:**
- Minimal external dependencies
- Optimized images and assets
- Efficient CSS and JavaScript
- Modern web standards compliance

## Common Tasks

**Content Updates:**
1. Edit `index.html` for text changes
2. Update `styles.css` for visual changes
3. Test locally with development server
4. Commit and push to deploy

**Adding New Sections:**
1. Add HTML structure in `index.html`
2. Add navigation link in navbar
3. Implement styles in `styles.css`
4. Add JavaScript interactions if needed

**Image Updates:**
1. Optimize images for web (WebP/PNG/JPG)
2. Update file references in HTML/CSS
3. Ensure responsive behavior
4. Test across devices
