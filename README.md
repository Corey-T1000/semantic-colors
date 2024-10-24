# Semantic Color System

A comprehensive color system designed for accessibility and visual hierarchy, featuring both light and dark modes.

## Features

- **WCAG Compliant**: All color combinations meet or exceed WCAG 2.1 standards
- **Dark Mode Support**: Complete dark mode implementation with balanced contrast
- **Semantic Tokens**: Purpose-based color assignments for consistent UI development
- **Visual Hierarchy**: Carefully calibrated contrast ratios for clear information hierarchy

## Color Tokens

### Base Colors

Each color palette includes variants from 025 to 975:

- **Stone**: `stone-025` to `stone-975` - Neutral colors for UI elements
- **Red**: `red-025` to `red-975` - Error and destructive actions
- **Sand**: `sand-025` to `sand-975` - Warning states
- **Teal**: `teal-025` to `teal-975` - Success states
- **Violet**: `violet-025` to `violet-975` - Creative elements
- **Magenta**: `magenta-025` to `magenta-975` - Additional accent palette

### Semantic Tokens

#### Light Mode

| Token      | Background | Foreground | Contrast Ratio | WCAG Level |
| ---------- | ---------- | ---------- | -------------- | ---------- |
| Background | stone-025  | stone-975  | 18.82:1        | AAA        |
| Primary    | stone-900  | stone-025  | 17.99:1        | AAA        |
| Secondary  | stone-200  | stone-975  | 11.46:1        | AAA        |
| Muted      | stone-200  | stone-800  | 8.21:1         | AAA        |
| Success    | teal-200   | teal-800   | 8.73:1         | AAA        |
| Warning    | sand-200   | sand-800   | 8.61:1         | AAA        |
| Error      | red-300    | red-800    | 5.85:1         | AA         |
| Creative   | violet-300 | violet-800 | 7.48:1         | AAA        |

#### Dark Mode

| Token      | Background | Foreground | Contrast Ratio | WCAG Level |
| ---------- | ---------- | ---------- | -------------- | ---------- |
| Background | stone-975  | stone-025  | 18.82:1        | AAA        |
| Primary    | stone-025  | stone-975  | 18.82:1        | AAA        |
| Secondary  | stone-800  | stone-025  | 14.85:1        | AAA        |
| Muted      | stone-800  | stone-300  | 6.39:1         | AA         |
| Success    | teal-900   | teal-200   | 12.83:1        | AAA        |
| Warning    | sand-900   | sand-200   | 11.43:1        | AAA        |
| Error      | red-900    | red-200    | 13.17:1        | AAA        |
| Creative   | violet-900 | violet-200 | 13.57:1        | AAA        |

## Usage

1. Import the color system:

```css
@import "styles/globals.css";
```

2. Use semantic tokens in your CSS:

```css
.element {
  background: var(--background);
  color: var(--foreground);
}

.button-primary {
  background: var(--primary);
  color: var(--primary-foreground);
}
```

3. Use specific color tokens:

```css
.custom-element {
  /* Using specific color tokens */
  background: var(--teal-200);
  color: var(--teal-800);
}
```

4. Dark mode is automatically applied with the `.dark` class:

```html
<html class="dark">
  <!-- Content will use dark mode colors -->
</html>
```

## Preview

Open `preview.html` in a browser to see:

- All color combinations with their contrast ratios
- Color token names (e.g., stone-025, teal-200)
- HSL values for each color
- WCAG compliance ratings

## Accessibility Standards

- **AAA Level** (7:1+): Most color pairs exceed this highest level
- **AA Level** (4.5:1+): All color pairs meet at least AA standard
- **Large Text**: All combinations are suitable for large text (3:1+)

## Additional Features

- **Chart Colors**: 15 distinct colors for data visualization
- **Border Colors**: Consistent border styling
- **Ring Colors**: Focus state highlighting
- **Radius Tokens**: Consistent border radius scaling

## Development

To run the preview locally:

```bash
npm run preview
```

## Integration with Tailwind CSS

The color system is fully compatible with Tailwind CSS through the included `tailwind.config.js`. All color tokens are available as Tailwind classes:

```html
<div class="bg-background text-foreground">
  <button class="bg-primary text-primary-foreground">Primary Button</button>
</div>
```
