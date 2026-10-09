# Papillon — site

Acest folder e un site static complet: aplicația Planificator + cele două ghiduri
de exerciții (Complet și Rapid), cu navigare comună și mod întunecat sincronizat
pe toate paginile. Nu are nevoie de server sau build — sunt fișiere simple
HTML/CSS/JS.

## Structura

```
papillon-site/
├── index.html              ← Planificatorul (pagina principală)
├── ghid-complet.html        ← Ghidul complet de studiu, cu index clicabil
├── ghid-rapid.html          ← Ghidul rapid de lucru, cu index clicabil
├── assets/
│   └── style.css            ← stiluri comune (navigare, mod întunecat, tipografie ghiduri)
└── downloads/
    ├── Papillon_Ghid_Complet_Exercitii.docx
    └── Papillon_Ghid_Rapid_Exercitii.docx
```

## Publicare online — două opțiuni simple

### Opțiunea A — Netlify Drop (cel mai rapid, ~1 minut)

1. Mergi la **https://app.netlify.com/drop**
2. Trage folderul `papillon-site` (tot folderul, nu fișierele individuale) direct în pagină
3. Gata — primești un link live (ex. `numele-tau.netlify.app`) imediat
4. Opțional: din contul Netlify poți schimba numele site-ului sau atașa un domeniu propriu

Nu necesită cont pentru testare rapidă, dar dacă vrei link permanent (nu expiră),
îți recomand să-ți faci un cont gratuit Netlify înainte de a trage folderul.

### Opțiunea B — GitHub Pages (gratuit, link permanent, fără cont Netlify)

1. Pe **github.com**, creează un repository nou (ex. `papillon-site`) — public
2. În repository, click **"uploading an existing file"** (sau **Add file → Upload files**)
3. Trage toate fișierele și folderele din `papillon-site` (index.html, ghid-complet.html,
   ghid-rapid.html, assets/, downloads/) — GitHub păstrează structura de foldere
4. Commit (Commit changes)
5. Mergi la **Settings → Pages** (în meniul din stânga al repository-ului)
6. La **Source**, alege branch-ul `main` și folderul `/ (root)`, apoi **Save**
7. După 1-2 minute, site-ul e live la:
   `https://<numele-tau-de-utilizator>.github.io/papillon-site/`

## Actualizări ulterioare

Pentru orice modificare viitoare (adăugare exerciții, corecturi text etc.),
trimite-mi noile fișiere sau spune-mi ce vrei schimbat — reconstruiesc paginile
afectate și le retrimit; tu doar re-încarci fișierele (drag & drop din nou pe
Netlify, sau upload din nou pe GitHub).

## Note tehnice

- Modul întunecat se salvează în `localStorage` (cheia `papapp_theme`) — comun
  tuturor celor 3 pagini, ca să rămână sincronizat când navighezi între ele.
- Selecțiile din Planificator se salvează tot în `localStorage`, local în
  browserul tău — nu sunt trimise nicăieri, nu necesită cont sau bază de date.
- Site-ul e complet static — poate fi găzduit și pe orice alt hosting static
  (Vercel, Cloudflare Pages, un server propriu etc.) în același fel: se
  urcă folderul așa cum e.
