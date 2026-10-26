# École de poker

Application web pour apprendre le Texas Hold’em, en français, sans serveur ni dépendance.

- **Bases** : règles, déroulé d’une main, actions, position, formule de Chen, cote du pot, règle du 2 et 4.
- **Combinaisons** : les 10 mains, de la quinte flush royale à la hauteur, avec leur fréquence.
- **S’entraîner** : trois quiz (quelle main gagne, nomme ta combinaison, jouer ou se coucher), avec score et record.
- **Jouer** : partie en tête-à-tête contre un robot, avec un coach qui estime tes chances et note chaque décision.

Fonctionne sur ordinateur et sur téléphone (portrait et paysage), s’installe comme une application et reste utilisable hors ligne après la première visite. Les statistiques sont stockées dans le navigateur uniquement.

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | L’application complète (HTML, CSS et JavaScript) |
| `manifest.webmanifest` | Nom, couleurs et icônes pour l’installation sur téléphone |
| `sw.js` | Service worker : mise en cache pour le mode hors ligne |
| `icon.svg`, `icon-192.png`, `icon-512.png` | Icônes |

`index.html` fonctionne aussi seul en double-cliquant dessus ; l’installation et le hors-ligne demandent une adresse en `https://`.

## Mise en ligne avec GitHub Pages

1. Créer un dépôt et y déposer tous les fichiers à la racine.
2. *Settings → Pages → Build and deployment* : source **Deploy from a branch**, branche `main`, dossier `/ (root)`.
3. L’application est publiée à l’adresse `https://<compte>.github.io/<dépôt>/`.

Sur téléphone, ouvrir l’adresse puis « Ajouter à l’écran d’accueil ».

## Mettre à jour

Après une modification de `index.html`, augmenter le numéro de version dans `sw.js` (`ecole-poker-v2` → `v3`) pour que les téléphones récupèrent la nouvelle version.
