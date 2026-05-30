# CLAUDE.md — pipelineai-site

Site vitrine **PipelineAI** (prospection B2B clé en main). Repo **public**, déployé via **GitHub Pages** (fichier `CNAME` = pipelineai.fr) : **tout push sur `main` = déploiement automatique en prod.**

## Structure
- `index.html` — landing (React standalone monté sur `<div id="app">` via `landing/*.js`). ⚠️ Le `<body>` contient un **contenu statique SEO dans `#app`** (H1, sections, FAQ + JSON-LD `FAQPage`) que React remplace au chargement — NE PAS le supprimer (c'est ce que Googlebot indexe).
- `blog/` — articles HTML + covers `blog-cover-*.png` (1200×630).
- `enrichir-vos-contacts.html` — page feature (à la racine).
- `sitemap.xml`, `robots.txt`, `Mentions.html`, `dashboard.html`.
- `landing/` — JS/CSS de la landing React.

## Règles d'édition
- Éditer ici, `git add/commit/push origin main` → déploie.
- **Toujours `git pull` + comparer avant d'écraser** (le repo peut être plus à jour que le local).
- Charte visuelle : fond bleu nuit `#0B1120`, primaire `#3B82F6`, dégradé `#3B82F6→#8B5CF6`, Plus Jakarta Sans + JetBrains Mono.
- Repo **public** : ne rien committer de sensible ici (clés, stratégie, données clients).

## Notes
- Après changement SEO : Search Console → « Demander une indexation ».
- Backend séparé (repo privé `pipelineai-backend`, déployé sur Railway).
