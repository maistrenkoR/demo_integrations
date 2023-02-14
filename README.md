# demo_integrations
1. Set yarn
```npm install --global yarn```

2. Install Cypress
```yarn add cypress --dev ```

3. Add node_modules to .gitignore

4. run Cypress
```yarn run cypress open```

5. install TypeScript
```yarn add --dev typescript```

6. create tsconfig.json inside cypress folder and configure it
```typescript
{
  "compilerOptions": {
    "target": "es5",
    "lib": ["es5", "dom"],
    "types": ["cypress", "node"]
  },
  "include": ["**/*.ts"]
}
```