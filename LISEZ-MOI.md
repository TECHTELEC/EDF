# État de frais — installation sur smartphone

Version 2.0

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `index.html` | Le formulaire complet. Fonctionne seul, sans réseau. |
| `manifest.webmanifest` | Nom, icône et mode plein écran de l'application. |
| `sw.js` | Mise en cache pour l'usage hors connexion. |
| `icone-192.png`, `icone-512.png` | Icônes de l'application. |

## Ce qu'il faut faire

Déposer les cinq fichiers **ensemble, dans un même dossier**, à une adresse en `https://`
(SharePoint, serveur interne, ou tout hébergement web). Ouvrir ensuite `index.html`
depuis cette adresse sur le téléphone.

L'adresse doit commencer par `https://`. C'est une règle des navigateurs : un fichier
ouvert depuis la mémoire du téléphone ne peut pas être installé, quel que soit le réglage.

## Installation sur le téléphone

**Android** — Chrome propose « Installer l'application » dans son menu, ou le bouton
« Installer » en haut de la page le fait directement.

**iPhone / iPad** — Menu Partager (le carré avec une flèche), puis « Sur l'écran d'accueil ».
Disponible dans Safari, Chrome, Edge et Firefox depuis iOS 16.4.

## Mise à jour

Remplacer `index.html`, puis incrémenter `CACHE` dans `sw.js` (`edf-v2-0` → `edf-v2-1`).
Sans cela, les téléphones conserveront la version en cache.

## Si l'hébergement n'est pas possible

`index.html` seul reste pleinement utilisable dans le navigateur du téléphone, saisie,
PDF et envoi compris. Seul le raccourci sur l'écran d'accueil manquera.
