# Fennec Run : version installable (PWA)

Ce dossier contient le jeu complet, prêt à être mis en ligne. Il fonctionne hors connexion une fois ouvert une première fois. Le jeu existe en français et en anglais (bouton FR/EN, langue du téléphone par défaut).

| Fichier | Rôle |
| --- | --- |
| `index.html` | Le jeu (polices intégrées, aucune dépendance externe) |
| `manifest.webmanifest` | Nom, icônes, plein écran, mode paysage |
| `sw.js` | Cache hors ligne |
| `apple-touch-icon.png`, `icon-*.png` | Icônes de l'écran d'accueil |

## Mettre en ligne (HTTPS obligatoire pour le mode hors ligne)

**GitHub Pages (gratuit)**
1. Crée un dépôt public `fennec-run` sur le compte robin57, et dépose tous les fichiers de ce dossier à la racine (« uploading an existing file »).
2. Settings → Pages → Source : Deploy from a branch, branche `main`, dossier `/ (root)`.
3. Le jeu est servi sur `https://robin57.github.io/fennec-run/`.

**itch.io**
1. Nouveau projet → Kind of project : HTML.
2. Envoie un zip de ce dossier et coche « This file will be played in the browser ».
3. Sur itch.io, le jeu tourne dans un cadre : l'installation sur l'écran d'accueil et le hors ligne y sont moins fiables. GitHub Pages est préférable pour la version iPhone.

## Installer sur iPhone
1. Ouvre l'adresse du jeu dans **Safari**.
2. Bouton Partager → **Sur l'écran d'accueil** → Ajouter.
3. Lance le jeu depuis l'icône : il s'ouvre en plein écran, sans barre Safari. Tourne le téléphone en paysage.

## À savoir
- La progression est enregistrée au début de chaque niveau, sur l'appareil. Effacer les données de Safari l'efface aussi.
- iOS ne permet pas de bloquer l'orientation d'une web app : le jeu affiche un message en mode portrait.
- Pour publier une mise à jour, remplace les fichiers : `sw.js` change de version à chaque nouvelle construction, et les joueurs reçoivent la nouvelle version au lancement suivant.
