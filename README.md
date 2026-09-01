# 🐙 GitHub Profile Explorer

**Task 6 — API Integration Project**
Remote Internship @ Synent Technologies

A simple, dependency-free web app that fetches and displays live user data from the public **GitHub REST API**, built with vanilla JavaScript and the Fetch API.

🔗 **Live Demo:** https://sol-api-integration.vercel.app

---

## 📋 Objective

Fetch and display data from a public API using JavaScript's Fetch API, with proper loading and error states.

## ✨ Features

- **Live data fetching** — queries `https://api.github.com/users/{username}` in real time
- **Dynamic UI rendering** — avatar, name, bio, repo count, followers, following, location, company, and join date
- **Loading state** — animated spinner and status message while the request is in flight
- **Error handling** — distinct, human-readable messages for:
  - `404` — username not found
  - `403` — API rate limit exceeded
  - other non-OK responses
  - network/connection failures
- **XSS-safe rendering** — all API and user-supplied text is escaped before being inserted into the DOM
- **Keyboard support** — press `Enter` to search
- **Responsive, dark-themed UI** with no external CSS/JS frameworks

## 🛠️ Tech Stack

- HTML5
- CSS3 (no frameworks)
- Vanilla JavaScript (`fetch`, `async/await`)
- [GitHub REST API](https://docs.github.com/en/rest/users/users) (no auth/API key required)

## 📁 Project Structure

```
github-profile-explorer/
├── index.html      # App markup, styles, and logic (single file)
├── favicon.svg      # Site favicon
└── README.md        # Project documentation
```

## 🚀 Getting Started Locally

No build step or dependencies needed.

```bash
git clone https://github.com/YOUR_USERNAME/github-profile-explorer.git
cd github-profile-explorer
open index.html   # or just double-click the file
```

Or serve it locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## 🌐 Deployment

This project is deployed on **Vercel** as a static site — no build configuration required, since it's plain HTML/CSS/JS.

## ⚠️ Notes

- The GitHub public API is unauthenticated and rate-limited to ~60 requests/hour per IP. That's plenty for demo/portfolio use, but a production app would add a server-side proxy with a personal access token to raise the limit.

## 👤 Author

Built as part of a remote internship task at **Synent Technologies**.
