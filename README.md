# Antonie de Groot — Portfolio Website

Een moderne, retro-futuristische portfolio website voor **Antonie de Groot**, gebouwd met React, Vite en CSS Custom Properties, exact gemodelleerd naar **Stylesheet(1).png** en **Website opmaak.png**.

---

## 🎨 Visual Identity & Design Tokens

- **Primary Pink**: `#FF0092`
- **Primary Yellow**: `#FFFF00`
- **Accent Cyan**: `#47C1E6`
- **Dark Background**: `#272C3F`
- **Dark UI**: `#111421`
- **White**: `#FFFFFF`
- **Light Pink**: `#FF80C9`

### Typografie
- **Display Header & CTA Font**: `Kunstraub` (`/fonts/Kunstraub.ttf`) — zware, geometrische, retro-futuristische arcade font.
- **Body & Subtitle Font**: `Helvetica Rounded` (`/fonts/helvetica-rounded-bold-5871d05ead8de.otf`) & `Helvetica`.

---

## 🚀 Aan de slag

### 1. Development Server starten
```bash
npm run dev
```
De website opent standaard op `http://localhost:3000` (of de poort getoond in de terminal).

### 2. Productie Build maken
```bash
npm run build
```
Genereert geoptimaliseerde statische bestanden in de map `dist/`.

### 3. Productie Preview bekijken
```bash
npm run preview
```

---

## 📂 Mappenstructuur

```text
website/
├── public/
│   ├── assets/              # Logo.png, Antoine Foto lagen, Background pattern.png
│   ├── fonts/               # Kunstraub.ttf, Helvetica Rounded, Helvetica.ttf
│   └── projecten/           # Echte projectafbeeldingen en PDF's
│       ├── branding-energy-drink/
│       └── emotie-wit-op-zwart/
├── src/
│   ├── components/
│   │   ├── Navbar.jsx       # Dark navbar met Logo en cyaan onderlijn
│   │   ├── Hero.jsx         # Hero met 3-laags chromatische offset portret & MY WORK knop
│   │   ├── Button.jsx       # Retro button met #FF80C9 lip en pressed state
│   │   ├── AnimatedButton.jsx # Squish entrance bounce animatie
│   │   ├── PortfolioGrid.jsx  # 4-koloms grid met afwisselend roze/geel kader
│   │   ├── ProjectCard.jsx  # Card met VIEW knop en afgeronde typografie
│   │   ├── ProjectPage.jsx  # Individuele pagina met terugknop, meta & documenten
│   │   ├── ImageGallery.jsx # Scrollbare showcase met fullscreen Lightbox
│   │   ├── PdfDownload.jsx  # Directe PDF downloadkaarten
│   │   ├── AboutSection.jsx # Introductie, Design DNA, disciplines en contact
│   │   ├── GraphicPattern.jsx # Antoine geel/roze merkelement
│   │   ├── Footer.jsx       # Donkere grafische footer
│   │   └── PageTransition.jsx # Route transities en staggers
│   ├── data/
│   │   └── projects.js      # Data-driven projectenlijst
│   ├── styles/
│   │   ├── tokens.css       # Kleuren en afmetingen
│   │   ├── typography.css   # @font-face definities en tekstklassen
│   │   ├── animations.css   # Squish keyframes en transitions
│   │   └── main.css         # Algemene layout en stijlen
│   ├── App.jsx              # Client router en pagina-orkestratie
│   └── main.jsx             # React entrypoint
├── index.html
├── package.json
└── vite.config.js
```

---

## ➕ Nieuw project toevoegen

1. Plaats je nieuwe projectmap in `public/projecten/jouw-project-naam/` met je afbeeldingen en PDF's.
2. Voeg een nieuw object toe in `src/data/projects.js` met de slug, titel, beschrijving, afbeeldingen en PDF's:
```js
{
  id: 'jouw-project-naam',
  slug: 'jouw-project-naam',
  title: 'Jouw Project Titel',
  nameOfWork: 'Jouw Project Titel',
  category: 'Branding & UI',
  year: '2025',
  role: 'Designer',
  tools: 'Illustrator, Figma',
  coverImage: './projecten/jouw-project-naam/cover.png',
  description: '...',
  images: [ ... ],
  pdfs: [ ... ]
}
```
3. Het project verschijnt automatisch in de portfolio grid en krijgt een eigen URL `/work/jouw-project-naam`!
