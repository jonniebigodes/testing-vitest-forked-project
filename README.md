# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some Oxlint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the Oxlint configuration

If you are developing a production application, we recommend enabling type-aware lint rules by installing `oxlint-tsgolint` and editing `.oxlintrc.json`:

```json
{
  "$schema": "./node_modules/oxlint/configuration_schema.json",
  "plugins": ["react", "typescript", "oxc"],
  "options": {
    "typeAware": true
  },
  "rules": {
    "react/rules-of-hooks": "error",
    "react/only-export-components": ["warn", { "allowConstantExport": true }]
  }
}
```

See the [Oxlint rules documentation](https://oxc.rs/docs/guide/usage/linter/rules) for the full list of rules and categories.

## Project structure

```
├── index.html
├── package.json
├── tsconfig.json
├── vite.config.ts
├── .oxlintrc.json
├── .eslintrc.json
├── .prettierrc
├── .gitignore
├── public/
└── src/
    ├── main.tsx
    ├── App.tsx
    ├── App.css
    ├── assets/
    ├── components/
    ├── pages/
    └── styles/
```

- `index.html` - The main HTML file for the application.
- `package.json` - The package manifest file that contains metadata about the project and its dependencies.
- `tsconfig.json` - The TypeScript configuration file that specifies compiler options and project settings.
- `vite.config.ts` - The Vite configuration file that defines how the application is built and served.
- `.oxlintrc.json` - The Oxlint configuration file that specifies the rules and settings for the linter.
- `.eslintrc.json` - The ESLint configuration file that specifies the rules and settings for the linter.
- `.prettierrc` - The Prettier configuration file that specifies the formatting rules for the code.
- `.gitignore` - The Git ignore file that specifies which files and directories should be ignored by Git.
- `public/` - The directory that contains static assets that are served as-is.
- `src/` - The directory that contains the source code for the application.
  - `main.tsx` - The entry point for the application that renders the root component.
  - `App.tsx` - The main component that defines the structure and behavior of the application.
  - `App.css` - The CSS file that defines the styles for the application.
  - `assets/` - The directory that contains images, fonts, and other static assets used in the application.
  - `components/` - The directory that contains reusable React components used in the application. It is recommended to organize components into subdirectories based on their functionality or feature and to use index.ts files to export components for easier imports. Additionally it also features in Storybook stories for each component, which can be used for visual testing and documentation and Vitest tests co-located with the components for easier testing and maintenance.
  - `pages/` - The directory that contains the main pages of the application.
  - `styles/` - The directory that contains global styles and theme files used in the application.
