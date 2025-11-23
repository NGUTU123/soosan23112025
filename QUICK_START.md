# Quick Start Guide

## Astro Migration - Ready to Begin!

Your project is now configured with Astro. The old React pages still exist (generating warnings) but won't be used.

## Current Status

✅ Astro v5.16 installed and configured
✅ React integration enabled
✅ Tailwind CSS configured
✅ Base layout created
✅ Sample homepage working
✅ Build and dev server tested

## Start Development

```bash
npm run dev
```

Visit: `http://localhost:4321`

## What You'll See

The warnings about `.tsx` files in `src/pages/` are expected. These are your old React Router pages that will be replaced with `.astro` files.

## Migration Checklist

### Step 1: Pages Directory Setup ✅
- [x] Create `src/pages/` structure
- [x] Create `src/layouts/BaseLayout.astro`
- [x] Create sample `index.astro`

### Step 2: Convert Pages (Your Next Steps)
- [ ] Convert Index.tsx → index.astro
- [ ] Convert AboutPage.tsx → gioi-thieu.astro
- [ ] Convert ContactPage.tsx → lien-he.astro
- [ ] Convert TruckCatalog.tsx → san-pham/index.astro
- [ ] Convert TruckDetail.tsx → san-pham/[id].astro
- [ ] Convert BlogPage.tsx → tin-tuc/index.astro
- [ ] Convert BlogPostPage.tsx → tin-tuc/[slug].astro
- [ ] Convert ComparePage.tsx → so-sanh.astro

### Step 3: Update Components
- [ ] Replace `<Link to="">` with `<a href="">`
- [ ] Add client directives where needed
- [ ] Test interactive features

### Step 4: Data & Routes
- [ ] Implement `getStaticPaths()` for dynamic routes
- [ ] Import data files in Astro pages
- [ ] Test all routes

## Example Conversion

### Old React Page:
```tsx
// src/pages/AboutPage.tsx
import Header from '../components/Header';

export default function AboutPage() {
  return (
    <div>
      <Header />
      <h1>About</h1>
    </div>
  );
}
```

### New Astro Page:
```astro
---
// src/pages/gioi-thieu.astro
import BaseLayout from '../layouts/BaseLayout.astro';
import Header from '../components/Header.tsx';
---

<BaseLayout title="Giới thiệu">
  <Header client:load />
  <main>
    <h1>Giới thiệu</h1>
  </main>
</BaseLayout>
```

## Key Differences

| Aspect | React SPA | Astro SSG |
|--------|-----------|-----------|
| Routing | React Router | File-based |
| Pages | `.tsx` components | `.astro` files |
| Links | `<Link to="">` | `<a href="">` |
| Data | Runtime fetch | Build-time |
| Hydration | Full page | Islands only |

## Getting Help

When ready to convert a page:
1. Show me the React page content
2. Show me any data it uses
3. I'll convert it to Astro format

Read `ASTRO_SETUP_COMPLETE.md` for detailed examples and patterns.

---

**Ready to start?** Share your first page to convert!
