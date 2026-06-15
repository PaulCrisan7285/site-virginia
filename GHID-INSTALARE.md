# 📘 Ghid complet — Site Cabinet Psihologic Virginia Crișan

Acest ghid te ajută să pui site-ul online și să activezi panoul de admin
unde soția ta poate scrie articole singură, fără cod.

Durata totală: ~30-40 de minute, o singură dată. După aceea, ea publică în 2 minute.

---

## 📁 Ce conține folderul

```
site/
├── index.html              ← site-ul propriu-zis
├── data/
│   └── articole.json        ← aici se salvează articolele
└── admin/
    ├── index.html           ← panoul de admin
    └── config.yml           ← configurarea panoului
```

**Important:** păstrează exact această structură de foldere. Nu redenumi folderele.

---

## PARTEA 1 — Pui site-ul online (GitHub + Netlify)

### Pasul 1: Cont GitHub
1. Intră pe **github.com** și creează un cont gratuit (dacă nu ai deja).

### Pasul 2: Creează un repository
1. Apasă pe **+** (dreapta sus) → **New repository**
2. Nume: de ex. `site-virginia` (poate fi orice)
3. Bifează **Public** (sau Private, merge și așa)
4. Apasă **Create repository**

### Pasul 3: Urcă fișierele
1. În pagina noului repository, apasă **uploading an existing file**
2. Trage TOT conținutul folderului `site/` (index.html, folderul data, folderul admin)
3. Apasă **Commit changes**

### Pasul 4: Conectează la Netlify
1. Intră pe **netlify.com** și fă cont (poți folosi contul GitHub — e cel mai simplu)
2. Apasă **Add new site** → **Import an existing project**
3. Alege **GitHub** și selectează repository-ul `site-virginia`
4. Lasă setările pe default și apasă **Deploy**
5. În ~1 minut site-ul e LIVE! Primești un link de tip `nume-aleatoriu.netlify.app`

🎉 Site-ul e online! Articolele demo apar deja.

---

## PARTEA 2 — Activează panoul de admin (Decap CMS)

Asta îi permite soției tale să adauge articole singură.

### Pasul 5: Modifică fișierul config
1. În repository-ul de pe GitHub, deschide `admin/config.yml`
2. (Nu e nevoie de modificări dacă folosești git-gateway — sări la pasul 6)

### Pasul 6: Activează autentificarea (Identity)
1. În Netlify, mergi la site-ul tău → **Integrations** (sau **Site settings**)
2. Caută **Identity** și apasă **Enable Identity**
3. Tot la Identity → **Registration** → setează pe **Invite only**
   (ca să nu se poată înregistra oricine)

### Pasul 7: Activează Git Gateway
1. Tot în Identity → derulează la **Services** → **Git Gateway**
2. Apasă **Enable Git Gateway**

### Pasul 8: Invită soția ta (sau pe tine)
1. La Identity → **Invite users**
2. Scrie adresa de email a soției tale
3. Ea primește un email cu un link de activare → își setează o parolă

### Pasul 9: Gata! Cum intră ea în panou
1. Merge pe `link-ul-site-ului.netlify.app/admin`
2. Se loghează cu email + parola
3. Vede o listă de articole, apasă pe **Lista de articole**
4. Poate adăuga un articol nou, completează câmpurile, apasă **Save** → **Publish**
5. În ~1 minut, articolul apare pe site automat! ✨

---

## 🌐 PARTEA 3 — Conectează domeniul virginiacrisan.ro

Domeniul `virginiacrisan.ro` este liber și e o alegere excelentă — scurt și memorabil.
Iată cum îl cumperi și îl conectezi la site.

### Pasul A: Cumpără domeniul
1. Intră pe un registrar românesc: **rotld.ro** (oficial), **cyberfolks.ro**, sau **nav.ro**
2. Caută `virginiacrisan.ro` și adaugă-l în coș
3. Completează datele de contact și plătește (~6–10 € / an pentru .ro)
4. Gata — domeniul e al vostru. Vei avea acces la un panou de unde poți
   configura "DNS" / "name servers" (vezi pasul C)

> 💡 Opțional: poți cumpăra și `.com` sau `.eu` în paralel, ca protecție de brand.
> Pentru un cabinet local, `.ro` este suficient.

### Pasul B: Adaugă domeniul în Netlify
1. În Netlify, intră la site-ul tău → **Domain management** (sau **Domain settings**)
2. Apasă **Add a domain** / **Add custom domain**
3. Scrie `virginiacrisan.ro` și apasă **Verify** → **Add domain**
4. Netlify îți va afișa instrucțiunile DNS (vezi pasul C)

### Pasul C: Leagă domeniul de Netlify (configurare DNS)
Ai două variante — alege UNA:

