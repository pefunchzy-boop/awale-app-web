# Awalé

Appli web d'awalé (2 joueurs, bot, en ligne) — un seul dossier statique, aucun serveur requis.

## Déployer sur GitHub Pages

1. Va sur **github.com**, connecte-toi, clique **New repository**. Donne-lui un nom (ex. `awale`), laisse-le public, ne coche aucune case d'initialisation, clique **Create repository**.
2. Sur la page du repo vide, clique **uploading an existing file**, puis glisse-dépose **tout le contenu de ce dossier** (`index.html`, `manifest.json`, `sw.js`, le dossier `icons/`) — pas le dossier lui-même, son contenu. Valide (**Commit changes**).
3. Va dans l'onglet **Settings** du repo → section **Pages** (menu de gauche) → sous **Build and deployment**, choisis **Branch: main**, dossier **/ (root)** → **Save**.
4. Attends 1-2 minutes, rafraîchis la page : l'URL apparaît en haut, du style `https://TON-PSEUDO.github.io/awale/`.

C'est en ligne. Chaque fois que tu modifies un fichier et le re-uploades (ou push via git), le site se met à jour automatiquement en 1-2 minutes.

## Ajouter à l'écran d'accueil (iPhone / Safari)

1. Ouvre l'URL du site dans **Safari** (pas Chrome — l'ajout à l'écran d'accueil avec icône ne marche bien que depuis Safari sur iOS).
2. Bouton **Partager** (le carré avec la flèche vers le haut) → **Sur l'écran d'accueil**.
3. L'icône du plateau apparaît, et l'appli s'ouvre en plein écran (sans barre d'adresse Safari) comme une vraie appli.

Android/Chrome : menu **⋮** → **Ajouter à l'écran d'accueil** (ou une bannière d'installation apparaît automatiquement après quelques visites).

## Mode en ligne (Firebase)

Le mode "en ligne" (2 appareils) a besoin d'un petit projet Firebase gratuit — l'appli explique les étapes directement dans son propre menu ("🌐 En ligne" → "Comment faire →"). Rien à configurer ici, c'est fait une fois depuis le téléphone, la config est sauvegardée dans le navigateur.

## Structure du dossier

```
index.html          l'appli (tout est dedans : moteur de jeu, bot, UI)
manifest.json        métadonnées pour l'installation en appli
sw.js                 service worker (cache hors-ligne pour les modes local/bot)
icons/
  icon-192.png        icône Android/Chrome
  icon-512.png        icône Android/Chrome (haute résolution)
  apple-touch-icon.png icône iOS (écran d'accueil)
  favicon-16.png        favicon (onglet navigateur)
  favicon-32.png        favicon (onglet navigateur)
```
