# 🎓 Donne Moi La Solution — Site Jekyll

Site one-page + blog pour cours de maths en ligne, hébergé sur GitHub Pages.

---

## 🚀 Mise en ligne en 5 étapes

### 1. Prérequis
- Avoir un compte [GitHub](https://github.com)
- Avoir Ruby + Jekyll installé localement (optionnel pour tester)

### 2. Créer le dépôt GitHub
1. Crée un nouveau repo nommé `dmls` (ou le nom que tu veux)
2. Rends-le **public**
3. Push ce dossier :

```bash
git init
git add .
git commit -m "Initial commit — DMLS site"
git remote add origin https://github.com/TON-USERNAME/dmls.git
git push -u origin main
```

### 3. Activer GitHub Pages
- Dans le repo → **Settings** → **Pages**
- Source : `main` branch, dossier `/root`
- Ton site sera dispo sur : `https://TON-USERNAME.github.io/dmls`

### 4. Configurer `_config.yml`
Ouvre `_config.yml` et remplace :
```yaml
url: "https://TON-USERNAME.github.io"   # ton username GitHub
baseurl: "/dmls"                         # nom du repo
author:
  name: "Ton Prénom Nom"
  email: "ton@email.fr"
```

---

## 💳 Configurer Stripe

1. Crée un compte sur [stripe.com](https://stripe.com)
2. Dans le dashboard Stripe → **Products** → crée tes produits :
   - "Pack 5h particulier" → 200€
   - "Pack 10h particulier" → 380€
   - "Abonnement mensuel" → 160€/mois
3. Pour chaque produit → **Payment Link** → copie l'URL
4. Colle ces URLs dans `_config.yml` :

```yaml
stripe:
  pack_5h_link: "https://buy.stripe.com/XXXXXXXX"
  pack_10h_link: "https://buy.stripe.com/YYYYYYYY"
  abonnement_link: "https://buy.stripe.com/ZZZZZZZZ"
```

---

## 📅 Configurer Cal.com

1. Crée un compte sur [cal.com](https://cal.com)
2. Configure tes disponibilités et tes types de réservation :
   - "Séance découverte (15 min)" — gratuit
   - "Cours particulier (1h)" — payant
   - "Cours groupe (1h30)" — payant
3. Note ton username Cal.com
4. Dans `_config.yml` :

```yaml
calcom:
  username: "ton-username-calcom"
```

---

## 📝 Ajouter un article de blog

Crée un fichier dans `_posts/` avec ce format de nom :
`AAAA-MM-JJ-titre-de-l-article.md`

En-tête obligatoire :
```yaml
---
layout: post
title: "Titre de l'article"
date: 2024-05-01
category: Méthode         # ou "Exercice corrigé"
niveau: Lycée             # Collège / Lycée / Terminale / Post-bac
readtime: 5               # minutes de lecture
excerpt: "Résumé court affiché sur la liste du blog."
---

Ton contenu en Markdown ici...
```

---

## 🖼️ Ajouter ta photo

Place ta photo dans `assets/images/prof.jpg`
(format recommandé : portrait 3:4, minimum 600×800px)

---

## 🔧 Tester en local

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000/dmls
```

---

## 📁 Structure du projet

```
dmls/
├── _config.yml          # Configuration principale
├── index.html           # One-page (Hero, À propos, Services, Tarifs, Cal.com, FAQ, Blog)
├── blog.html            # Page liste du blog
├── _layouts/
│   ├── default.html     # Layout principal
│   └── post.html        # Layout article
├── _includes/
│   ├── nav.html         # Navigation fixe
│   └── footer.html      # Pied de page
├── _posts/              # Tes articles de blog (.md)
├── assets/
│   ├── css/main.css     # Tous les styles
│   ├── js/main.js       # Interactions JS
│   └── images/          # Tes images (dont prof.jpg)
└── Gemfile              # Dépendances Ruby/Jekyll
```

---

## ✅ Checklist avant mise en ligne

- [ ] Remplacer `TON-USERNAME` dans `_config.yml`
- [ ] Ajouter ta photo dans `assets/images/prof.jpg`
- [ ] Remplir ton nom, email et bio dans `_config.yml`
- [ ] Créer tes produits Stripe et coller les Payment Links
- [ ] Créer ton compte Cal.com et renseigner ton username
- [ ] Mettre à jour les tarifs dans `_config.yml`
- [ ] Écrire ton premier vrai article de blog
- [ ] Mettre à jour les stats hero (élèves accompagnés, taux réussite)
- [ ] Activer GitHub Pages dans les settings du repo
