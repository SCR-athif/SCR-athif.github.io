# Mohammed Athif — Cybersecurity Portfolio

> A premium, fully animated cybersecurity portfolio built with pure HTML, CSS, and JavaScript — no framework dependencies needed for deployment.

## 🚀 Quick Deploy (3 ways)

### Option 1: GitHub Pages (Free, Instant)
```bash
# 1. Create a new GitHub repo named: yourusername.github.io
# 2. Upload index.html to the root
# 3. Go to Settings → Pages → Source: main branch
# Your site will be live at: https://yourusername.github.io
```

### Option 2: Vercel (Recommended — CDN, Fast)
```bash
npm install -g vercel
vercel --prod
# Follow prompts → your site is live in 30 seconds
```

### Option 3: Netlify (Drag & Drop)
1. Go to https://netlify.com
2. Drag the `athif-portfolio/` folder onto the deploy zone
3. Done — live URL in seconds

---

## ✏️ Customization Guide

### 1. Update Your Info
Search for these strings in `index.html` and replace:

| Find | Replace With |
|------|-------------|
| `Mohammed Athif` | Your name |
| `athif@secresearch.io` | Your email |
| `SCR-athif` | Your GitHub username |
| `keybase.io/athif` | Your keybase profile |

### 2. Update Stats (Hero Section)
Find `data-target="87"` etc. and change the numbers:
```html
<div class="stat-num" data-target="87">0</div>  <!-- Vulnerabilities Found -->
<div class="stat-num" data-target="12">0</div>  <!-- CVEs Published -->
<div class="stat-num" data-target="34">0</div>  <!-- Programs Tested -->
<div class="stat-num" data-target="5">0</div>   <!-- Hall of Fames -->
```

### 3. GitHub CVE Integration
The site auto-fetches CVEs from your GitHub repo. To enable:
1. Create a public GitHub repo named `CVE` under your account
2. Add files named like `CVE-2024-XXXXX.md` with descriptions
3. The site automatically pulls and displays them

For private repos, add a GitHub token:
```javascript
// In the fetchCVEs() function, add:
headers: { 
  'Accept': 'application/vnd.github.v3+json',
  'Authorization': 'token YOUR_GITHUB_TOKEN'
}
```

### 4. Update Severity Charts
Find the Chart.js data in the script section:
```javascript
data: [23,31,24,7,2]  // Critical, High, Medium, Low, Info counts
```

### 5. Add Resume Download
Replace the `#` in the download button with your PDF link:
```html
<a href="resume.pdf" class="btn btn-outline" download>⬇ DOWNLOAD RESUME</a>
```
Place `resume.pdf` in the same folder as `index.html`.

### 6. Update Projects
Each project card follows this pattern:
```html
<div class="glass-card project-card fade-in tilt">
  <div class="project-icon">🔓 <span>CVE PoC</span></div>
  <div class="project-title">Your Project Title</div>
  <div class="project-desc">Your description...</div>
  <div class="project-tags">
    <span class="chip chip-red">TAG</span>
  </div>
  <div class="project-links">
    <a href="YOUR_GITHUB_URL" class="project-link">→ GitHub</a>
  </div>
</div>
```

---

## 🎨 Color Customization

Change the primary accent color (currently cyan):
```css
:root {
  --cyan: #00f5ff;        /* Main accent */
  --cyan-dim: #00c4d4;    /* Muted accent */
  --cyan-glow: rgba(0,245,255,0.35);  /* Glow effect */
  --red: #ff2244;         /* Danger/critical */
  --green: #00ff88;       /* Success/low severity */
  --amber: #ffb800;       /* Warning/medium */
}
```

---

## 📦 Features Included

- ✅ Custom animated cursor
- ✅ Cyberpunk preloader with text animation
- ✅ Animated particle network background
- ✅ Hero section with typewriter effect
- ✅ Animated stat counters
- ✅ 3D tilt effect on cards
- ✅ Glassmorphism UI throughout
- ✅ Skill bars with scroll animation
- ✅ Bug bounty platforms showcase
- ✅ Chart.js severity + type charts
- ✅ GitHub API CVE integration with fallback data
- ✅ CVE search + filter by severity
- ✅ 6 project cards with tags
- ✅ 6 blog writeup cards
- ✅ Impact dashboard with animated counters
- ✅ Achievement timeline
- ✅ Experience timeline
- ✅ Interactive terminal (whoami, show skills, list cves, etc.)
- ✅ Contact form with animation
- ✅ Social links section
- ✅ Dark/Light theme toggle
- ✅ Scan lines overlay effect
- ✅ Fully responsive (mobile, tablet, desktop)
- ✅ Smooth scroll animations
- ✅ Glitch text effect on preloader

---

## 🔧 Tech Stack

- **HTML5 + CSS3** — No build step required
- **Vanilla JavaScript** — Zero dependencies
- **Chart.js** — Loaded from CDN
- **Google Fonts** — Orbitron + Rajdhani + Share Tech Mono
- **GitHub REST API** — Dynamic CVE fetching

---

## 📱 Browser Support

Chrome 90+ · Firefox 88+ · Safari 14+ · Edge 90+

---

Built with ❤️ for the security community.
