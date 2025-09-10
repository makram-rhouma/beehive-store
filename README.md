# Beehive Store – Site vitrine (Template Savora)

Ce dépôt contient un site vitrine statique basé sur le template « Savora » (BootstrapMade). Il inclut une page d’accueil (`index.html`), une page de confidentialité (`privacy.html`), des mentions/légales (`terms.html`) et les ressources nécessaires (CSS, JS, images, vendors, formulaires).

## Aperçu
- Stack: HTML5, Bootstrap 5.3.7, Bootstrap Icons, AOS, GLightbox, Isotope, ImagesLoaded
- Structure simple, 100% statique
- Formulaire newsletter (footer) avec validation JS et endpoint PHP (exemple)

## Arborescence
```
.
├─ assets/                  # CSS / JS / images / vendors
├─ forms/                   # Exemple endpoints PHP (newsletter)
├─ 404.html
├─ index.html               # Page d'accueil
├─ privacy.html             # Politique de confidentialité
├─ terms.html               # Conditions d'utilisation
```

## Lancer en local
- Option 1 (simple): Ouvrir `index.html` dans le navigateur (double-clic). Convient pour un aperçu statique.
- Option 2 (serveur local):
  - Avec PHP (requis si vous testez les formulaires PHP):
    ```bash
    php -S 127.0.0.1:8080 -t .
    ```
    Puis ouvrez http://127.0.0.1:8080
  - Avec l’extension VS Code « Live Server »: clic droit sur `index.html` → « Open with Live Server ».

Note: Les endpoints `forms/*.php` nécessitent un serveur supportant PHP. En mode fichier (sans serveur), les requêtes ne fonctionneront pas.

## Personnalisation
- Nom du site / logo:
  - Modifiez les éléments `.sitename` et le logo dans l’en-tête et le footer des pages (par ex. `index.html`, `privacy.html`).
- Couleurs / styles:
  - Éditez `assets/css/main.css` pour ajuster variables, couleurs, espacements.
- Contenu:
  - Page d’accueil: sections et ancres dans `index.html` (`#hero`, `#about`, `#menu`, etc.).
  - Politique de confidentialité: `privacy.html` (déjà localisée en FR).
  - Conditions d’utilisation: `terms.html`.
- Favicons:
  - Remplacez `assets/img/favicon.png` et `assets/img/apple-touch-icon.png`.

## Formulaires
- Newsletter (footer) envoie vers `forms/newsletter.php` et utilise `assets/vendor/php-email-form/validate.js`.
- Pour un envoi réel, implémentez la logique serveur dans `forms/newsletter.php` (validation, sécurité, envoi d’email) et déployez sur un hébergement avec PHP.

## Déploiement
- Dépôt statique: GitHub Pages, Netlify, Vercel (projets statiques), OVH, etc.
- Si vous utilisez des scripts PHP, déployez sur un hébergeur compatible (Apache/Nginx + PHP) ou servez la partie statique via CDN et les formulaires via une API/Function.

## Dépendances / Vendors
- Bootstrap 5.3.7, Bootstrap Icons
- AOS (animations), GLightbox, Isotope, ImagesLoaded
- Validation formulaire: `assets/vendor/php-email-form/validate.js`



## Pages légales
- Politique de confidentialité: `privacy.html`
- Conditions d’utilisation: `terms.html`

## Support
- Ouvrez une issue (si dépôt git) ou contactez l’équipe projet. Pour ajustements spécifiques (textes légaux, RGPD), fournissez les versions validées par votre conseil juridique.
