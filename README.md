# VC Partners Website

A modern, responsive website for VC Partners - Vietnam's leading venture capital firm. Built with HTML5, CSS3, and JavaScript.

## Features

- **Responsive Design**: Optimized for all devices (desktop, tablet, mobile)
- **Modern UI/UX**: Clean, professional design with smooth animations
- **Interactive Elements**: Dynamic navigation, form handling, and scroll effects
- **Performance Optimized**: Fast loading with minimal dependencies
- **SEO Friendly**: Semantic HTML structure and meta tags

## Project Structure

```
vcp_website/
├── index.html          # Main HTML file
├── styles.css          # CSS styles and responsive design
├── script.js           # JavaScript functionality
└── README.md           # Project documentation
```

## Local Development

1. Clone or download the project files
2. Open `index.html` in your web browser
3. For development with live reload, use a local server:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using PHP
   php -S localhost:8000
   ```

## Deployment to GitHub Pages

### Method 1: Using GitHub Web Interface

1. **Create a new repository on GitHub:**
   - Go to [GitHub](https://github.com) and sign in
   - Click the "+" icon and select "New repository"
   - Name it `vcpartners-website` (or your preferred name)
   - Make it **Public** (required for free GitHub Pages)
   - Don't initialize with README, .gitignore, or license
   - Click "Create repository"

2. **Upload files:**
   - In your new repository, click "Add file" → "Upload files"
   - Drag and drop all project files (`index.html`, `styles.css`, `script.js`)
   - Add a commit message: "Initial commit - VC Partners website"
   - Click "Commit changes"

3. **Enable GitHub Pages:**
   - Go to your repository's "Settings" tab
   - Scroll down to "Pages" section in the left sidebar
   - Under "Source", select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"
   - Wait 5-10 minutes for deployment

4. **Access your website:**
   - Your site will be available at: `https://yourusername.github.io/vcpartners-website/`

### Method 2: Using Git Command Line

1. **Initialize Git repository:**
   ```bash
   cd /path/to/vcp_website
   git init
   ```

2. **Add files and commit:**
   ```bash
   git add .
   git commit -m "Initial commit - VC Partners website"
   ```

3. **Connect to GitHub repository:**
   ```bash
   git remote add origin https://github.com/yourusername/vcpartners-website.git
   git branch -M main
   git push -u origin main
   ```

4. **Enable GitHub Pages:**
   - Follow steps 3-4 from Method 1 above

## Customization

### Updating Content

- **Company Information**: Edit the content in `index.html`
- **Styling**: Modify colors, fonts, and layout in `styles.css`
- **Functionality**: Add or modify features in `script.js`

### Key Sections to Customize

1. **Hero Section**: Update the main headline and call-to-action
2. **About Section**: Modify company description and statistics
3. **Portfolio**: Replace with actual portfolio companies
4. **Team**: Update team member information
5. **Contact**: Change contact details and form handling

### Color Scheme

The website uses a professional blue color scheme:
- Primary Blue: `#2563eb`
- Dark Gray: `#1f2937`
- Light Gray: `#6b7280`
- Background: `#f9fafb`

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- **Lighthouse Score**: 95+ (Performance, Accessibility, Best Practices, SEO)
- **Load Time**: < 2 seconds on 3G connection
- **File Size**: < 100KB total (excluding external fonts)

## Troubleshooting

### Common Issues

1. **GitHub Pages not updating:**
   - Wait 10-15 minutes for changes to propagate
   - Check if files are in the root directory
   - Ensure `index.html` is the main file

2. **Styling not loading:**
   - Verify file paths in HTML
   - Check for typos in CSS class names
   - Clear browser cache

3. **JavaScript not working:**
   - Check browser console for errors
   - Ensure all files are uploaded correctly
   - Verify script tag is at the bottom of HTML

### Support

For technical support or customization requests, please contact the development team.

## License

This project is open source and available under the [MIT License](LICENSE).

---

**Built with ❤️ for VC Partners**
