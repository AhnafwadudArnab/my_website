# Portfolio Website

এটি একটি modern, responsive portfolio website যা MyPortfolio-main এর UI design অনুসরণ করে তৈরি করা হয়েছে।

## Features

- ✨ Modern & Clean Design
- 📱 Fully Responsive (Mobile, Tablet, Desktop)
- 🎨 Dark/Light Mode Toggle
- 🚀 Fast Loading with Optimized Assets
- 💼 Professional Portfolio Sections:
  - Hero Section with Animated Profile
  - About Section
  - Certifications & Achievements
  - Skills Section
  - Resume/Timeline
  - Projects Gallery with GitHub Integration
  - Services Section
  - Contact Form

## Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript
- **CSS Framework**: Bootstrap 5.3.3
- **Icons**: Bootstrap Icons
- **Animations**: AOS (Animate On Scroll)
- **Lightbox**: GLightbox
- **Slider**: Swiper
- **Typing Effect**: Typed.js
- **Scroll Animations**: Waypoints

## How to Use

1. **Open the website**: 
   - Simply open `index.html` in your browser
   - Or use a local server (recommended)

2. **Customize Content**:
   - Edit `index.html` to update your personal information
   - Replace images in `assets/img/` folder
   - Update certifications in `assets/certifications/`
   - Modify project thumbnails in `assets/project_thumbnail/`

3. **Customize Styling**:
   - Main styles are in `assets/css/main.css`
   - Color scheme can be changed in CSS variables

4. **Update JavaScript**:
   - Main functionality in `assets/js/main.js`
   - GitHub projects integration included

## Folder Structure

```
portfolio_website/
├── assets/
│   ├── certifications/     # Certificate PDFs and images
│   ├── css/               # Stylesheets
│   ├── img/               # Images (profile, hero, etc.)
│   ├── js/                # JavaScript files
│   ├── project_thumbnail/ # Project preview images
│   ├── resume/            # Resume PDF
│   ├── scss/              # SCSS source files
│   └── vendor/            # Third-party libraries
├── forms/
│   └── contact.php        # Contact form handler
├── index.html             # Main HTML file
└── README.md              # This file
```

## Customization Guide

### 1. Personal Information
Edit the following sections in `index.html`:
- Name and title in `<header>` section
- Social media links
- About section content
- Contact information

### 2. Colors & Theme
Modify CSS variables in `assets/css/main.css`:
```css
:root {
  --background-color: #0C0A09;
  --default-color: #C9C9C9;
  --heading-color: #F2F2F2;
  --accent-color: #22C55E;
  --surface-color: #131211;
  --contrast-color: #ffffff;
}
```

### 3. Projects
Update the GitHub username and project list in `assets/js/main.js`:
```javascript
const username = "YourGitHubUsername";
const PROJECTS = [
  { name: "Project1", live: "https://project1.com" },
  // Add more projects
];
```

## Contact Form Setup

The contact form requires PHP backend. Update `forms/contact.php` with your email configuration.

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This template is based on iPortfolio by BootstrapMade.
- Template URL: https://bootstrapmade.com/iportfolio-bootstrap-portfolio-websites-template/
- License: https://bootstrapmade.com/license/

## Credits

- Template: BootstrapMade
- Icons: Bootstrap Icons
- Fonts: Google Fonts (DM Sans, Montserrat, Plus Jakarta Sans)

---

Made with ❤️ for developers
