# Rocketseat ESLint config

## Whats included?

- Standard config base;
- React plugin;
- React Hooks plugin;
- JSX a11y plugin;
- Prettier;

## Setup

### React (with Next.js) or Node.js and settings for using the prettier-plugin-tailwindcss plugin
Install dependencies:
```
npm i -D eslint @rocketseat/eslint-config
```
```
npm i -D @typescript-eslint/parser @typescript-eslint/eslint-plugin
```
Inside `eslint.config.mjs`
```
import { dirname } from 'path'
import { fileURLToPath } from 'url'
import { FlatCompat } from '@eslint/eslintrc'

const __filename = fileURLToPath(import.meta.url)
const __dirname = dirname(__filename)

const compat = new FlatCompat({
  baseDirectory: __dirname,
})

const eslintConfig = [
  ...compat.extends(
    'next/core-web-vitals',
    '@rocketseat/eslint-config/next',
    'prettier',
  ),
  {
    files: ['*.ts', '*.tsx'],
    parser: '@typescript-eslint/parser',
    parserOptions: {
      project: './tsconfig.json', // Certifique-se de que o ESLint sabe onde está o tsconfig
    },
    rules: {
      'prettier/prettier': 'error',
    },
  },
]

export default eslintConfig
```

Inside `package.json`
```
"overrides": {
  "eslint-plugin-react-hooks": "5.1.0"
}
```

### VS Code config
Inside `settings.json`
```
"[prisma]": {
  "editor.formatOnSave": true
},
"editor.codeActionsOnSave": {
  "source.fixAll.eslint": "explicit",
  "source.addMissingImports": "explicit"
}
```

Inside `settings.json`
```
"[language]": {
  "editor.defaultFormatter": "dbaeumer.vscode-eslint"
}
```

## Test commands
```
npx eslint .
```

```

```
