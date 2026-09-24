# Theme Switcher

A responsive theme switcher built with HTML and CSS. The project demonstrates how to implement multiple visual themes using CSS custom properties without JavaScript.

## Overview

The application provides three selectable themes:

* Light
* Dark
* Custom

The selected theme updates the page background, text colors, controls, preview card, and other visual elements.

Theme switching is implemented entirely with HTML and CSS.

## Features

* Three visual themes: Light, Dark, and Custom
* CSS custom properties for centralized design tokens
* Theme-specific color palettes
* Accessible theme selection controls
* Keyboard focus styles
* Responsive layout for smaller screens
* Smooth visual transitions
* No JavaScript required

## Technologies

* HTML5
* CSS3
* CSS Custom Properties
* Vite

## Project Structure

```text
theme-switcher/
├── src/
│   └── styles/
│       └── main.css
├── index.html
├── package.json
├── package-lock.json
└── README.md
```

## Getting Started

### Prerequisites

* Node.js
* npm

### Installation

Clone the repository and install the dependencies:

```bash
npm install
```

### Development

Start the Vite development server:

```bash
npm run dev
```

The application will be available at the local URL provided by Vite.

### Production Build

Create a production build:

```bash
npm run build
```

### Preview Production Build

Preview the production build locally:

```bash
npm run preview
```

## Theme Implementation

The application uses CSS custom properties as design tokens.

The default theme values are defined in `:root`:

```css
:root {
  --color-page-background: #f4f5f7;
  --color-surface: #ffffff;
  --color-text: #1f2937;
  --color-text-muted: #6b7280;
  --color-border: #d1d5db;
  --color-accent: #2563eb;
}
```

Theme-specific values are applied to the main application container when the corresponding radio input is selected.

The Dark and Custom themes use the CSS `:has()` pseudo-class to update the custom properties inherited by the application:

```css
.theme-app:has(#theme-dark:checked) {
  --color-page-background: #111827;
  --color-surface: #1f2937;
}
```

This allows the same HTML structure to display different themes without duplicating the preview card or using JavaScript.

## Accessibility

The theme controls use radio inputs with associated labels.

The inputs are visually hidden but remain available to keyboard users. Focus states are provided for the theme controls, and the selected theme is visually indicated.

The page also uses semantic HTML elements such as:

* `main`
* `header`
* `section`
* `fieldset`
* `legend`
* `article`

## Responsive Design

The layout adapts to smaller screens using CSS media queries.

On narrow screens:

* Theme controls become a single-column layout.
* The preview card uses reduced padding.
* The main content maintains consistent horizontal spacing.

## Roadmap

This project was created as part of the [Theme Switcher](https://roadmap.sh/projects/theme-switcher) project from roadmap.sh.

## License

This project is for educational purposes.
