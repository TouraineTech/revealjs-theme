# reveal.js Theme Touraine Tech

Official [reveal.js](https://revealjs.com) theme for Touraine Tech presentations.

## Installation

### Via CDN (recommended)

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/revealjs-theme-touraine-tech@1/dist/touraine-tech.css">
```

The `@1` pins the major version: you get fixes and new features, never a breaking change.

### Via npm

```bash
npm install revealjs-theme-touraine-tech
```

```html
<link rel="stylesheet" href="node_modules/revealjs-theme-touraine-tech/dist/touraine-tech.css">
```

## Quick start

```html
<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8">
  <title>My talk - Touraine Tech</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@6.0.2/dist/reset.css">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@6.0.2/dist/reveal.css">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/revealjs-theme-touraine-tech@1/dist/touraine-tech.css">
</head>
<body>
  <div class="reveal">
    <div class="slides">
      <section class="cover">
        <h1>My talk title</h1>
        <p>Speaker name</p>
      </section>

      <section class="default">
        <h1>My content</h1>
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

The theme works with reveal.js 5 and 6. With reveal.js 6, plugins live under `dist/plugin/` (for example `reveal.js@6.0.2/dist/plugin/highlight.js`): see [`example.html`](./example.html) for a full deck with plugins.

## Layouts

Add the class to a `<section>`.

| Class | Description |
|-------|-------------|
| `cover` | Title slide, centered |
| `section` | Transition between sections, with decorative triangles |
| `default` | Content slide, title underlined in teal |
| `two-cols` | Two-column content |
| `end` | Closing / thank-you slide, with decorative triangles |

### `cover`

```html
<section class="cover">
  <h1>My talk title</h1>
  <p>Speaker name</p>
</section>
```

### `section`

```html
<section class="section">
  <h1>New section</h1>
  <p>Optional subtitle</p>
</section>
```

### `two-cols`

```html
<section class="two-cols">
  <div class="col">
    <h2>Left</h2>
    <ul>
      <li>Point A</li>
      <li>Point B</li>
    </ul>
  </div>
  <div class="col">
    <h2>Right</h2>
    <p>Text content</p>
  </div>
</section>
```

## Footer

A global footer shows the TNT logo at the bottom left, with the speaker's handle (X, Bluesky, LinkedIn…) next to it. Put it inside `<div class="reveal">`, but **outside** the slides:

```html
<div class="reveal">
  <div class="slides">
    <!-- Your slides -->
  </div>

  <div class="slide-footer">
    <div class="tnt-logo tnt-logo--inverted">
      <!-- TNT logo SVG -->
    </div>
    <span class="speaker-handle">@YourHandle</span>
  </div>
</div>
```

The footer is visible on every slide.

## TNT logo

The logo SVG is in [`assets/logo.svg`](./assets/logo.svg), and inline in [`example.html`](./example.html).

```html
<div class="tnt-logo tnt-logo--xl tnt-logo--inverted">
  <!-- Logo SVG -->
</div>
```

| Class | Width |
|-------|-------|
| `tnt-logo--sm` | 80px |
| `tnt-logo--md` | 150px |
| `tnt-logo--lg` | 250px |
| `tnt-logo--xl` | 400px |

Add `tnt-logo--inverted` on dark backgrounds (white logo).

## Colors

| Variable | Value | Usage |
|----------|-------|-------|
| `--tnt-primary` | `#222333` | Dark background |
| `--tnt-secondary` | `#6ABFAD` | Accents, links, decorations |
| `--tnt-white` | `#ffffff` | Text on dark background |

### Utility classes

```html
<div class="bg-tnt-primary">Dark background</div>
<div class="bg-tnt-secondary">Teal background</div>
<span class="text-tnt-primary">Dark text</span>
<span class="text-tnt-secondary">Teal text</span>
<span class="text-tnt-white">White text</span>

<p class="text-center">…</p>
<p class="text-left">…</p>
<p class="text-right">…</p>
```

## Typography

- **Font**: Noto Sans (Google Fonts)
- **Code**: Fira Code

Both are loaded from Google Fonts by the theme.

## Development

```bash
git clone https://github.com/TouraineTech/revealjs-theme
cd revealjs-theme

# Serve example.html
npm run serve
```

The theme is a single CSS file, [`dist/touraine-tech.css`](./dist/touraine-tech.css): there is no build step.

### Releasing

Record every change under `[Unreleased]` in the [CHANGELOG](./CHANGELOG.md). To release, open a PR that bumps `version` in `package.json` and renames the `[Unreleased]` section to that version: on merge, CI publishes to npm and creates the GitHub release with that changelog entry as notes. A PR without a version bump publishes nothing.

## License

MIT
