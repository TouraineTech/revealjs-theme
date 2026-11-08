# Changelog

Toutes les évolutions notables du thème sont listées ici.

Le format suit [Keep a Changelog](https://keepachangelog.com/fr/1.1.0/) et le projet respecte le [Semantic Versioning](https://semver.org/lang/fr/).

## [Unreleased]

## [1.1.0] - 2026-11-08

### Ajouté

- Compatibilité avec reveal.js 6. Le thème fonctionne toujours avec reveal.js 5.
- Publication automatique sur npm depuis la CI, avec attestation de provenance.

### Corrigé

- La slide `end` ne sort plus de l'écran quand elle suit une slide `section`.
- Les titres des slides `section` passent devant les triangles décoratifs.
- La documentation du footer : la classe `.slide-footer.light` n'existe pas et le handle s'affiche à droite du logo.

### Modifié

- L'exemple et le README chargent reveal.js 6.0.2, dont les plugins sont maintenant sous `dist/plugin/`.
- Le handle Touraine Tech de l'exemple devient `@tourainetech`.

## [1.0.0] - 2025-12-23

### Ajouté

- Première version du thème : layouts `cover`, `section`, `default`, `end` et `two-cols`, footer avec logo et handle, logo TNT en SVG, classes utilitaires.

[Unreleased]: https://github.com/TouraineTech/revealjs-theme/compare/v1.1.0...HEAD
[1.1.0]: https://github.com/TouraineTech/revealjs-theme/compare/7499cb3...v1.1.0
[1.0.0]: https://github.com/TouraineTech/revealjs-theme/commit/7499cb3
