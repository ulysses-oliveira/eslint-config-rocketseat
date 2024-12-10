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
Inside `.eslintrc.json`
```
// Next.js
// "@rocketseat/eslint-config/next"
// Node.js
// "@rocketseat/eslint-config/node"
// React
// "@rocketseat/eslint-config/react"

{
  "extends": [
    "next/core-web-vitals",
    "@rocketseat/eslint-config/next",
    "prettier"
  ],
  "rules": {
    "prettier/prettier": "error"
  }
}
```

Inside `package.json`
```
"overrides": {
  "eslint-plugin-react-hooks": "5.1.0"
}
```

Inside `.prettierrc`
```
{
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2,
  "plugins": ["prettier-plugin-tailwindcss"]
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
