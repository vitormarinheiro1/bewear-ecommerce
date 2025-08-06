CONFIGURACAO VSCODE FRONTEND:

1. ordenacao tailwind: npm install -D prettier prettier-plugin-tailwindcss

2. settings.json:
"[javascript]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[typescript]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[javascriptreact]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[typescriptreact]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
}

3. importacoes eslint
npm install --save-dev eslint-plugin-simple-import-sort

file: eslint.config.mjs
  {
    plugins: {
      "simple-import-sort": simpleImportSort,
    },
    rules: {
      "simple-import-sort/imports": "error",
      "simple-import-sort/exports": "error",
    },
  },

4. Criar pasta e arquivo: .vscode/settings.json
{
  "eslint.workingDirectories": [{ "mode": "auto" }],
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact"
  ],
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit"
  }
}



===================================
Shadcn THEME: https://ui.shadcn.com/themes#themes

=============
ORM DRIZZLE = https://orm.drizzle.team/docs/get-started/postgresql-new

npx drizzle-kit push - subir tudo
npx drizzle-kit studio - ambiente do drizzle
seed: npx tsx --env-file=.env src/db/seed.ts

NEON DB = PARA RODAR POSTGRES, MAS POSSO RODAR COM DOCKER


autenticacao: npm i better-auth
