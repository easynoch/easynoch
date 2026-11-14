# Enoch Adesina — Email Marketing Portfolio

Klaviyo Email Marketing Specialist portfolio for Shopify DTC brands.

**Stack:** Next.js 15 · TypeScript · Tailwind CSS v4 · Framer Motion

---

## Quick start

```bash
npm install
npm run dev
```

Open http://localhost:3000

---

## 1. Connect the contact form (Formspree)

1. Create a free account at https://formspree.io
2. Create a new form and copy the form ID (e.g. `xyzabcde`)
3. Open `src/app/contact/page.tsx`
4. Replace:

```ts
const FORMSPREE_ID = "YOUR_FORMSPREE_ID";
```

with your real ID. Messages will be sent to the email you registered with Formspree.

Until you do this, the form still works in “demo” mode (shows success but does not send).

---

## 2. Add email screenshots

1. Export designs from Figma as PNG/JPG (2x recommended)
2. Drop files into `public/screenshots/`
3. Use the filenames listed in `public/screenshots/README.txt`

Case study pages automatically swap placeholders for real images when the file exists.

---

## 3. Deploy to Vercel

```bash
npx vercel
```

Or connect the GitHub repo on vercel.com.

---

## Project structure

```
src/
├── app/
│   ├── page.tsx          # Home
│   ├── work/             # Case studies
│   ├── designs/          # Figma design gallery
│   ├── about/
│   └── contact/          # Formspree-powered form
├── components/
│   ├── Navbar.tsx
│   ├── Footer.tsx
│   └── ScreenshotPlaceholder.tsx
└── data/
    └── projects.ts       # Case studies + design samples
public/
└── screenshots/          # Drop your email images here
```

---

## Customization

| What | Where |
|------|--------|
| Projects / metrics / Figma links | `src/data/projects.ts` |
| Colors | `src/app/globals.css` |
| Contact & social links | `Footer.tsx` + `contact/page.tsx` |
| Form backend | `contact/page.tsx` → `FORMSPREE_ID` |
