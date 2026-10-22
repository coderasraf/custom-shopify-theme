# Custom Dawn Shopify Theme

A Shopify Online Store 2.0 theme based on Shopify's Dawn (v15.1.0), extended with a Laravel Mix build pipeline for Tailwind CSS and Alpine.js so custom sections can be styled with utility classes.

![Shopify](https://img.shields.io/badge/Shopify-Dawn%2015.1-7AB55C?logo=shopify&logoColor=white) ![Liquid](https://img.shields.io/badge/Liquid-Templates-2C3E50) ![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-3.4-06B6D4?logo=tailwindcss&logoColor=white) ![Alpine.js](https://img.shields.io/badge/Alpine.js-3-8BC0D0?logo=alpinedotjs&logoColor=white)

## Overview

A starter theme for custom Shopify builds. It keeps Dawn's sections, snippets and templates intact and adds a front-end toolchain on top: Tailwind CSS is compiled from `src/scss/app.scss` and Alpine.js from `src/js/app.js` into the theme's `assets/` folder.

## Features

- All standard Dawn 15.1.0 Online Store 2.0 features: JSON templates, sections everywhere, header/footer section groups, cart drawer, predictive search, faceted filtering, quick order list, product media gallery and swatches
- Tailwind CSS 3 configured to scan `layout/`, `sections/`, `snippets/`, `templates/` and `config/` for classes
- Alpine.js 3 bundled and exposed as `window.Alpine` for lightweight interactivity
- Laravel Mix (webpack) build that outputs `assets/app.css` and `assets/app.js`
- `app.css` loaded globally from `layout/theme.liquid`
- Theme Check config (`.theme-check.yml`) and Prettier config included

## Tech Stack

- Shopify Liquid, Dawn 15.1.0
- Tailwind CSS 3, Sass
- Alpine.js 3
- Laravel Mix 6 (webpack)

## Getting Started

**Prerequisites:** Node.js, [Shopify CLI](https://shopify.dev/docs/api/shopify-cli), and a Shopify store or development store.

```bash
git clone https://github.com/coderasraf/custom-shopify-theme.git
cd custom-shopify-theme
npm install

# Build Tailwind/Alpine assets into assets/
npx mix            # or: npx mix watch

# Preview the theme on your store
shopify theme dev --store your-store.myshopify.com
```

To publish, push the theme with `shopify theme push` or connect the repository through Shopify's GitHub integration.

## Project Structure

```text
custom-shopify-theme/
├── assets/            # Dawn assets + compiled app.css / app.js
├── config/            # settings_schema.json, settings_data.json
├── layout/            # theme.liquid, password.liquid
├── locales/           # Translations
├── sections/          # Dawn sections and section groups
├── snippets/          # Reusable Liquid snippets
├── templates/         # JSON templates (incl. customers/)
├── src/
│   ├── js/app.js      # Alpine.js entry
│   └── scss/app.scss  # Tailwind entry
├── tailwind.config.js
└── webpack.mix.js
```

## License

Based on Shopify's Dawn theme. See [LICENSE.md](LICENSE.md) for Shopify's license terms.

## Author

Built by **Ashraf Siddik**, Shopify developer & CRO specialist.

- Website: [ashraf-siddik.com](https://ashraf-siddik.com)
- GitHub: [@coderasraf](https://github.com/coderasraf)
