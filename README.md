# Academic Website - Setup Instructions

## 🚀 Quick Start

1. **Download all files** and create this folder structure:
```
your-repo/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
├── data/
│   ├── personal.json
│   ├── publications.json
│   ├── courses.json
│   └── projects.json
├── assets/
│   ├── images/
│   │   └── profile.jpg  ← ADD YOUR PHOTO HERE
│   └── docs/
│       └── (your PDFs here)
└── README.md
```

2. **Replace `assets/images/profile.jpg`** with your photo (recommended: 500x500px)

3. **Edit the JSON files** in the `data/` folder to customize your content

4. **Upload to GitHub** and enable GitHub Pages

---

## 📝 How to Customize Your Content

### 1. Personal Information (`data/personal.json`)

```json
{
  "name": "YOUR NAME HERE",
  "title": "YOUR TITLE HERE",
  "heroTitle": "YOUR HERO TITLE",
  "heroSubtitle": "YOUR SUBTITLE",
  "bio": [
    "YOUR FIRST BIO PARAGRAPH",
    "YOUR SECOND BIO PARAGRAPH"
  ]
}
```

**Most Important Fields to Update:**
- `name`: Your full name
- `title`: Your academic position
- `heroTitle` & `heroSubtitle`: Main page welcome message
- `bio`: Your biography (array of paragraphs)
- `education`: Your degrees
- `contact.email`: Your email address
- `socialLinks`: Update all URLs

### 2. Publications (`data/publications.json`)

Add your publications like this:
```json
{
  "title": "Your Paper Title",
  "authors": ["Your Name", "Co-author 1", "Co-author 2"],
  "venue": "Conference/Journal Name",
  "year": 2023,
  "featured": true,
  "links": [
    {
      "type": "PDF",
      "url": "assets/docs/your-paper.pdf"
    }
  ]
}
```

**Tips:**
- Set `"featured": true` for your most important papers
- Put your name exactly as it appears to get bold formatting
- Add PDFs to `assets/docs/` folder

### 3. Teaching (`data/courses.json`)

Add courses like this:
```json
{
  "courseCode": "CS 101",
  "title": "Course Title",
  "semester": "Fall 2023",
  "level": "Undergraduate",
  "description": "Course description...",
  "students": 45,
  "status": "current"
}
```

**Status options:**
- `"current"` - Currently teaching
- `"past"` - Previously taught

### 4. Projects (`data/projects.json`)

Add projects like this:
```json
{
  "title": "Project Name",
  "status": "active",
  "description": "Short description",
  "technologies": ["Python", "React", "etc"],
  "featured": true,
  "links": [
    {
      "type": "GitHub",
      "icon": "fab fa-github",
      "url": "https://github.com/your-repo"
    }
  ]
}
```

---

## 🎨 Easy Customization

### Change Colors
Edit `css/style.css` at the top:
```css
:root {
    --primary-color: #2c3e50;    /* Dark blue-gray */
    --secondary-color: #3498db;  /* Blue */
    --accent-color: #e74c3c;     /* Red */
}
```

### Add Your Photo
- Replace `assets/images/profile.jpg` with your photo
- Recommended size: 500x500px
- Will be automatically cropped to circle

---

## 📁 Adding Documents

### Research Papers
1. Add PDF files to `assets/docs/`
2. Reference them in `publications.json`:
```json
"links": [
  {
    "type": "PDF",
    "url": "assets/docs/your-paper.pdf"
  }
]
```

### Course Materials
1. Add syllabi to `assets/docs/`
2. Reference in `courses.json`:
```json
"materials": {
  "syllabus": "assets/docs/course-syllabus.pdf"
}
```

---

## 🚀 GitHub Pages Deployment

### Method 1: Direct Upload
1. Create repository named `your-username.github.io`
2. Upload all files maintaining folder structure
3. Go to Settings → Pages
4. Enable GitHub Pages from main branch
5. Site available at `https://your-username.github.io`

### Method 2: Subdirectory
1. Create any repository name
2. Upload files
3. Enable GitHub Pages
4. Site available at `https://your-username.github.io/repo-name`

---

## ✨ Features Included

- **📱 Fully Responsive** - Works on all devices
- **🔍 Search Functionality** - Press Ctrl+K to search
- **🎯 Smooth Animations** - Professional fade-in effects
- **⚡ Fast Loading** - Optimized performance
- **🎨 Modern Design** - Clean, academic styling
- **♿ Accessible** - Proper semantic HTML
- **📄 Print-Friendly** - Looks good when printed

---

## 🔧 Advanced Customization

### Enable Dark Mode
Uncomment these lines in `js/script.js`:
```javascript
// addThemeToggle(); // Uncomment to add theme toggle
// loadSavedTheme(); // Uncomment to enable theme persistence
```

### Add Google Analytics
Add this to `index.html` before `</head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-GA-ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR-GA-ID');
</script>
```

### Custom Domain
1. Add `CNAME` file to repository root
2. Add your domain name inside
3. Configure DNS settings with your domain provider

---

## 🐛 Troubleshooting

### Website Not Loading Content
- Check that all JSON files are in `data/` folder
- Ensure JSON syntax is valid (use JSONLint.com)
- Check browser console for errors

### Images Not Showing
- Ensure `assets/images/profile.jpg` exists
- Check file path capitalization
- Ensure image file is not too large (< 2MB recommended)

### GitHub Pages Not Working
- Ensure repository is public
- Check Settings → Pages is enabled
- Wait 5-10 minutes for deployment

---

## 💡 Content Tips

### Writing Your Bio
- Keep it professional but approachable
- Highlight your main research areas
- Mention key achievements
- Include current position and institution

### Organizing Publications
- List most recent/important first
- Use consistent author name format
- Include DOI or paper links when possible
- Mark your best papers as `"featured": true`

### Project Descriptions
- Start with what the project does
- Mention technologies used
- Include links to demos/code
- Note funding sources if applicable

---

## 📧 Support

If you need help:
1. Check this README first
2. Validate your JSON files at jsonlint.com
3. Check browser console for error messages
4. Ensure all files are in the correct folders

---

**🎉 Your academic website is ready to go! Just edit the JSON files and upload to GitHub.**