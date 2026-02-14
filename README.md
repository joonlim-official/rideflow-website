<p align="center">
  <img src="https://files.manuscdn.com/user_upload_by_module/session_file/310519663319984753/UmCoYtfqdmmvGBhC.png" alt="RideFlow Logo" width="100" height="100" />
</p>

<h1 align="center">RideFlow — Marketing Website</h1>

<p align="center">
  <strong>Landing page, legal documents, and public-facing web presence for <a href="https://ridehelp.top">RideFlow</a></strong><br/>
  An AI-powered family ride coordination app for iOS and Android.
</p>

<p align="center">
  <a href="https://ridehelp.top"><img src="https://img.shields.io/badge/Live_Site-ridehelp.top-E91E63?style=flat-square" alt="Live Site" /></a>
  <img src="https://img.shields.io/badge/Hosted_on-GitHub_Pages-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub Pages" />
  <img src="https://img.shields.io/badge/HTML%2FCSS-Vanilla-F16529?style=flat-square&logo=html5&logoColor=white" alt="HTML/CSS" />
  <img src="https://img.shields.io/badge/License-Proprietary-lightgrey?style=flat-square" alt="License" />
</p>

---

## Overview

This repository contains the public marketing website for **RideFlow**, a production-grade mobile application that streamlines communication between parents and their ride helpers (nannies, carpoolers, family members). The website serves as the product's primary web presence, hosting the marketing landing page, privacy policy, and terms of service required for App Store and Google Play submissions.

The site is a **static, single-page application** built with vanilla HTML and CSS — no frameworks, no build step, no JavaScript dependencies. It is deployed via **GitHub Pages** with a custom domain (`ridehelp.top`) and loads in under one second on a 3G connection.

---

## Live Site

**https://ridehelp.top**

---

## Pages

| Page | Path | Description |
|------|------|-------------|
| **Landing Page** | `/` (`index.html`) | Product marketing page with hero section, interactive phone mockups, AI feature showcase, feature grid, onboarding flow, security overview, and app store download badges |
| **Privacy Policy** | `/privacy-policy.html` | GDPR-compliant privacy policy covering data collection, usage, storage, third-party sharing, and user rights |
| **Terms of Service** | `/terms-of-service.html` | Legal terms governing app usage, user responsibilities, intellectual property, and liability limitations |

---

## Design & Technical Details

### Architecture

The website is intentionally built without a JavaScript framework. Every page is a self-contained HTML file with embedded CSS, ensuring maximum performance, zero runtime dependencies, and trivial deployment. This approach was chosen because the site's purpose is informational — it does not require client-side routing, state management, or dynamic data fetching.

### Visual Design

The landing page follows a **warm, approachable aesthetic** designed to build trust with parents:

| Element | Implementation |
|---------|---------------|
| **Color palette** | Primary pink (`#E91E63`) with warm neutrals (`#F5F0EB`, `#FAF8F5`) and teal accents (`#00897B`) |
| **Typography** | Inter (Google Fonts) at weights 400–800 for clear hierarchy |
| **Navigation** | Fixed top bar with frosted glass effect (`backdrop-filter: blur(12px)`) |
| **Phone mockups** | Three CSS-only device frames showing Home, AI Quick Fill, and Family Chat screens |
| **Sections** | Hero, App Preview, AI Features (6 cards), Core Features (6 cards), How It Works (4 steps), Security (4 pillars), Download CTA |
| **Responsive** | Fully responsive from 320px mobile to 1200px+ desktop with CSS media queries |

### SEO & Open Graph

The landing page includes structured metadata for search engines and social media sharing:

- `<title>` and `<meta name="description">` optimized for "family ride coordination" keywords
- Open Graph tags (`og:title`, `og:description`, `og:image`, `og:type`) for rich link previews on Facebook, LinkedIn, and iMessage
- Favicon linked to the RideFlow app icon

### Performance

With no JavaScript bundle, no framework overhead, and a single external font request, the page achieves near-instant load times. The entire `index.html` is approximately 34 KB — smaller than most hero images on competing sites. CSS is embedded inline to eliminate render-blocking stylesheet requests.

---

## Repository Structure

```
rideflow-website/
├── index.html              # Marketing landing page (759 lines)
├── privacy-policy.html     # Privacy policy (342 lines)
├── terms-of-service.html   # Terms of service (271 lines)
├── CNAME                   # Custom domain configuration (ridehelp.top)
└── README.md               # This file
```

---

## Deployment

The site is deployed automatically via **GitHub Pages** from the `main` branch. Any push to `main` triggers a rebuild and deployment within minutes.

| Setting | Value |
|---------|-------|
| **Hosting** | GitHub Pages |
| **Branch** | `main` |
| **Custom domain** | `ridehelp.top` |
| **HTTPS** | Enforced (via GitHub Pages) |
| **CDN** | GitHub's global CDN (Fastly) |

### Custom Domain Setup

The `CNAME` file in the repository root points to `ridehelp.top`. DNS is configured with:

- An `A` record pointing to GitHub Pages IP addresses
- A `CNAME` record for `www` subdomain redirect

---

## Related Repositories

| Repository | Description |
|------------|-------------|
| [**rideflow**](https://github.com/joonlim-official/rideflow) | The full-stack mobile application — React Native (Expo), Express/tRPC server, PostgreSQL, WebSocket chat, and built-in AI |

---

## Local Development

Since the site is static HTML, no build tools are required. Open `index.html` directly in a browser or use any local server:

```bash
# Clone the repository
git clone https://github.com/joonlim-official/rideflow-website.git
cd rideflow-website

# Option 1: Open directly
open index.html

# Option 2: Local server (Python)
python3 -m http.server 8000

# Option 3: Local server (Node.js)
npx serve .
```

---

## License

Proprietary. All rights reserved.
