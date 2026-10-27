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


Étape 1 : Vérifier et créer/basculer sur la branche dev en local
Ouvre ton terminal dans VS Code et tape ces commandes une par une :

Bash
# 1. Voir sur quelle branche tu te trouves actuellement
git status

# 2. Créer la branche dev en local et basculer dessus (si ce n'est pas déjà fait)
git checkout -b dev

# (Si la commande du dessus te dit qu'elle existe déjà, fais simplement :)
git switch dev
Étape 2 : Préparer et envoyer le code sur origin/dev
Maintenant que tu es bien positionné sur ta branche dev locale avec tout ton code :

Bash
# 1. Ajouter tous tes fichiers modifiés ou créés à l'index
git add .

# 2. Enregistrer (valider) les modifications avec un message clair
git commit -m "feat: ajout de la structure initiale du site et des pages du TP SEO"

# 3. Pousser ta branche dev locale vers le dépôt distant GitHub pour la première fois
git push -u origin dev
(Le paramètre -u permet de lier ta branche locale dev à la branche distante dev sur GitHub. Pour les prochains envois, un simple git push suffira).

Étape 3 : Comment vos coéquipiers (Oméga, Afou, etc.) doivent récupérer et travailler sur le projet
Pour que les autres membres du groupe puissent cloner le projet sur leur machine, récupérer le code et travailler sur la branche dev, ils doivent exécuter ces commandes dans leur propre terminal VS Code :

Bash
# 1. Cloner le dépôt sur leur machine (en remplaçant par l'URL exacte du repo)
git clone https://github.com/jeremyferrierpro-create/TP_SEO_Afou_Omega_Jeremy.git

# 2. Entrer dans le dossier du projet
cd o_capitole_site

# 3. Basculer sur la branche dev (Git va automatiquement la lier à distance)
git checkout dev
# OU
git switch dev
Routine quotidienne de travail en équipe (pour éviter les conflits) :
Chaque fois qu'un membre du groupe commence à travailler ou veut envoyer son code :

Bash
# AVANT de commencer à coder (pour récupérer le travail des autres)
git pull origin dev

# FMODIFIER LE CODE DANS VS CODE...

# POUR ENVOYER SON TRAVAIL SUR DEV :
git add .
git commit -m "nom: description de ce qui a été fait"
git push origin dev


Étape 4 : La validation finale pour le formateur (fusion de dev vers main)
Quand le projet sera entièrement terminé, testé et validé par l'équipe, vous basculerez sur la branche main pour préparer la présentation au formateur :

Bash
# 1. Se placer sur la branche main
git checkout main
# OU
git switch main

# 2. Récupérer la dernière version de main
git pull origin main

# 3. Fusionner tout le travail validé de la branche dev dans main
git merge dev

# 4. Envoyer la branche main mise à jour sur GitHub
git push origin main
C'est cette branche main propre et complète que vous pourrez présenter au formateur le jour J !
