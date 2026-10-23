# 6 qui prend ! — pour le hub ChadGangGames

Le jeu tient dans **un seul fichier `index.html`** (HTML/CSS/JS, aucun serveur, aucune compilation).

## Fichiers
- `index.html` : le jeu complet
- `chadgang.json` : la fiche du jeu dans le hub
- `cover.png` : l'image de couverture (1280×720)

## Ce que fait le jeu
- **En ligne** via le SDK du hub (`ChadGang.join`) : on crée une salle (code de 4 lettres) ou on la rejoint. Si on arrive par une invitation (`?room=CODE`), on entre directement dans la salle.
- **Bots** : l'hôte peut compléter la table jusqu'à 10 joueurs (niveau Facile ou Malin).
- **Solo** contre les bots, y compris hors du hub. La partie solo est sauvegardée et peut être reprise.
- **Réglages de l'hôte** : fin de partie à 33, 66 ou 100 têtes ; temps par tour illimité, 20 s ou 40 s ; niveau des bots.
- **Robuste** : si l'hôte part, le joueur suivant reprend la partie. Un joueur absent est joué par un bot, et il reprend la main à son retour (rechargement de la page compris).
- **Effets** : cartes qui volent, rangées qui explosent, tremblements d'écran proportionnels aux dégâts, bannières (« 6 QUI PREND ! », « CARNAGE ! », « APOCALYPSE BOVINE ! »), pluie de vaches, confettis, sons synthétisés (meuh compris) avec bouton pour couper, réactions emoji, historique des coups, classement en direct.

## Mettre en ligne
```bash
git init
git add .
git commit -m "6 qui prend !"
git branch -M main
git remote add origin https://github.com/<ton-compte>/jeu-6-qui-prend.git
git push -u origin main
```
Puis dans le hub : **Admin → Jeux → Ajouter le jeu**, et colle le lien du dépôt.

## Tester en local
Ouvre `index.html` dans un navigateur : le mode solo marche sans le hub.
Astuce de test : ajoute `?speed=4` à l'adresse pour accélérer les animations.
