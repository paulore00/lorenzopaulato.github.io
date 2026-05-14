# BRIEF — Lorenzo Paulato Portfolio
> Questo file è per Claude Code: contiene tutto il contesto del progetto.

---

## Identità

**Nome:** Lorenzo Paulato  
**Professione:** Product Designer  
**Motto:** *Helping Through Shape* — la forma come strumento per risolvere problemi  
**Email:** paulato.lorenzo@gmail.com  
**Università:** Politecnico di Torino (2023–oggi) + ELISAVA Barcellona (exchange, 2025–2026)

---

## Brand Identity

### Colori
```
--red:   #9c1915   ← accento primario, mai usato come sfondo neutro
--white: #FFFFFF   ← sfondo "chiaro"
--black: #100E09   ← sfondo "scuro" (non nero puro)
```

### Tipografia
- **Display / Titoli:** Barlow Condensed (700, 900) — geometrico, condensato, impattante
- **Body / Testo:** DM Sans (300, 400, 500) — pulito, leggibile
- Google Fonts, già importati in `style.css`

### Geometrie identitarie
- Linee orizzontali sottili (1px) in rosso, bianco o nero
- Forme bombate / cerchi parziali come elementi decorativi
- I 3 colori giocano in contrasto a seconda dello sfondo
- Ogni progetto è presentato prima tramite **wireframe** (crea hype), poi reveal del prodotto reale

### Tono
Minimal, geometrico, diretto. Niente decorazioni superflue. Molto spazio bianco/nero. Numeri grandi come elemento grafico.

---

## Struttura del sito

```
index.html              ← Home: hero + griglia 2×2 progetti + about/contatti
style.css               ← CSS globale (cursore, nav, footer, variabili)
project.css             ← CSS condiviso per le pagine progetto
README.md               ← Questo file (istruzioni GitHub)
projects/
  nisus.html            ← Progetto 01, sfondo NERO
  monolith.html         ← Progetto 02, sfondo BIANCO
  blooming-wire.html    ← Progetto 03, sfondo ROSSO
  trust-me.html         ← Progetto 04, sfondo NERO con top-line rossa
assets/
  images/               ← Immagini estratte dal PDF portfolio (1.jpeg → 24.jpeg)
```

**Regola colori alternati per i progetti:**
- 01 Nisus → nero
- 02 Monolith → bianco
- 03 Blooming Wire → rosso
- 04 Trust Me → nero

---

## Progetti

### 01 · Nisus — *Not just a lamp*
- Lampada da scrivania con timer Pomodoro integrato
- Con: Hans Emilio Pianezza, Martino Trinchero, Juan Josè Ricci
- Ruolo: Concept Development, 3D Modeling, Product Engineering
- Feature chiave: slider luminosità + pulsante a clessidra per timer 25 min
- Prototipo stampato in 3D
- Immagini usate: 4 (wireframe), 5 (render), 6 (dettaglio base), 7 (esploso), 8 (prototipo)

### 02 · Monolith — *Speaker*
- Speaker Bluetooth personale, geometria essenziale
- Progetto personale
- Ruolo: tutto (concept, 3D, rendering)
- Feature: 3 driver, shell alluminio effetto pietra, 1 touch slider in cima
- Slogan: "Solid Presence. Refined Sound."
- Immagini: 9 (wireframe), 10 (schizzi), 11-12-13 (render), 14 (hero dark)

### 03 · Blooming Wire — *Flower holder*
- Portafiori in filo metallico, mono-materiale, pieghevole
- Con: Carlotta Schillaci, Martino Trinchero, Miriam Vindrola
- Ruolo: Concept Development, 3D Modeling, Prototyping
- **Vincitore Concept Design Competition**
- Ispirato ai Mandala trasformabili — giunti di forma invece di giunti meccanici
- Immagini: 15 (wireframe), 16 (schizzi), 17 (3D model), 18 (istruzioni uso), 19 (foto reale)

### 04 · Trust Me — *A speculative design*
- Wearable di facial recognition che suggerisce "di chi fidarsi" in tempo reale
- Progetto personale / provocazione su AI e scelte sociali delegate
- Hardware: ESP32-CAM, OLED display, speaker, button, MicroSD, DFPlayer, fabric band
- Output: percentuale + label (BAD / GOOD / PERFECT MATCH) + audio
- Immagini: 20 (hero wireframe tecnico), 21 (schema sistema), 22 (display), 23 (indossato)

---

## Funzionalità implementate

| Feature | Dove |
|---------|------|
| Cursore custom rosso + anello lag | `style.css` + JS inline in ogni pagina |
| Toggle lingua EN / IT | JS inline — `data-en` / `data-it` su ogni elemento |
| Wireframe → Reveal prodotto | Pulsante "Reveal Product" in hero di ogni progetto |
| Scroll reveal (IntersectionObserver) | JS inline in ogni pagina |
| Nav con mix-blend-mode:difference | `style.css` — attenzione: su sfondi bianchi va disattivato |
| Scrollbar custom rossa | `style.css` |
| Selezione testo rossa | `style.css` |

---

## Note tecniche

- **Nessun framework** — HTML/CSS/JS vanilla puro
- **Nessun build step** — i file si aprono direttamente nel browser
- I percorsi immagini nelle pagine progetto sono **relativi**: `../assets/images/X.jpeg`
- Il CSS della nav usa `mix-blend-mode: difference` → su pagine con sfondo bianco (Monolith) va aggiunto `mix-blend-mode: normal` nel CSS della pagina
- Per aggiungere un nuovo progetto: copia uno dei file in `projects/`, aggiorna i link nel nav di `index.html` e nei `project-nav` delle pagine adiacenti

---

## Deploy — GitHub Pages

Repository: `https://github.com/lorenzopaulato/lorenzopaulato.github.io`  
URL live: `https://lorenzopaulato.github.io`

```bash
# Prima volta
git init
git remote add origin https://github.com/lorenzopaulato/lorenzopaulato.github.io.git
git add .
git commit -m "init: portfolio site"
git push -u origin main

# Aggiornamenti successivi
git add .
git commit -m "descrizione modifica"
git push
```

In **Settings → Pages → Source: Deploy from branch → main → / (root)**

---

## Cosa manca / possibili miglioramenti futuri

- [ ] Favicon (logo LP minimalista)
- [ ] Meta OG tags per condivisione social con anteprima
- [ ] Pagina 404 custom
- [ ] Animazione di transizione tra pagine (page fade)
- [ ] Form contatti funzionante (es. Formspree — gratuito)
- [ ] Versione mobile ottimizzata (nav hamburger)
- [ ] Aggiungere nuovi progetti quando pronti

---

*Ultimo aggiornamento: Maggio 2026*
