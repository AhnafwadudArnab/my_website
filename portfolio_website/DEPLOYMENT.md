# Deployment Guide

এই portfolio website টি বিভিন্ন platform এ deploy করার guide।

---

## 🌐 GitHub Pages (Free)

### Prerequisites
- GitHub account
- Git installed

### Steps

1. **GitHub Repository তৈরি করুন**
```bash
# Terminal/Command Prompt এ
cd portfolio_website
git init
git add .
git commit -m "Initial commit: Portfolio website"
```

2. **GitHub এ Repository তৈরি করুন**
- GitHub.com এ যান
- "New repository" click করুন
- Repository name দিন (e.g., `my-portfolio`)
- Public select করুন
- "Create repository" click করুন

3. **Code Push করুন**
```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git branch -M main
git push -u origin main
```

4. **GitHub Pages Enable করুন**
- Repository > Settings > Pages
- Source: Deploy from a branch
- Branch: main / (root)
- Save

5. **Live URL**
আপনার site live হবে: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME`

---

## 🚀 Netlify (Free)

### Method 1: Drag & Drop

1. [Netlify.com](https://netlify.com) এ যান
2. Sign up করুন (GitHub দিয়ে)
3. "Sites" > "Add new site" > "Deploy manually"
4. `portfolio_website` folder টি drag & drop করুন
5. Deploy complete!

### Method 2: Git Integration

1. GitHub এ code push করুন (উপরের steps দেখুন)
2. Netlify > "Add new site" > "Import an existing project"
3. GitHub connect করুন
4. Repository select করুন
5. Deploy settings:
   - Build command: (leave empty)
   - Publish directory: `/`
6. "Deploy site" click করুন

### Custom Domain Setup
- Site settings > Domain management
- "Add custom domain" click করুন
- আপনার domain name দিন
- DNS settings configure করুন

---

## ⚡ Vercel (Free)

### Steps

1. [Vercel.com](https://vercel.com) এ যান
2. Sign up করুন (GitHub দিয়ে)
3. "Add New" > "Project"
4. GitHub repository import করুন
5. Deploy settings:
   - Framework Preset: Other
   - Build Command: (leave empty)
   - Output Directory: (leave empty)
6. "Deploy" click করুন

### Custom Domain
- Project Settings > Domains
- "Add" click করুন
- আপনার domain দিন

---

## 🔥 Firebase Hosting (Free)

### Prerequisites
```bash
npm install -g firebase-tools
```

### Steps

1. **Firebase Login**
```bash
firebase login
```

2. **Initialize Firebase**
```bash
cd portfolio_website
firebase init hosting
```

Settings:
- Use existing project or create new
- Public directory: `.` (current directory)
- Single-page app: No
- Overwrite index.html: No

3. **Deploy**
```bash
firebase deploy
```

4. **Live URL**
আপনার site: `https://YOUR_PROJECT_ID.web.app`

---

## 🐳 Docker (Advanced)

### Dockerfile তৈরি করুন

```dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

### Build & Run

```bash
# Build image
docker build -t my-portfolio .

# Run container
docker run -d -p 8080:80 my-portfolio
```

Visit: `http://localhost:8080`

---

## 📦 Traditional Web Hosting

### cPanel Hosting

1. **Files Upload করুন**
   - cPanel > File Manager
   - `public_html` folder এ যান
   - Upload all files from `portfolio_website`

2. **Permissions Check করুন**
   - Files: 644
   - Folders: 755

3. **Contact Form Setup**
   - PHP version check করুন (7.4+)
   - `forms/contact.php` configure করুন

### FTP Upload

```bash
# FileZilla বা অন্য FTP client ব্যবহার করুন
Host: ftp.yourdomain.com
Username: your_username
Password: your_password
Port: 21

# Upload all files to public_html or www folder
```

---

## ✅ Post-Deployment Checklist

### 1. Test করুন
- [ ] Homepage load হচ্ছে
- [ ] All images দেখা যাচ্ছে
- [ ] Navigation links কাজ করছে
- [ ] Contact form submit হচ্ছে
- [ ] Mobile responsive
- [ ] Dark/Light mode toggle

### 2. SEO Setup
- [ ] Meta tags check করুন
- [ ] Open Graph tags add করুন
- [ ] Sitemap.xml তৈরি করুন
- [ ] Google Search Console এ submit করুন

### 3. Performance
- [ ] Images optimize করুন
- [ ] Lighthouse score check করুন
- [ ] Loading speed test করুন

### 4. Analytics (Optional)
- [ ] Google Analytics setup করুন
- [ ] Facebook Pixel add করুন

---

## 🔧 Troubleshooting

### Images দেখা যাচ্ছে না
```
Solution: 
- File paths check করুন (case-sensitive)
- Images সঠিক folder এ আছে কিনা verify করুন
```

### Contact Form কাজ করছে না
```
Solution:
- PHP enabled আছে কিনা check করুন
- Email configuration verify করুন
- Server logs check করুন
```

### CSS/JS load হচ্ছে না
```
Solution:
- File paths সঠিক আছে কিনা check করুন
- Browser cache clear করুন
- CDN links working কিনা verify করুন
```

---

## 📊 Performance Optimization

### Images
```bash
# ImageOptim, TinyPNG, বা Squoosh ব্যবহার করুন
# Target: < 200KB per image
```

### Minify CSS/JS
```bash
# Online tools:
# - cssminifier.com
# - javascript-minifier.com
```

### Enable Caching
```apache
# .htaccess file এ add করুন
<IfModule mod_expires.c>
  ExpiresActive On
  ExpiresByType image/jpg "access plus 1 year"
  ExpiresByType image/jpeg "access plus 1 year"
  ExpiresByType image/png "access plus 1 year"
  ExpiresByType text/css "access plus 1 month"
  ExpiresByType application/javascript "access plus 1 month"
</IfModule>
```

---

## 🔒 Security Tips

1. **HTTPS Enable করুন**
   - Let's Encrypt free SSL certificate
   - Cloudflare SSL

2. **Contact Form Protection**
   - reCAPTCHA add করুন
   - Rate limiting implement করুন

3. **Headers Security**
```apache
# .htaccess
Header set X-Content-Type-Options "nosniff"
Header set X-Frame-Options "SAMEORIGIN"
Header set X-XSS-Protection "1; mode=block"
```

---

## 📱 Custom Domain Setup

### Namecheap/GoDaddy

1. **DNS Settings**
```
Type: A Record
Host: @
Value: [Your hosting IP]

Type: CNAME
Host: www
Value: yourdomain.com
```

2. **Wait for Propagation**
- Usually 24-48 hours
- Check: https://dnschecker.org

---

## 🎉 Success!

আপনার portfolio এখন live! 🚀

Share করুন:
- LinkedIn
- Twitter
- Facebook
- Resume/CV তে link add করুন

---

**Need Help?**
- GitHub Issues: Create an issue
- Email: your-email@example.com
