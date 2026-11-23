# AGENTS.md — osmrides_website

Dépôt de le site d'accueil d'OSMrides : présentation du projet, liens vers les jeux (parcs, stations), concepts (OSM comme référence, commande par zones, éditeur), comment contribuer (éditer OSM, éditeur local).
Fait partie d'OSMrides (simulations d'exploitation sur données OpenStreetMap, jeu de fan non officiel, interface en français). Organisation des quatre dépôts et règles communes : `docs/ORGANISATION.md` du dépôt `qhess34/osmrides` (à lire une fois).

## Responsable : Webmestre

Session longue lancée par le propriétaire ; mémoire et reprise : `docs/PILOTAGE.md`. Le chef code peu : il lit les issues, découpe, délègue à un sous-agent (`.claude/agents/`), vérifie, publie sur `main`, rend compte au propriétaire en français court (fait, testé, non testé, estimé).

## Règles du propriétaire

- Réalisme : rendu crédible, couleurs sourdes, aucun pictogramme ni emoji, rien d'enfantin.
- OSM est la référence ; tout ce qui est estimé est signalé dans le code et dit au propriétaire.
- Code lisible, KISS ; aucune dépendance, tout marche en ouvrant le fichier (`file://`), sans `fetch` ni modules ES.
- Le moteur (`engine/`) est une **copie figée** d'une version d'`osmrides` : ne jamais la modifier ici ; un besoin = issue `inter-equipe` dans `qhess34/osmrides`.
- Git : branche `main`, commits directs, messages en anglais à l'impératif.

## Tests

pages ouvertes sans erreur dans Chromium (Playwright), liens vers les jeux valides, lecture sur téléphone (390 px) ; relever les erreurs de page. Captures seulement pour un point visuel (une petite, ≈ 600×450, JPEG ≈ 70, regardée une fois).

## Économie de tokens

- Lire : ce fichier, `docs/PILOTAGE.md`, les issues ouvertes. Le reste par l'`explorateur` (Haiku).
- Un sous-agent par tâche, consigne autonome (réponses du propriétaire recopiées), rapport ≤ 8 lignes. Modèle : Haiku (recherche, tests), Sonnet (travail courant), Opus seulement sur demande du propriétaire.
- Ne jamais lire en entier un fichier de données généré (`*.data.js`).
