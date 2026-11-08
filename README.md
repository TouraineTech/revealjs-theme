# Touraine Tech - Theme reveal.js

Theme reveal.js officiel pour les conférences Touraine Tech.

![Preview](https://touraine.tech/images/revealjs-theme-preview.png)

## Installation

### Via CDN (recommandé)

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/revealjs-theme-touraine-tech/dist/touraine-tech.css">
```

### Via npm

```bash
npm install revealjs-theme-touraine-tech
```

```html
<link rel="stylesheet" href="node_modules/revealjs-theme-touraine-tech/dist/touraine-tech.css">
```

## Utilisation rapide

```html
<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8">
  <title>Ma présentation - Touraine Tech</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@6.0.2/dist/reset.css">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@6.0.2/dist/reveal.css">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/revealjs-theme-touraine-tech/dist/touraine-tech.css">
</head>
<body>
  <div class="reveal">
    <div class="slides">
      <section class="cover">
        <h1>Titre de ma présentation</h1>
        <p>Mon nom</p>
      </section>

      <section>
        <h1>Mon contenu</h1>
        <ul>
          <li>Point 1</li>
          <li>Point 2</li>
        </ul>
      </section>

      <section class="end">
        <h1>Merci !</h1>
        <p>Des questions ?</p>
      </section>
    </div>
  </div>
  <script src="https://cdn.jsdelivr.net/npm/reveal.js@6.0.2/dist/reveal.js"></script>
  <script>Reveal.initialize();</script>
</body>
</html>
```

## Layouts disponibles

| Classe | Description |
|--------|-------------|
| `cover` | Slide de titre avec logo centré |
| `section` | Slide de transition (avec triangles décoratifs) |
| `default` | Slide de contenu (titre avec bordure turquoise) |
| `end` | Slide de fin "Merci !" |
| `two-cols` | Layout à deux colonnes |

### Slide cover

```html
<section class="cover">
  <h1>Titre de la présentation</h1>
  <p>Nom du speaker</p>
</section>
```

### Slide section

```html
<section class="section">
  <h1>Nouvelle partie</h1>
  <p>Description optionnelle</p>
</section>
```

### Slide deux colonnes

```html
<section class="two-cols">
  <div class="col">
    <h2>Gauche</h2>
    <ul>
      <li>Point A</li>
      <li>Point B</li>
    </ul>
  </div>
  <div class="col">
    <h2>Droite</h2>
    <p>Contenu texte</p>
  </div>
</section>
```

## Footer (Logo + handle du speaker)

Ajoutez un footer global avec le logo TNT et votre handle (X, Bluesky, LinkedIn…). Placez-le dans le `<div class="reveal">` mais **en dehors** des slides :

```html
<div class="reveal">
  <div class="slides">
    <!-- Vos slides ici -->
  </div>

  <!-- Footer global -->
  <div class="slide-footer">
    <div class="tnt-logo tnt-logo--inverted">
      <!-- SVG du logo TNT -->
    </div>
    <span class="speaker-handle">@VotreHandle</span>
  </div>
</div>
```

Le footer affiche :
- **Logo TNT** en bas à gauche
- **Handle du speaker** à droite du logo

Le footer est visible sur toutes les slides.

## Couleurs

| Variable CSS | Valeur | Usage |
|--------------|--------|-------|
| `--tnt-primary` | `#222333` | Bleu foncé (fond) |
| `--tnt-secondary` | `#6ABFAD` | Turquoise (accents) |
| `--tnt-white` | `#ffffff` | Blanc |

## Classes utilitaires

```html
<!-- Couleurs de fond -->
<div class="bg-tnt-primary">...</div>
<div class="bg-tnt-secondary">...</div>

<!-- Couleurs de texte -->
<span class="text-tnt-primary">...</span>
<span class="text-tnt-secondary">...</span>
<span class="text-tnt-white">...</span>

<!-- Alignement -->
<p class="text-center">...</p>
<p class="text-left">...</p>
<p class="text-right">...</p>
```

## Logo TNT

Le logo est inclus en SVG avec plusieurs tailles :

```html
<div class="tnt-logo tnt-logo--xl tnt-logo--inverted">
  <!-- SVG du logo -->
</div>
```

| Classe | Largeur |
|--------|---------|
| `tnt-logo--sm` | 80px |
| `tnt-logo--md` | 150px |
| `tnt-logo--lg` | 250px |
| `tnt-logo--xl` | 400px |

Ajoutez `tnt-logo--inverted` pour les fonds foncés (logo blanc).

## Polices

Le thème utilise :
- **Noto Sans** pour le texte
- **Fira Code** pour le code

Elles sont chargées automatiquement via Google Fonts.

## Liens

- [Touraine Tech](https://touraine.tech)
- [reveal.js Documentation](https://revealjs.com)
- [Exemple en ligne](https://touraine.tech/themes/revealjs/example.html)

## Licence

MIT - Touraine Tech
