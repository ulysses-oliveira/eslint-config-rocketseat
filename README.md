# Rocketseat ESLint config

## Whats included?

- Standard config base;
- React plugin;
- React Hooks plugin;
- JSX a11y plugin;
- Prettier;

## Setup

### React (with Next.js) or Node.js
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
    "@rocketseat/eslint-config/next", 
    "next/core-web-vitals"
  ]
}
```

## VS Code config
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

### Settings for using the prettier-plugin-tailwindcss plugin
Inside `package.json`
```
"overrides": {
  "eslint-plugin-react-hooks": "5.1.0"
}
```
Inside `.eslintrc.json`
```
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
