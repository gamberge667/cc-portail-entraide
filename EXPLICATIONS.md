# EXPLICATIONS

**Nom / Prénom :** Meylan Timée

## Commit de départ
`4a266e1`  premier commit de `main`.
Test initial : durée d'un créneau 200 min, 2 clics → 2 créneaux / 400 min, Recommencer → 0 / 0.

## Branches
- `feature/accueil`, `feature/contact` : créées depuis `main` au commit `76184a8`.
- `feature/tutorat` : fournie, partie du même `76184a8` (commit `a43f314`).
- `hotfix/duree` : créée depuis le `main` intégré (`6aae8ba`).

## Mes changements
- `7334c51` : paragraphe de permanence → accueil libre sans inscription le jeudi à 16 h.
- `c6085d2` : adresse de contact rendue cliquable (`mailto:`).
- `7da5d8d` : fusion de `feature/contact` dans `main` (`feature/accueil` avait avancé `main` en fast-forward).

## Conflit
Les branches ont divergé : accueil et tutorat sont parties de `76184a8` et ont modifié la même ligne (`<p id="permanence">`).
Décision : une seule phrase qui garde les deux informations (accueil libre sans inscription à 16 h, puis tutorat individuel sur inscription à 16 h 30), contact cliquable conservé.
Commit de fusion : `6aae8ba`, parents `7da5d8d` et `a43f314`. Vérifié : `grep` sans marqueur, `git status` propre.

## Annulation
- Commit annulé : `b88cc98` (durée portée de 20 à 200 min).
- Commit d'annulation : `335d2ba`, fait avec `git revert`, sans réécrire l'histoire. Le conseil du README (`76184a8`) est conservé.
- Fusionné dans `main` en fast-forward.

## Tests
| Test | Attendu | Observé |
|---|---|---|
| Avant : durée d'un créneau | 20 min | 200 min (erreur) |
| Après : durée d'un créneau | 20 min | 20 min |
| Après : 2 clics | 2 créneaux / 40 min | 2 créneaux / 40 min |
| Après : Recommencer | 0 / 0 | 0 / 0 |
| Permanences, contact, conseil README | présents | présents |

## Dernier identifiant de main
`335d2ba` avant ce fichier ; l'identifiant du commit d'EXPLICATIONS.md est dans mon message de remise. Identique sur GitHub : à vérifier.

## Aides utilisées
Aide IA (Claude) guidage point par point. J'ai fait les manipulations, commande et les tests moi-même et vérifié chaque résultat dans le terminal.
