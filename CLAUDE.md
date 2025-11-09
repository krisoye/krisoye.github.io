# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a GitHub Pages repository hosted at `krisoye.github.io`. The repository serves static web content directly from the main branch.

## Key Commands

### Local Development
- **Start local server**: `python -m http.server 8000` or `python3 -m http.server 8000`
  - Access at: http://localhost:8000
- **Alternative with live reload** (if using Node.js): `npx live-server`

### Deployment
- **Deploy**: Push to the `main` branch
  - Changes are automatically published to https://krisoye.github.io
  - Allow 1-2 minutes for GitHub Pages to rebuild after push

### Git Operations
- **Check status**: `git status`
- **Stage changes**: `git add .`
- **Commit**: `git commit -m "message"`
- **Push to GitHub Pages**: `git push origin main`

## Architecture

### GitHub Pages Configuration
- **Hosting**: Static files served directly from the `main` branch root
- **Custom domain**: Can be configured via CNAME file in repository root
- **Supported formats**: HTML, CSS, JavaScript, and Jekyll (optional)

### File Structure Conventions
- `index.html` - Main entry point served at root URL
- Static assets typically organized in:
  - `/css/` - Stylesheets
  - `/js/` - JavaScript files
  - `/images/` or `/assets/` - Media files
- Jekyll sites (if used) follow standard Jekyll structure with `_config.yml`

## Development Notes

### Testing Before Deploy
Always test changes locally before pushing to main, as all commits to main are immediately published to the live site.

### Path References
Use relative paths for assets (e.g., `./css/style.css` or `css/style.css`) to ensure compatibility with GitHub Pages URL structure.

### Jekyll Processing
GitHub Pages automatically processes Jekyll sites. To disable Jekyll processing (for plain HTML sites), add an empty `.nojekyll` file to the repository root.
