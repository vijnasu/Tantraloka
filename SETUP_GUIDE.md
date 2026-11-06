# 🔱 Tantraloka Web Setup Guide

## Project Overview
**Tantraloka** is a digital repository of **Abhinavagupta's** famous Sanskrit philosophical text on Kashmir Shaivism, now available with Kannada translations, transliterations, and detailed commentaries.

- **Original Text**: Sanskrit (Devanagari script)
- **Translations**: Kannada with Kannada script
- **Language**: Kannada, Sanskrit
- **Repository**: [vijnasu/Tantraloka](https://github.com/vijnasu/Tantraloka)

---

## ✅ Extraction Complete

The ZIP file `Tantraloka_Project_75_Files (1).zip` has been successfully extracted with:
- **37 Chapters** (Ahniks) with 5,000+ stanzas
- Complete markdown source files
- Jekyll static site generator configuration
- Styling and assets for Kannada typography

### Extracted Files:
```
/workspaces/Tantraloka/
├── chapters/           # 37 directories with chapter content
├── assets/            # CSS, fonts, and styling
├── _layouts/          # Jekyll HTML templates
├── _site/             # Generated static HTML (build output)
├── _config.yml        # Jekyll configuration
├── index.md          # Home page content
├── introduction.md    # Introduction to the text
├── README.md         # Project readme
└── CONTRIBUTING.md   # Contribution guidelines
```

---

## 🏗️ Web Page Setup

### 1. **Jekyll Build System**
The site uses **Jekyll** (Ruby static site generator) to convert Markdown files to HTML.

**Build Status**: ✅ **Successfully Built**

```bash
# Build command used:
jekyll build

# Output directory: _site/
# Size: 540 KB
```

### 2. **Web Server**
A Python HTTP server is now running to serve the site:

```
🌐 Server: http://localhost:8000
📂 Base URL: /Tantraloka/
```

**Access the site**:
- **Home**: http://localhost:8000/Tantraloka/
- **GitHub Pages URL**: https://vijnasu.github.io/Tantraloka/

### 3. **Site Features**

#### Homepage Features:
✅ Multilingual support (Kannada + Sanskrit)  
✅ Chapter library with search functionality  
✅ Responsive design for all devices  
✅ Accessible navigation (Skip links, ARIA labels)  
✅ Search box for finding stanzas/chapters  

#### Chapter Structure:
- 37 chapters (Ahniks) organized by number
- Stanzas split into manageable sections
- Direct links to each chapter/section
- Status indicators (✅ = Translated, ⏳ = Pending)

---

## 📊 Content Statistics

| Metric | Count |
|--------|-------|
| Chapters | 37 |
| Total Stanzas | 5,000+ |
| Translated Sections | 2+ (expanding) |
| Chapter Directories | 39 |
| Main Pages | 3 (index, introduction, chapters) |

---

## 🔧 Configuration Details

### Jekyll Configuration (_config.yml)
```yaml
title: ತಂತ್ರಾಲೋಕ
description: Abhinavagupta's Tantraloka with Kannada commentary
lang: kn
url: https://vijnasu.github.io
baseurl: /Tantraloka
markdown: kramdown
plugins:
  - jekyll-relative-links
```

### Key Settings:
- **Language**: Kannada (kn)
- **Markdown Parser**: Kramdown
- **Relative Links**: Enabled (works offline too)
- **Base URL**: `/Tantraloka` (for GitHub Pages)

---

## 📁 Directory Structure

### Chapters Organization
```
chapters/
├── chapter-01/    [332 stanzas across 3 files]
├── chapter-02/    [50 stanzas]
├── chapter-03/    [294 stanzas across 2 files]
├── chapter-04/    [279 stanzas across 2 files]
├── chapter-05/    [159 stanzas]
├── ... (chapter-06 through chapter-37)
└── chapter-37/    [85 stanzas]
```

### Large Chapters (subdivided):
- **Chapter 1**: 3 files (1-150, 151-300, 301-332)
- **Chapter 8**: 3 files (1-161, 162-302, 303-452)
- **Chapter 15**: 4 files (1-159, 160-307, 308-453, 454-615)
- **Chapter 28**: 3 files (1-150, 151-302, 303-434)
- **Chapter 29**: 2 files (1-150, 151-291)

---

## 🌐 Running the Web Server

### Current Status
✅ Server is running on port 8000

### Start/Stop Commands
```bash
# Start the server (background)
cd /workspaces/Tantraloka/_site
python3 -m http.server 8000 > /tmp/server.log 2>&1 &

# Check if running
lsof -i :8000

# Stop the server
kill <PID>

# View logs
tail -f /tmp/server.log
```

### Access Points
- **Local**: http://localhost:8000/Tantraloka/
- **Home Page**: Shows all 57 chapter entries with status
- **Search**: Use the search box to find stanzas by number or content
- **Chapter Links**: Click any chapter to view its stanzas

---

## 🎨 Site Features & Navigation

### Header
- Logo: Kannada "ತ" (Ta) 
- Site Title: "ತಂತ್ರಾಲೋಕ" (Tantraloka)
- Main Navigation: Links to home and chapters

### Main Page
1. **Intro Section**: Brief description of the text
2. **Library Section**: Searchable chapter list
3. **Chapter Grid**: Organized by translation status
   - ✅ = Completed translation
   - ⏳ = Pending translation

### Search Functionality
- Real-time search of chapter/stanza numbers
- Filters results as you type
- Helps locate specific content quickly

### Accessibility
- Skip-to-content link
- ARIA labels for screen readers
- Semantic HTML structure
- Keyboard-navigable interface

---

## 🚀 Future Enhancements

### Planned Features:
1. Full Kannada translations for all chapters
2. Parallel Sanskrit text display
3. Audio narration of stanzas
4. Commentary layer with expandable explanations
5. Full-text search across all content
6. Dark mode support
7. Bookmarking system
8. Mobile app version

### Current Translation Status
- **Chapter 1**: ✅ Partially translated (1-150 complete)
- **Other Chapters**: ⏳ Source text provided, translation pending

---

## 📝 Content Format

Each chapter file follows this structure:
```markdown
# ಶ್ಲೋಕ 1-50 (Stanzas 1-50)

## ಶ್ಲೋಕ 1 (Stanza 1)
**Sanskrit (Devanagari)**
Sanskrit text here...

**ಕನ್ನಡ ಅರ್ಥ (Kannada Translation)**
Kannada meaning here...

**ವಿವರಣೆ (Commentary)**
Detailed explanation...

---
## ಶ್ಲೋಕ 2 (Stanza 2)
[Similar structure continues...]
```

---

## 🔗 Important Links

- **GitHub Repository**: https://github.com/vijnasu/Tantraloka
- **Live Website**: https://vijnasu.github.io/Tantraloka/
- **Contributing**: See [CONTRIBUTING.md](CONTRIBUTING.md)
- **README**: See [README.md](README.md)

---

## 💡 How to Contribute

1. Clone the repository
2. Add translations to chapter files
3. Follow the content format (Sanskrit → Kannada → Commentary)
4. Create a pull request with your changes
5. Ensure build passes with `jekyll build`

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

---

## 🛠️ Technical Stack

- **Static Site Generator**: Jekyll (Ruby)
- **Markup Language**: Markdown (Kramdown flavor)
- **Styling**: CSS (custom for Kannada typography)
- **Hosting**: GitHub Pages
- **Version Control**: Git
- **Accessibility**: WCAG 2.1 Level AA

---

## 📞 Support

For issues, questions, or contributions:
1. Open an issue on [GitHub](https://github.com/vijnasu/Tantraloka/issues)
2. Review [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines
3. Check the README for context

---

**Last Updated**: 2026-11-05  
**Build Status**: ✅ Success  
**Pages Generated**: 1 (index.html)  
**Total Size**: 540 KB  

---

🙏 *Tantraloka - Making classical wisdom accessible to the digital age*
