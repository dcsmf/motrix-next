# Motrix Next Contributing Guide

Before you start contributing, make sure you already understand [GitHub flow](https://guides.github.com/introduction/flow/).

## 🛠 Development Setup

```bash
git clone https://github.com/AnInsomniacy/motrix-next.git
cd motrix-next
pnpm install
pnpm tauri dev
```

### Prerequisites

- [Rust](https://rustup.rs/) (latest stable)
- [Node.js](https://nodejs.org/) >= 18
- [pnpm](https://pnpm.io/)

## 🌍 Translation Guide

First you need to determine the English abbreviation of a language as **locale**, such as `en-US`. This locale value should strictly refer to the [Chromium Source Code](https://source.chromium.org/chromium/chromium/src/+/main:ui/base/l10n/l10n_util.cc).

The internationalization of Motrix Next uses [vue-i18n](https://vue-i18n.intlify.dev/).

The configuration files are divided by **locale** under `src/shared/locales/`, such as `src/shared/locales/en-US` and `src/shared/locales/zh-CN`.

There are language files in each directory organized by business module:

- `about.js`
- `app.js`
- `edit.js`
- `help.js`
- `index.js`
- `menu.js`
- `preferences.js`
- `subnav.js`
- `task.js`
- `window.js`

### Adding a New Language

1. Create a new directory under `src/shared/locales/` with the locale code (e.g. `src/shared/locales/de/`)
2. Copy the files from `src/shared/locales/en-US/` as a template
3. Translate each file
4. Register the locale in `src/shared/locales/all.js`
5. Submit a Pull Request

## 🤝 Pull Requests

- Fork the repo and create your branch from `main`
- If you've added code, ensure TypeScript compiles without errors (`npx vue-tsc --noEmit`)
- Make sure your code follows the existing style
- Write a clear PR description

## 📜 License

By contributing, you agree that your contributions will be licensed under the [MIT License](https://opensource.org/licenses/MIT).
