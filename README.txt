# Stremio Liquid Glass — pack complet

Cette version est une **interface web indépendante (PWA)** inspirée de Stremio et du style Liquid Glass. Elle n'est ni l'application officielle Stremio, ni affiliée à Stremio.

## Contenu
- `index.html` — interface, catalogues, recherche et fiches interactives.
- `manifest.webmanifest` — configuration PWA.
- `sw.js` — cache de l'interface (version renouvelée v4).
- `icon-192.png` et `icon-512.png` — icônes.
- `README.txt` — guide d'installation.

## Mise en ligne sur GitHub Pages
1. Décompresse le ZIP.
2. Dans ton dépôt `stremio-liquid-glass`, remplace les anciens fichiers par **tous** les fichiers de ce pack.
3. Conserve les icônes avec exactement leurs noms.
4. Fais un commit sur la branche publiée par GitHub Pages et attends la fin du déploiement.
5. Ouvre le site en HTTPS dans Safari sur l'iPad et recharge la page.
6. Si l'ancienne version reste affichée dans la PWA, ferme-la complètement puis rouvre-la.
7. Pour installer : Safari → Partager → Sur l'écran d'accueil.

## Utilisation
1. Ouvre **Addons** et ajoute l'URL HTTPS d'un manifeste public Stremio.
2. Appuie sur **Actualiser**.
3. Ouvre Films, Séries ou Recherche.
4. Touche une affiche pour ouvrir sa fiche détaillée.

## Limites importantes
- Le catalogue n'est pas préchargé : il faut ajouter un addon de catalogue compatible (par exemple Cinemeta si son manifeste est accessible depuis le navigateur).
- Les serveurs d'addons doivent autoriser les requêtes navigateur (CORS). Les addons avec authentification, jetons ou routes spéciales peuvent ne pas fonctionner.
- Cinemeta fournit des métadonnées et affiches, pas les flux vidéo.
- Les sources torrent et certains flux externes nécessitent l'application Stremio. La lecture intégrée ne fonctionne que pour des URL vidéo HTTP(S) compatibles avec le navigateur et ses codecs.
- Le bouton **Ouvrir dans Stremio** tente de lancer l'application via son lien profond ; le comportement dépend de l'installation de Stremio et d'iPadOS.
- Cette PWA ne se connecte pas au compte Stremio et ne synchronise ni bibliothèque, ni favoris, ni progression.
- N'ajoute jamais de mot de passe, jeton ou identifiant privé dans cette interface.

## Dépannage
- **Catalogue vide :** vérifie le manifeste, CORS et la présence de catalogues dans le manifeste.
- **Fiche sans sources :** l'addon de catalogue ne fournit pas forcément de flux. Il faut un addon qui annonce la ressource `stream`.
- **Ancienne version sur iPad :** ferme et rouvre la PWA après le déploiement. Le cache a été renouvelé en v4.

Le pack corrige les clics sur les affiches, l'ouverture des fiches, l'accès clavier, la gestion d'un stockage local illisible et le cache de l'interface. Ce n'est pas un client Stremio complet.
