# Quick Start Guide

## 🚀 দ্রুত শুরু করুন

### ১. Website খুলুন

**Option A: সরাসরি Browser এ**
```bash
# portfolio_website folder এ যান এবং index.html file টি double-click করুন
```

**Option B: Local Server দিয়ে (Recommended)**
```bash
# Python দিয়ে
cd portfolio_website
python -m http.server 8000

# অথবা PHP দিয়ে
php -S localhost:8000

# অথবা VS Code এর Live Server extension ব্যবহার করুন
```

তারপর browser এ যান: `http://localhost:8000`

---

## ✏️ আপনার তথ্য দিয়ে Customize করুন

### ১. নাম ও Title পরিবর্তন করুন

`index.html` file খুলুন এবং খুঁজুন:

```html
<!-- Line 7 -->
<title>Shariful Islam | Full-Stack Web Developer</title>

<!-- Line 91 -->
<h1 class="sitename">Shariful Islam</h1>

<!-- Line 143 -->
<h2>Shariful Islam</h2>
```

এগুলো আপনার নাম দিয়ে replace করুন।

---

### ২. Social Media Links আপডেট করুন

`index.html` এ খুঁজুন (Line 95-107):

```html
<div class="social-links text-center">
  <a href="https://www.linkedin.com/in/your-profile/" class="linkedin" target="_blank">
    <i class="bi bi-linkedin"></i>
  </a>
  <a href="https://facebook.com/your-profile" class="facebook" target="_blank">
    <i class="bi bi-facebook"></i>
  </a>
  <!-- আরও social links... -->
</div>
```

আপনার profile links দিয়ে replace করুন।

---

### ৩. Profile Picture পরিবর্তন করুন

আপনার ছবি `assets/img/` folder এ রাখুন:

- `my-profile-img.jpg` - Header এর profile picture
- `me.jpg` - Hero section এর desktop image
- `me_mobile.jpg` - Hero section এর mobile image
- `me_about.jpg` - About section এর image

---

### ৪. About Section আপডেট করুন

`index.html` এ About section খুঁজুন (Line 155+):

```html
<section id="about" class="about section">
  <!-- আপনার bio, education, contact info এখানে -->
</section>
```

আপনার তথ্য দিয়ে replace করুন:
- Birthday
- Degree
- Phone
- Email
- City
- University
- LinkedIn
- GitHub

---

### ৫. Skills আপডেট করুন

Skills section এ আপনার skills add করুন। প্রতিটি skill এর জন্য:

```html
<div class="skill-pill">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React">
  <span>React</span>
</div>
```

DevIcon থেকে icons পাবেন: https://devicons.github.io/devicon/

---

### ৬. Projects আপডেট করুন

`assets/js/main.js` file এ খুঁজুন (Line 280+):

```javascript
const username = "YourGitHubUsername"; // আপনার GitHub username

const PROJECTS = [
  { name: "Project1", live: "https://project1-demo.com" },
  { name: "Project2", live: "https://project2-demo.com" },
  // আরও projects...
];
```

আপনার GitHub username এবং project names দিয়ে replace করুন।

**Project Thumbnails:**
- আপনার project এর screenshots `assets/project_thumbnail/` folder এ রাখুন
- File name: `project_name.jpg` (lowercase, underscore দিয়ে)

---

### ৭. Resume/CV আপডেট করুন

আপনার resume PDF file টি এখানে রাখুন:
```
assets/resume/resume.pdf
```

---

### ৮. Certifications যোগ করুন

Certificate files রাখুন:
```
assets/certifications/your-certificate.pdf
```

তারপর `index.html` এ Certifications section এ add করুন।

---

### ৯. Contact Form Setup করুন

`forms/contact.php` file এ আপনার email configure করুন:

```php
$receiving_email_address = 'your-email@example.com';
```

**Note:** Contact form কাজ করার জন্য PHP server প্রয়োজন।

---

## 🎨 Color Theme পরিবর্তন করুন

`assets/css/main.css` file এ CSS variables পরিবর্তন করুন:

```css
:root {
  --background-color: #0C0A09;      /* Background color */
  --default-color: #C9C9C9;         /* Text color */
  --heading-color: #F2F2F2;         /* Heading color */
  --accent-color: #22C55E;          /* Primary/Accent color */
  --surface-color: #131211;         /* Card background */
  --contrast-color: #ffffff;        /* White/Contrast */
}
```

আপনার পছন্দের colors দিয়ে replace করুন।

---

## 📱 Test করুন

### Desktop
- Chrome, Firefox, Safari, Edge এ test করুন

### Mobile
- Browser এর Developer Tools (F12) দিয়ে mobile view test করুন
- অথবা আপনার phone এ test করুন

### Dark/Light Mode
- Header এর theme toggle button click করে test করুন

---

## 🚀 Deploy করুন

### GitHub Pages
1. GitHub এ একটি repository তৈরি করুন
2. Portfolio files upload করুন
3. Settings > Pages > Source: main branch
4. আপনার site live হবে: `https://username.github.io/repo-name`

### Netlify
1. Netlify.com এ sign up করুন
2. "New site from Git" click করুন
3. আপনার repository connect করুন
4. Deploy!

### Vercel
1. Vercel.com এ sign up করুন
2. "Import Project" click করুন
3. আপনার repository select করুন
4. Deploy!

---

## ❓ সমস্যা হলে

### Images দেখা যাচ্ছে না
- File paths check করুন
- Image files সঠিক folder এ আছে কিনা দেখুন

### Contact Form কাজ করছে না
- PHP server চালু আছে কিনা check করুন
- `forms/contact.php` এ email সঠিকভাবে configure করা আছে কিনা দেখুন

### Projects দেখা যাচ্ছে না
- GitHub username সঠিক আছে কিনা check করুন
- Repository names সঠিক আছে কিনা দেখুন
- Browser console (F12) এ errors আছে কিনা দেখুন

---

## 📚 আরও সাহায্য

- Full documentation: `README.md` file দেখুন
- Template documentation: https://bootstrapmade.com/iportfolio-bootstrap-portfolio-websites-template/

---

**শুভকামনা! 🎉**

আপনার portfolio website তৈরি করার জন্য all the best!
