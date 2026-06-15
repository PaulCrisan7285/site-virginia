# Virginia Crișan Psychology Practice — Website

A bilingual (Romanian / English) website for a psychology practice in Cluj-Napoca,
featuring a no-code content management system for blog articles.

🔗 **Live:** [virginiacrisan.ro](https://virginiacrisan.ro)

---

## ✨ Features

- **Bilingual RO / EN** — instant switching of all content via a language toggle
- **Responsive design** — optimized for desktop, tablet, and mobile (with hamburger menu)
- **Blog with CMS** — articles are managed through a visual panel (Decap CMS), no code required
- **Automatic icons** — each article gets an icon based on its category
- **Scroll animations** — subtle fade-in effects, respecting `prefers-reduced-motion`
- **Contact form** — with anti-spam protection (honeypot), integrable with Netlify Forms / Formspree
- **SEO optimized** — meta tags, Open Graph, structured data (schema.org), sitemap, robots.txt
- **Accessibility** — visible keyboard focus, adequate contrast, semantic markup

---

## 🛠️ Tech Stack

| Area | Technology |
|------|-----------|
| Structure | Semantic HTML5 |
| Styling | CSS3 (Grid, Flexbox, custom properties, animations) |
| Interactivity | Vanilla JavaScript (no dependencies) |
| Icons | Inline SVG (Lucide style) |
| CMS | Decap CMS (git-based) |
| Hosting | Netlify |
| Typography | Playfair Display + Inter (Google Fonts) |

---

## 📁 Project Structure

```
.
├── index.html           # Main page (single-page)
├── admin/
│   ├── index.html       # Decap CMS admin panel
│   └── config.yml       # CMS collections configuration
├── data/
│   └── articole.json    # Blog articles (editable from the CMS)
├── media/               # Images (photos, articles)
├── sitemap.xml          # Sitemap for SEO
├── robots.txt           # Directives for search engines
└── GHID-INSTALARE.md    # Step-by-step setup & administration guide (Romanian)
```

---

## 🚀 Installation & Deployment

See the full guide in [`GHID-INSTALARE.md`](GHID-INSTALARE.md). In short:

1. Upload the files to a GitHub repository
2. Connect the repository to Netlify (Import an existing project)
3. Enable Netlify Identity + Git Gateway for the admin panel
4. (Optional) Connect a custom domain

---

## 📝 Content Management

Articles are added and edited through the admin panel available at `/admin`,
without touching the code. Each article supports bilingual content (RO/EN),
category, summary, and date.

---

## 📄 License

Private project. All rights reserved.
