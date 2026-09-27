# Paisatges de la Comunitat Valenciana

Pàgina web estàtica d'una sola pàgina amb una galeria de sis paisatges
emblemàtics del País Valencià (l'Albufera, Chulilla, Peníscola, Montanejos,
el Penyal d'Ifac i la Font Roja), pensada per a publicar-se amb **GitHub
Pages**.

## Fitxers

- `index.html` — l'estructura i el contingut de la pàgina.
- `style.css` — tots els estils (colors, tipografia, graella responsiva).
- `images/` — carpeta on han d'anar les fotos (vore
  `images/COM-AFEGIR-FOTOS.md` per als noms exactes i d'on traure fotos
  lliures de drets). Fins que no hi haja fotos, la pàgina mostra targetes
  de reserva amb icones, així que ja pots publicar-la tal com està.

No hi ha cap dependència de build ni de JavaScript extra: és HTML i CSS
purs (només carrega una font de Google Fonts).

## Com publicar-la a GitHub Pages

1. Crea un repositori nou a GitHub (per exemple `paisatges-valencians`).
2. Puja estos tres elements a l'arrel del repositori: `index.html`,
   `style.css` i la carpeta `images/` (amb les fotos que hi afiges).
   - Des de la web de GitHub: botó **Add file → Upload files**, arrossega
     els fitxers i fes *commit*.
   - Des de la terminal:
     ```bash
     git init
     git add .
     git commit -m "Primera versió de la pàgina"
     git branch -M main
     git remote add origin https://github.com/EL_TEU_USUARI/paisatges-valencians.git
     git push -u origin main
     ```
3. Al repositori, ves a **Settings → Pages**.
4. A "Build and deployment", tria **Deploy from a branch**, selecciona la
   branca `main` i la carpeta `/ (root)`, i guarda.
5. Espera un minut i la pàgina estarà disponible a:
   `https://EL_TEU_USUARI.github.io/paisatges-valencians/`

## Personalitzar-la

- Els colors principals estan definits com a variables al principi de
  `style.css` (`:root { --blau-mar: ...; --terra: ...; }`), així que es
  poden canviar en un sol lloc.
- Per afegir o llevar un indret de la galeria, copia o elimina un bloc
  `<figure class="card">...</figure>` dins d'`index.html`.
