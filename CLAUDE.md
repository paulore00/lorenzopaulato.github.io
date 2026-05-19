# CLAUDE.md — Lorenzo Paulato Portfolio

Questo file viene letto automaticamente da Claude Code ad ogni sessione.
Per i dettagli completi del progetto leggi sempre anche:

@BRIEF.md

---

## Istruzioni per Claude

### Cosa siamo
Sito portfolio personale di Lorenzo Paulato, Product Designer.
Deployato su GitHub Pages: `https://lorenzopaulato.github.io`
Tecnologia: HTML / CSS / JS vanilla — nessun framework, nessun build step.

### Prima di modificare qualsiasi file
1. Leggi `BRIEF.md` per capire identità visiva, struttura e regole dei colori.
2. Leggi il file che stai per modificare prima di toccare nulla.
3. Controlla quale pagina progetto usa quale sfondo (nero / bianco / rosso) per non rompere i contrasti.

### Regole d'oro
- **Colori:** solo `#9c1915` (rosso), `#FFFFFF` (bianco), `#100E09` (nero). Nessun altro colore.
- **Font:** `'Helvetica Neue', Arial, sans-serif` per tutto (display e body). Non usare Google Fonts sull'homepage.
- **Nessun framework CSS o JS** — tutto vanilla.
- **Percorsi immagini** nelle pagine progetto: `../assets/images/X.jpeg` (relativi, non assoluti).
- La nav usa `mix-blend-mode: difference` → su sfondi bianchi aggiungere override `mix-blend-mode: normal`.
- Il reveal wireframe→foto è un pattern identitario: non rimuoverlo dai project card.
- Commenti nel codice: solo se il motivo non è ovvio. Niente docstring, niente spiegazioni ovvie.

### Aggiungere un nuovo progetto
1. Copia uno dei file `projects/*.html` con lo stesso sfondo desiderato.
2. Aggiorna i link nel nav di `index.html` (griglia `projects-grid`).
3. Aggiorna i link `project-nav` (prev/next) nelle pagine adiacenti.
4. Aggiungi le immagini in `assets/images/` con numerazione progressiva.
5. Segui la rotazione colori: nero → bianco → rosso → nero…

### Deploy
```bash
git add .
git commit -m "descrizione breve"
git push
```
GitHub Pages aggiorna automaticamente da branch `main`, root `/`.

### Cose ancora da fare (backlog)
- [ ] Favicon — logo LP minimalista
- [ ] Meta OG tags per condivisione social
- [ ] Pagina 404 custom
- [ ] Transizione animata tra pagine
- [ ] Form contatti (Formspree)
- [ ] Nav hamburger per mobile
- [ ] Aggiungere progetti futuri
