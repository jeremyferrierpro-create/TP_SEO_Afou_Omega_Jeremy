# Ô Capitole — maquette de site vitrine

## Contenu
- `index.html` : landing page
- `conseils.html` : index éditorial / blog
- `recette-cassoulet.html` : article recette
- `producteurs-locaux.html` : article conseil sur le circuit court
- `mentions-legales.html` : modèle à compléter
- `assets/style.css` : design responsive
- `assets/main.js` : menu mobile

## Lancer en local
Ouvrir `index.html` dans un navigateur. Pour un comportement plus proche d'un hébergement, lancer un serveur HTTP local depuis ce dossier, par exemple :
`python -m http.server 8000`
Puis ouvrir `http://localhost:8000`.

## Images
Les images de démonstration sont chargées depuis Unsplash avec des paramètres `fm=webp`, `auto=format` et des largeurs adaptées. Elles nécessitent une connexion Internet et ne sont pas des fichiers locaux. Pour une mise en production robuste, télécharger des images dont les droits sont vérifiés, générer des variantes WebP locales (hero, cartes, articles), renseigner `width`/`height`, et conserver un texte alternatif utile.

## À vérifier avant mise en ligne
- Confirmer que le restaurant existe bien à l'adresse indiquée et que le nom commercial peut être utilisé.
- Remplacer l'e-mail `.example`, ajouter téléphone, horaires, lien de réservation et informations légales réelles.
- Vérifier les spécialités, prix, disponibilité des plats, origine et engagements fournisseurs.
- Ne pas publier « 100 % local » ou « moins de 100 km » sans justificatifs opérationnels.
- Ajouter une vraie carte et les informations allergènes validées par le restaurant.
- Vérifier les droits des images, les performances, l'accessibilité et le référencement avec des outils réels.

## Statut
Maquette statique HTML/CSS/JS. Pas de backend, réservation en ligne, CMS, base de données, analytics ni formulaire de réservation connecté.