**Varianta 1 (recomandată, cea mai simplă): Netlify DNS**
1. În Netlify, la domeniul adăugat, alege **Set up Netlify DNS**
2. Netlify îți dă 4 adrese "name servers" (ex: `dns1.p01.nsone.net` ...)
3. Intră în panoul registrarului (de unde ai cumpărat domeniul)
4. Caută secțiunea **Name servers** / **Servere de nume** / **DNS**
5. Înlocuiește serverele existente cu cele 4 de la Netlify
6. Salvează. Gata!

**Varianta 2: Lași DNS la registrar (adaugi doar 2 înregistrări)**
1. În panoul registrarului, la secțiunea **DNS / Zone records**, adaugă:
   - Un record de tip **A**: nume `@`, valoare `75.2.60.5`
   - Un record de tip **CNAME**: nume `www`, valoare `numele-site-ului.netlify.app`
2. Salvează.

> ⏳ După ce salvezi, modificările DNS pot dura între 10 minute și 24 de ore
> să se propage (de obicei sub 1 oră). Ai răbdare dacă nu merge imediat.

### Pasul D: Activează HTTPS (lacătul verde 🔒)
1. După ce DNS-ul s-a propagat, Netlify activează **automat** certificatul HTTPS
2. Dacă nu se activează singur în câteva ore: Netlify → Domain management →
   **HTTPS** → **Verify DNS configuration** → **Provision certificate**
3. Gata! Site-ul va fi accesibil la `https://virginiacrisan.ro` cu lacăt verde.

> ⚠️ Important: cumpărarea domeniului și plata se fac DOAR de către tine,
> direct pe site-ul registrarului. Implică date personale și card —
> nu le da nimănui altcuiva.

---

## ✍️ Cum scrie un articol nou (pentru soția ta)

1. Intră pe `site.ro/admin` și se loghează
2. Apasă **Lista de articole** → **Articole**
3. Apasă butonul **+** pentru un articol nou
4. Completează:
   - **Data** — data publicării
   - **Categorie** — ex: Anxietate, Relații (iconița se alege automat după categorie)
   - **Titlu** — în română (și engleză dacă vrea)
   - **Rezumat** — 1-2 propoziții scurte
   - **Conținut** — textul complet (lasă o linie goală între paragrafe)
5. Apasă **Save** apoi **Publish** → **Publish now**
6. Gata! Articolul apare pe site în ~1 minut.

> 💡 Câmpurile în engleză sunt opționale. Dacă le lasă goale,
> site-ul afișează versiunea în română și la varianta EN.

---

## ❓ Probleme frecvente

**Articolele nu apar pe site după publish:**
Așteaptă 1-2 minute (Netlify reconstruiește site-ul). Reîmprospătează pagina (Ctrl+F5).

**Nu pot intra în /admin:**
Verifică că ai activat Identity ȘI Git Gateway (pașii 6 și 7).

**Vreau să șterg un articol:**
În panou, deschizi lista, apeși pe articolul respectiv și îl ștergi din listă, apoi Publish.

---

## 📧 Formularul de contact

Formularul funcționează automat pe Netlify! Mesajele apar în:
**Netlify → site-ul tău → Forms**

Ca să primești și email când vine un mesaj:
**Forms → Settings → Form notifications → Add notification → Email**
și pui adresa soției tale.

---

## 🔍 SEO — Cum te găsesc oamenii pe Google

Site-ul este deja optimizat pentru SEO (titlu, descriere, date structurate,
cuvinte-cheie despre psiholog Cluj-Napoca, sitemap). Iată ce mai poți face
ca să apară mai sus în Google:

1. **Google Business Profile (cel mai important pentru local!)**
   - Creează gratuit un profil pe business.google.com
   - Adaugă cabinetul: nume, adresă în Cluj-Napoca, telefon, program, poze
   - Asta te face să apari pe Google Maps și la căutări „psiholog Cluj"

2. **Google Search Console**
   - Intră pe search.google.com/search-console
   - Adaugă site-ul `virginiacrisan.ro` și trimite sitemap-ul (`/sitemap.xml`)
   - Google îți va indexa site-ul mai repede

3. **Articolele de blog = magneți pentru Google**
   - Fiecare articol nou (ex: „atacuri de panică", „terapie de cuplu")
     e o poartă prin care oamenii ajung pe site din căutări
   - Cu cât scrie mai des, cu atât mai bine pentru SEO

4. **Când ai poza Virginiei**, decomentează linia `og:image` din `index.html`
   (în secțiunea `<head>`) — link-ul va arăta cu poză pe Facebook/WhatsApp

---

Mult succes! Dacă te blochezi la vreun pas, salvează acest ghid și revino la el.
