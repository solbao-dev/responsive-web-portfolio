# Responsive Web Portfolio

> A responsive portfolio built from scratch with Vanilla HTML, CSS, and JavaScript to understand the fundamentals behind modern frontend frameworks.

**CODYSSEY · Tool Learning**  
`HTML5` `CSS3` `JavaScript` `GitHub API` `Responsive Web` `GitHub Pages`

## Overview

The goal of this project was to understand the browser interaction cycle — **user event → state change → DOM update** — without relying on React, Vue, jQuery, Bootstrap, or other UI frameworks.

It implements responsive layouts, theme persistence, GitHub API integration, form validation, filtering, and interaction states using browser-native technologies.

## Core Features

- Mobile-first responsive layout with `768px` and `1024px` breakpoints
- Dark mode with `prefers-color-scheme` detection and `localStorage` persistence
- Responsive navigation and hamburger menu
- Smooth scrolling and scroll-aware navigation styling
- Intersection Observer reveal animations
- Contact-form validation with field-level error messages
- GitHub REST API integration using `fetch` and `async/await`
- Loading, success, error, and empty UI states
- Repository filtering by programming language
- Hero typing effect

## Tech Stack

| Area | Technology |
|---|---|
| Markup | Semantic HTML5 |
| Styling | CSS3, Flexbox, Grid, Custom Properties |
| Script | Vanilla JavaScript ES6+ |
| Browser APIs | Fetch API, Intersection Observer, localStorage |
| Integration | GitHub REST API |
| Deployment | GitHub Pages |

## State → Rendering

| Event | State change | UI result |
|---|---|---|
| Theme toggle | `data-theme` + localStorage | Global color variables update |
| GitHub API request | loading → success/error/empty | Project section changes state |
| Form input | validation state | Inline error feedback |
| Language filter | `activeLang` | Project cards re-render |

## Structure

```text
responsive-web-portfolio/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js
├── images/
└── README.md
```

## Run Locally

```bash
git clone https://github.com/solbao-dev/responsive-web-portfolio.git
cd responsive-web-portfolio
```

Open the project with VS Code and run `index.html` with Live Server. The GitHub username can be configured in `js/main.js` through `CONFIG.githubUsername`.

## Screenshots

| Desktop | Mobile | Dark Mode |
|---|---|---|
| ![Desktop](images/desktop.png) | ![Mobile](images/mobile.png) | ![Dark Mode](images/darkmode.png) |

## Known Limitations

- Unauthenticated GitHub API requests are rate-limited; the UI handles API failure as an explicit error state.
- The contact form currently validates input and displays a success state but does not send email to a backend service.

## What I Learned

Building without a framework helped me understand what frameworks normally abstract away: DOM updates, UI state, browser APIs, persistence, responsive layout, and error handling. It also reinforced the importance of designing not only the successful path but also loading, empty, and failure experiences for users.

---

Part of my **CODYSSEY Tool Learning** journey.