# OU MODIFIER MON PORTFOLIO — GUIDE RAPIDE

Ouvre le dossier dans **Visual Studio Code**. Tu peux utiliser l’extension Live Server, ou ouvrir `index.html` directement.

## 1. Modifier tes informations

- Page d’accueil et boutons : `index.html`.
- Présentation, formation, parcours : `a-propos.html`.
- CV : remplace `assets/documents/CV_2026-10-05_Ilan_Breton.pdf` par un nouveau PDF **avec exactement le même nom**, ou change le lien dans les pages concernées.
- Rapport de stage : remplace `assets/documents/RAPPORT-DE-STAGE.pdf` ou adapte les liens.
- Contact : `contact.html` et l’adresse utilisée dans `assets/js/main.js`.

## 2. Personnaliser les thèmes

Dans `assets/css/style.css` :

```css
:root { --bg: #090f1b; --surface:#111c2f; --text:#f3f7ff; --accent:#70f0d0; }
:root[data-theme="light"] { --bg: #f5f8fc; --surface:#ffffff; --text:#14243a; --accent:#087b79; }
```

Le bouton est dans l’en-tête de chaque `.html`. Son comportement est dans `assets/js/main.js`. Le thème choisi est sauvegardé localement dans le navigateur.

## 3. Modifier des projets scolaires

- Grille de tous les projets, tags, années et filtres : `projets.html`.
- 1re année : `projet-active-directory.html`, `projet-ipv4.html`, `projet-bootstrap.html`, `projet-sql.html`.
- 2e année : `projet-pfsense.html` et `projet-topologie.html`.
- Stage 1re année : `projet-forticlient.html`, `projet-powershell.html`, `projet-kace.html`, `projet-maintenance.html`, `projet-support.html`.

Pour modifier un texte, ouvre le fichier et cherche son titre avec **Ctrl+F**, remplace la phrase puis fais **Ctrl+S**. 

Pour ajouter une réalisation : duplique l’une des pages `projet-*.html`, change son titre, son corps et sa description, puis ajoute une carte avec un lien vers cette nouvelle page dans `projets.html`.

⚠️ Les projets scolaires non accompagnés de sujets/captures restent volontairement généraux : ajoute le nom exact du TP, les étapes faites, les résultats testés et des captures personnelles avant de les présenter comme des dossiers techniques définitifs.

## 4. Modifier les images

Les photos extraites du rapport sont dans `assets/img/stage/`. Les légendes et liens sont codés dans `stage.html`.

Pour remplacer une photo, copie un nouveau `.webp` à la même place et sous le même nom. Pour ajouter une photo, copie ce modèle dans la galerie `stage.html` :

```html
<figure class="gallery-card evidence-photo">
  <a class="gallery-image" href="assets/img/stage/ma-photo.webp" target="_blank" rel="noopener">
    <img src="assets/img/stage/ma-photo.webp" alt="Description de la photo" loading="lazy">
  </a>
  <figcaption>La légende de ma photo</figcaption>
</figure>
```

## 5. Documents

- `documents.html` contient les liens de téléchargement.
- `stage.html` contient le bouton rapport.
- `a-propos.html` et `index.html` contiennent des liens vers le CV.
- Ne supprime pas le dossier `assets/documents/` quand tu publies.

## 6. Mettre le site sur Internet

Tu peux utiliser GitHub Pages ou Netlify. Déploie tout le dossier et conserve l’arborescence. **Attention : ne publie pas le CV ou le rapport avec leurs données personnelles et internes sans les avoir revus.**

## 7. Vérification avant d’envoyer le portfolio à un recruteur / jury

- Essayer chaque lien interne et les 2 PDF.
- Vérifier les menus mobile et le bouton clair/sombre.
- Ajouter des preuves personnelles pour tes ateliers de cours (captures, consignes, scripts, schémas).
- Corriger les fiches dont l’intitulé ou l’année diffèrent de tes travaux.
- Vérifier l’accord de diffusion de toute photo ou donnée d’Euralis.
