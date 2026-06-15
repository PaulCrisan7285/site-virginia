# Cabinet Psihologic Virginia Crișan — Website

Site bilingv (română / engleză) pentru un cabinet de psihologie din Cluj-Napoca,
cu sistem de administrare a articolelor (CMS) fără cod.

🔗 **Live:** [virginiacrisan.ro](https://virginiacrisan.ro)

---

## ✨ Funcționalități

- **Bilingv RO / EN** — comutare instantanee a întregului conținut printr-un toggle
- **Design responsive** — optimizat pentru desktop, tabletă și mobil (cu meniu hamburger)
- **Blog cu CMS** — articolele se administrează printr-un panou vizual (Decap CMS), fără cod
- **Iconițe automate** — fiecare articol primește o iconiță în funcție de categorie
- **Animații la scroll** — efecte fade-in subtile, cu respectarea `prefers-reduced-motion`
- **Formular de contact** — cu protecție anti-spam (honeypot), integrabil cu Netlify Forms / Formspree
- **SEO optimizat** — meta tags, Open Graph, date structurate (schema.org), sitemap, robots.txt
- **Accesibilitate** — focus vizibil pe tastatură, contrast adecvat, markup semantic

---

## 🛠️ Tehnologii

| Zonă | Tehnologie |
|------|-----------|
| Structură | HTML5 semantic |
| Stilizare | CSS3 (Grid, Flexbox, custom properties, animații) |
| Interactivitate | JavaScript vanilla (fără dependențe) |
| Iconițe | SVG inline (stil Lucide) |
| CMS | Decap CMS (git-based) |
| Hosting | Netlify |
| Tipografie | Playfair Display + Inter (Google Fonts) |

---

## 📁 Structura proiectului

```
.
├── index.html           # Pagina principală (single-page)
├── admin/
│   ├── index.html       # Panoul de administrare Decap CMS
│   └── config.yml       # Configurarea colecțiilor CMS
├── data/
│   └── articole.json    # Articolele de blog (editabile din CMS)
├── media/               # Imagini (poze, articole)
├── sitemap.xml          # Sitemap pentru SEO
├── robots.txt           # Directive pentru motoarele de căutare
└── GHID-INSTALARE.md    # Ghid pas-cu-pas de instalare și administrare
```

---

## 🚀 Instalare & deployment

Vezi ghidul complet în [`GHID-INSTALARE.md`](GHID-INSTALARE.md). Pe scurt:

1. Urcă fișierele într-un repository GitHub
2. Conectează repository-ul la Netlify (Import an existing project)
3. Activează Netlify Identity + Git Gateway pentru panoul de admin
4. (Opțional) Conectează un domeniu propriu

---

## 📝 Administrarea conținutului

Articolele se adaugă și se editează din panoul de admin disponibil la `/admin`,
fără a atinge codul. Fiecare articol suportă conținut bilingv (RO/EN), categorie,
rezumat și dată.

---

## 📄 Licență

Proiect privat. Toate drepturile rezervate.
