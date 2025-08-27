## GTA‑6 Landing Page (React + Vite)

A high‑impact landing page inspired by GTA VI with an animated intro reveal and parallax hero built using React, Vite, Tailwind CSS, and GSAP.

### Features
- **Animated intro mask**: SVG text mask reveal powered by GSAP timelines
- **Parallax hero**: Mouse‑driven parallax across sky/bg/text layers
- **Character/hero reveal**: Smooth scale/position transitions on content load
- **Utility‑first styling**: Tailwind CSS v4 classes
- **Iconography**: Remix Icon

### Tech Stack
- **React** 19
- **Vite** 6
- **Tailwind CSS** 4 (via `@tailwindcss/vite`)
- **GSAP** (`@gsap/react`, `gsap`)
- **Remix Icon**

### Project Structure
```
GTA-6-Landing-page/
  public/                # Static assets served at /
    bg.png
    sky.png
    girlbg.png
    imag.png
    ps5.png
    pricedown.otf
    logo18.png
  src/
    App.jsx              # Main page + animations
    index.css            # Tailwind + custom font-face
    main.jsx             # App mount point
  index.html             # Vite HTML entry
  vite.config.js         # Vite + React + Tailwind plugin
  eslint.config.js       # ESLint rules
  package.json           # Scripts and deps
```

### Prerequisites
- Node.js 18+ (recommended: latest LTS)
- npm 9+ (ships with Node)

Verify versions:
```bash
node -v
npm -v
```

### Setup & Run (Development)
```bash
# install dependencies
npm install

# start dev server (Vite)
npm run dev

# Vite will print a local URL, typically:
#   Local:   http://localhost:5173/
```

Open the printed Local URL in your browser.

### Production Build & Preview
```bash
# create an optimized production build in dist/
npm run build

# locally preview the production build
npm run preview
```

### Linting
```bash
npm run lint
```

### Notes on Assets & Paths
- Files in `public/` are served from the site root. In JSX/HTML, reference them as `/bg.png` (absolute) or `bg.png` from the root URL.
- If the custom font does not load, update the `@font-face` URL in `src/index.css` to use an absolute path:
  ```css
  @font-face {
    font-family: "pricedown";
    src: url("/pricedown.otf");
  }
  ```

### Troubleshooting
- **Blank screen or missing images**: Ensure assets exist in `public/` and references point to `/asset-name.ext`.
- **Font not loading**: Use `/pricedown.otf` as shown above.
- **Port in use**: Start dev server on another port:
  ```bash
  npm run dev -- --port 5174
  ```
- **Animations not running**: Check console for errors; ensure `@gsap/react` and `gsap` are installed from `package.json` via `npm install`.

### Available Scripts
- **`npm run dev`**: Start Vite dev server
- **`npm run build`**: Build for production (outputs to `dist/`)
- **`npm run preview`**: Preview production build
- **`npm run lint`**: Run ESLint

### License
This project is for educational/demonstration purposes. No affiliation with Rockstar Games. Use assets responsibly.


