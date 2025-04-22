# Shopify Theme Boilerplate

[![Build status](https://img.shields.io/badge/build-passing-success)]()  
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?color=informational)]()

A modern, high-performance Shopify theme boilerplate based on the Dawn theme. This project is designed for maintainable and scalable Shopify theme development with:

- **Dawn as base** — latest Shopify Online Store 2.0 features
- **Vite** — optimized JS/CSS bundling with fast build times
- **Tailwind CSS** — utility-first styling
- **Vue.js (or Vanilla/Alpine options)** — optional reactive components
- **GSAP** — smooth animations
- **pnpm** — fast dependency management
- **shopify.theme.toml** — environment configuration
- **CSS/JS optimization** — production-ready builds

---

## 📁 Directory Structure

```
src/
  js/
    global.js
    components/
      example.js → becomes assets/example.js

  styles/
    base.css
    components/
      button.css → becomes assets/component-button.css
    sections/
      hero.css → becomes assets/section-hero.css
    templates/
      product.css → becomes assets/template-product.css
    helpers/
      forms.css → becomes assets/forms.css
```

---

## 🚀 Getting Started

### 1. Clone & Install

```bash
pnpm install
```

### 2. Configure Shopify Environment

Edit `shopify.theme.toml`:

```toml
[environments.env]
theme = "your-theme-id"
store = "your-store.myshopify.com"
password = "your-admin-api-password"
ignore = ["*.scss", "src/**", "README.md", "node_modules/**"]
```

### 3. Development

Start local development server with live reload and Vite:

```bash
pnpm dev
```

### 4. Production Build

```bash
pnpm build
```

### 5. Deploy Theme to Shopify

```bash
pnpm deploy
```

---

## 🧰 Scripts

```json
"scripts": {
  "build": "vite build",
  "deploy": "shopify theme push -e env",
  "preview": "shopify theme preview -e env"
}
```

---

## 🔍 Tooling & Tech

- **Tailwind**: Config in `tailwind.config.js`
- **PostCSS**: Config in `postcss.config.js`
- **Vite**: Handles optimized JS and CSS bundling, replacing Webpack
- **Vite Plugin for Tailwind**: Handles purging of unused CSS during production build

---

## 📦 License

MIT © [Dmytro]  
See [LICENSE.md](./LICENSE.md) for details.
