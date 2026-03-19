# GitHub Dashboard - OpenClaw

A **vanilla HTML/CSS/JavaScript dashboard** that displays real-time statistics for the [openclaw/openclaw](https://github.com/openclaw/openclaw) GitHub repository.

## Features

✨ **Real-time Repository Stats**
- Stars count
- Forks count  
- Open issues count

💻 **Programming Languages**
- Detected languages with percentages
- Sorted by codebase volume

🔄 **Recent Commits**
- Last 5 commits from the main branch
- Author, timestamp, and commit hash
- Truncated commit messages for readability

## Tech Stack

- **Pure Vanilla JavaScript** — no dependencies, no build step
- **Responsive Design** — works on desktop, tablet, and mobile
- **GitHub Public API** — no authentication required
- **API Caching** — minimizes repeated calls
- **Modern UI** — gradient header, hover effects, smooth animations

## How to Use

1. **Open the file:**
   ```bash
   open github-dashboard.html
   # or in any modern web browser
   ```

2. **That's it!** The dashboard will automatically fetch data from GitHub's public API and display it.

## API Endpoints Used

The dashboard makes minimal API calls to GitHub (3 total):

```
GET https://api.github.com/repos/openclaw/openclaw
GET https://api.github.com/repos/openclaw/openclaw/languages
GET https://api.github.com/repos/openclaw/openclaw/commits?per_page=5
```

All endpoints are **public** — no GitHub authentication token required.

## Caching

API responses are cached in memory to prevent repeated calls during the session.

## Browser Compatibility

- Chrome/Chromium (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Customization

To monitor a different repository, edit the `API_BASE` variable in the script:

```javascript
const API_BASE = 'https://api.github.com/repos/YOUR_OWNER/YOUR_REPO';
```

## Performance

- **Load time:** <1 second (network dependent)
- **File size:** ~12 KB (minified HTML)
- **Dependencies:** 0

## License

MIT

---

**Created:** March 19, 2026  
**Repository:** [royam0820/github-dashboard.html](https://github.com/royam0820/github-dashboard.html)
