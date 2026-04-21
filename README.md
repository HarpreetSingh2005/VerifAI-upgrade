# VerifAI — Anti-Counterfeit QR Platform

AI-powered product authentication for India's FMCG supply chain.  
Scan once to verify. QR dies after that. Counterfeiting stops being profitable.

---

## Setup & Run

```bash
# 1. Install dependencies (requires Node 18+)
npm install

# 2. Start dev server
npm run dev
```

Then open **http://localhost:5173** in your browser.

> ⚠️ If you see "Page Not Found" — make sure you open the URL that Vite prints
> in the terminal (usually http://localhost:5173), **not** a file:// path.
> Do NOT open index.html directly in the browser.

---

## Routes

| URL | Description |
|-----|-------------|
| `/` | Hero landing — scroll-driven 4-scene animation |
| `/app` | Dashboard — Generate, Verify, Database tabs |

---

## Tech Stack

- **React 18** + Vite
- **GSAP** + ScrollTrigger — all scroll animations
- **Three.js** via @react-three/fiber — QR shatter particle effect (Scene 3)
- **qrcode** — real scannable QR code generation
- **jsQR** — camera-based QR scanning
- **React Router v6** — client-side routing
- **localStorage** — all data, no backend required
- Plain CSS only — zero Tailwind

---

## Troubleshooting

**Page not found / blank page**
- Run `npm install` first, then `npm run dev`
- Open http://localhost:5173 exactly as shown in terminal

**Camera not working in Verify tab**
- Camera requires HTTPS or localhost — works fine on `npm run dev`
- Allow camera permissions when browser prompts

**QR shatter scene shows fallback / loading**
- Three.js is lazy-loaded — give it 1–2 seconds on first scroll to Scene 3
- If it stays as fallback, check browser console for WebGL errors
