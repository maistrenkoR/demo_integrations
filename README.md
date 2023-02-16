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

7. install ```npm install -D @cypress/code-coverage```
```cypress.config.ts
import { defineConfig } from 'cypress'

export default defineConfig({
  // setupNodeEvents can be defined in either
  // the e2e or component configuration
  e2e: {
    setupNodeEvents(on, config) {
      require('@cypress/code-coverage/task')(on, config)
      // include any other plugin code...

      // It's IMPORTANT to return the config object
      // with any changed environment variables
      return config
    },
  },
})
```
```e2e.ts
import '@cypress/code-coverage/support'
```