# Portfolio BTS SIO SISR — Axel Royer

Site statique : HTML, CSS et JavaScript natifs, sans framework ni dépendance.

## Lancer le site

- **Recommandé** : extension *Live Server* de VS Code (clic droit sur `code.html` → *Open with Live Server*).
- **Sans outil** : double-clic sur `code.html`. Tout s’affiche, mais le bouton « Copier » peut être bloqué par le navigateur.
- **En ligne** : déposer le dossier entier chez n’importe quel hébergeur statique (GitHub Pages, Netlify, ton NAS…).
  Renommer `code.html` en `index.html` permet d’avoir une adresse sans nom de fichier.

## Arborescence

```
code.html         contenu du site (sommaire en tête du fichier)
code.css          styles (sommaire en tête, 16 sections dans l’ordre de la page)
code.js           interactions (sommaire en tête, 12 sections)
docs/             documents publiés (PDF, XLSX)
docs/apercus/     aperçus des documents (WebP 480 × 340)
fonts/            police Archivo hébergée avec le site + sa licence (OFL)
og-image.png      image d’aperçu pour LinkedIn, Discord…
robots.txt        autorise l’indexation
```

## Modifier le contenu

| Je veux… | Où |
|---|---|
| Ajouter un projet | `code.html`, section PROJETS : copier le **MODÈLE** commenté en fin de baie (`data-context="ecole"` ou `"perso"`). Il apparaît tout seul dans la matrice B1, les indicateurs, la recherche et la fiche. |
| Ajouter une mission en entreprise | Même modèle, mais à placer dans la section ALTERNANCE (`<div id="missions">`), avec `data-context="entreprise"` et `data-status="ongoing"` (LED bleue « En continu »). |
| Compléter une fiche (difficultés, résultats) | Dans le projet, retirer les balises de commentaire autour du bloc **À COMPLÉTER**. |
| Ajouter un document | Le copier dans `docs/` (avec son aperçu WebP 480 × 340 dans `docs/apercus/`), puis dupliquer une carte dans la section DOCUMENTATION, dans le bon groupe (Missions en entreprise, Projets, Épreuve et références). Pour un PDF, garder `data-viewer` (ouverture dans la visionneuse). Pour rattacher le document à un projet ou une mission, ajouter aussi un lien dans sa carte (bloc `unit-links`). |
| Ajouter une étape au parcours | Ajouter un `<li class="tl-item">` dans la frise (section PROFIL) : elle s’affiche sur 4 colonnes et passe à la ligne toute seule. Pour la dernière étape (l’objectif), garder la classe `tl-next`. |
| Changer une couleur | `code.css`, section 01 : chaque couleur est écrite une fois sous la forme `light-dark(clair, sombre)`. |
| Changer l’adresse email | `code.js` section 00 (`CONTACT_EMAIL`) et `code.html` section CONTACT. |

## Une fois le site en ligne

1. Dans `code.html`, remplacer `og-image.png` par son adresse complète (`https://…/og-image.png`) dans la balise `og:image`.
2. Reporter l’adresse du site dans le tableau de synthèse E5 (champ « Adresse URL du portfolio »).

## Vérifications effectuées (octobre 2026)

- Tests automatisés : fonctionnement, liens, fichiers, clavier, thème, impression, 8 largeurs d’écran, sans JavaScript, animations réduites.
- Accessibilité axe-core (WCAG 2.2 AA) dans 7 états de la page : aucune violation détectée. Ce test automatique ne remplace pas un audit RGAA complet.
- Lighthouse : 100 / 100 / 100 / 100 sur ordinateur, 98 / 100 / 100 / 100 sur mobile, mesuré sur un serveur local sans compression (un hébergeur avec gzip fera mieux).
