🇫🇷 Français · [🇬🇧 English](L-H3-contexte-memoire.en.md)

# L-H3 — Contexte & mémoire de mes agents

## Étapes
1. Auditer `HOMELAB/CLAUDE.md`, `~/.claude/CLAUDE.md` et la mémoire auto : pour chaque ligne, se demander si elle est utile à chaque session, à la demande seulement (à déplacer dans une skill), ou jamais (à supprimer).
2. Mesurer RTK : la même session type (diagnostic Flux) avec et sans proxy, en comparant tokens consommés et résultat.
3. Tester la compaction contre un reset avec fichier de progression, sur une tâche longue.
4. Réécouter [IFTTD #383](https://www.ifttd.io/episodes/contexte-engineering) et confronter ses recommandations à ton setup, par écrit.

## Livrable
CLAUDE.md allégé (diff), mesure RTK, fiche de lecture IFTTD dans `notes/`.
