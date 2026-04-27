<div align="center">
  <h1>Ayaka Link Hub</h1>
  <p>A soft anime-style link aggregation station for Ayaka's blog, socials, media and daily portals.</p>
</div>

---

<p align="center">
  <img src="./docs/readme-banner.svg" alt="Ayaka Link Hub banner" width="100%" />
</p>

<p align="center">
  A Vue-powered personal link hub with a two-dimensional Miku-inspired vibe, featuring soft gradients, rounded cards,
  hover sweeps, theme switching and animated profile details.
</p>

<p align="center">
  <a href="#readme">简体中文</a>
  ·
  <a href="https://blog.ayakacloud.cn">BLOG</a>
  ·
  <a href="https://github.com/KasuganoAyaka">GITHUB</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Vue-3-7AD6D4?style=for-the-badge&logo=vuedotjs&logoColor=white" alt="Vue 3" />
  <img src="https://img.shields.io/badge/Vite-6-8FA8FF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite 6" />
  <img src="https://img.shields.io/badge/Responsive-Ready-8BDDCB?style=for-the-badge" alt="Responsive Ready" />
  <img src="https://img.shields.io/badge/Theme-Light%20%2F%20Dark-F6A6BF?style=for-the-badge" alt="Light and Dark Theme" />
  <img src="https://img.shields.io/badge/License-MIT-4F5563?style=for-the-badge" alt="MIT License" />
</p>

<p align="center">
  Hero Profile • Quick Links • Works • Contact • Content & Interests • Hover Motion • Copy Feedback
</p>

## Station Overview

Ayaka Link Hub is a lightweight personal landing page built with `Vue 3 + Vite`.
It is designed to visually align with the Anime Blog project while staying focused on one job:
collecting important destinations into a single soft, polished, mobile-friendly page.

## Features

- Soft cyan gradient interface inspired by Miku-style teal accents
- Animated hero profile with avatar hover interaction
- Quick icon bar for social and content shortcuts
- Sectioned link cards for works, contact, and content interests
- Stronger hover feedback with visible sweep-light motion
- Copy-link feedback and theme toggle support
- Mobile-friendly layout with rounded card presentation

## Preview Structure

- `作品与主站`
  Blog, network drive, daily food picker, project repository
- `与我取得联系`
  Email, Telegram, QQ, Discord
- `内容与兴趣`
  X, BiliBili, KooK game hub

## Tech Stack

- `Vue 3`
- `Vite`
- `lucide-vue-next`
- Plain CSS with custom theme variables and motion styling

## Getting Started

```bash
npm install
npm run dev
```

Local development server:

```text
http://127.0.0.1:4173/
```

## Build

```bash
npm run build
```

Production files will be generated in:

```text
dist/
```

## Project Structure

```text
.
├─ docs/
│  └─ readme-banner.svg
├─ public/
│  └─ ayaka.jpg
├─ src/
│  ├─ components/
│  ├─ data/
│  ├─ App.vue
│  ├─ main.js
│  └─ styles.css
├─ LICENSE
├─ package.json
└─ README.md
```

## Customization

Most content can be updated from:

```text
src/data/site.js
```

You can change:

- profile text
- quick links
- section groups
- card badges
- target URLs

Visual theme and interaction details can be adjusted in:

```text
src/styles.css
```

## License

This project is licensed under the [MIT License](./LICENSE).
