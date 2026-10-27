# aih-gare-du-temps-vr

Expérience de réalité virtuelle du futur musée **La Gare du Temps** (ancienne gare de Maransart, Lasne).
Première époque : **Plancenoit, 18 juin 1815**, l’arrivée des Prussiens, dans un style de gravure animée.

Projet AI Horizon — Axelion Group.

## État

- Version actuelle : **v0.1** (démo de 2 minutes, une seule scène).
- Contenu historique **provisoire** : relief, village et église sont des hypothèses de démonstration, à valider par le CGHL et un historien avant toute présentation publique.

## Lancer en local

La page doit être servie par un serveur (les modules ES ne se chargent pas en ouvrant le fichier directement) :

```bash
npx serve .
```

Puis ouvrir l’adresse indiquée dans un navigateur récent. Le mode VR n’est disponible qu’en HTTPS (voir ci-dessous).

## Tester dans le casque

1. Ouvrir l’adresse GitHub Pages du dépôt dans le navigateur du Meta Quest 3.
2. Attendre le chargement, puis appuyer sur « Enter VR ».
3. Si l’ancienne version s’affiche, ajouter `?v=<version>` à l’adresse.

## Structure

```
index.html                 page de la démo (v0.1 : tout le code est dans ce fichier)
vendor/three/              three.js 0.160.0 embarqué (licence MIT, voir vendor/three/LICENSE)
docs/CHANGELOG.md          journal des versions
.github/ISSUE_TEMPLATE/    modèle de retour de test dans le casque
```

L’arborescence cible à partir de la v0.2 (`src/engine`, `src/scenes`, `i18n`, `assets`) est décrite dans les spécifications techniques.

## Règles

- three.js reste en **0.160.0** sauf décision explicite.
- Aucun appel à un CDN : l’expérience doit fonctionner sans Internet au musée.
- Rien de confidentiel dans ce dépôt public : ni clé, ni mot de passe, ni données personnelles, ni documents internes.

## Documents de référence

- Spécifications — Expérience VR « Plancenoit, 18 juin 1815 » (partagé par Jérémie)
- Spécifications techniques — aih-gare-du-temps-vr (partagé par Jérémie)
