# Nova — React + Tailwind Landing Page

A modern, responsive landing page built with React, Vite, and Tailwind CSS. It features animated titles, interactive buttons, custom clip-path imagery, and clean sectioned layout (About, Features, Store, Contact) with a social footer.

## Features
- **Responsive UI** with Tailwind CSS utility classes
- **Animated titles** and transitions using custom classes and GSAP hooks
- **Interactive buttons** with `group` hover effects and text transitions
- **Custom shapes** via CSS `clip-path` (see `index.css`)
- **Modular components**: `Navbar`, `Features`, `Store`, `Contact`, `Footer`, `Button`, `AnimatedTitle`
- **Iconography** with `react-icons`

## Tech Stack
- React 19 + Vite 7
- Tailwind CSS 3
- GSAP (`gsap`, `@gsap/react`) for animations
- React Icons
- Utility helpers: `clsx`

## Getting Started
1. Install dependencies:
   ```bash
   npm install
   ```
2. Start the dev server:
   ```bash
   npm run dev
   ```
3. Build for production:
   ```bash
   npm run build
   ```
4. Preview the production build:
   ```bash
   npm run preview
   ```

## Available Scripts
- `npm run dev` — Start Vite dev server
- `npm run build` — Build the app for production
- `npm run preview` — Preview the production build locally
- `npm run lint` — Run ESLint

## Project Structure
```
TailwindReact/
├─ public/                  # Static assets (served as-is)
├─ src/
│  ├─ components/
│  │  ├─ Navbar.jsx
│  │  ├─ Features.jsx
│  │  ├─ Store.jsx
│  │  ├─ Contact.jsx        # Uses ImageClipBox + clip-path classes
│  │  ├─ Footer.jsx         # Social links via react-icons
│  │  ├─ Button.jsx         # group hover transitions
│  │  └─ AnimatedTitle.jsx  # Title animations
│  ├─ App.jsx
│  ├─ index.css             # Tailwind + custom utilities (clip-path, etc.)
│  └─ main.jsx
├─ index.html
├─ tailwind.config.js
├─ postcss.config.js
└─ vite.config.js
```

## Styling & Utilities
- Tailwind utilities live in `src/index.css`.
- Custom classes like `contact-clip-path-1` and `contact-clip-path-2` use CSS `clip-path` to shape images.
- `group` is applied on parent elements (e.g., in `Button.jsx`) to enable `group-hover:*` effects on children.

## Assets
Place images under `public/img/` and reference them like `/img/filename.webp` inside components.

## Deployment
You can deploy the production build (`npm run build`) to any static hosting provider:
- Netlify, Vercel, GitHub Pages, Cloudflare Pages, etc.
Upload the contents of `dist/` as your site output.

## License
This project is provided as-is for educational and demo purposes. Adapt and use freely within your projects.
