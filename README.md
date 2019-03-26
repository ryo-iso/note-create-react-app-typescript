# Note: React with Typescript from Create React App

This is for the note purpose on how to start new react project with lint customizations.

To start a project, better follow steps.

## Steps to Create New Project

1. `yarn create react-app my-app --typescript`

2. `yarn add prettier @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-config-airbnb eslint-config-prettier eslint-plugin-prettier stylelint stylelint-config-recommended --dev`

3. Edit `package.json`:

   ```diff
   -  "eslintConfig": {
   -    "extends": "react-app"
   -  },
   ```

4. Copy `.eslintrc`, `.prettierrc`, `.stylelintrc` from this repo into project root

5. (Temporary until Create React App includes this rule as default) 

   `yarn add eslint-plugin-react-hooks@next --dev`

   Edit `.eslintrc`:

   ```diff
      "plugins": [
        // ...
   +    "react-hooks",
        // ...
      ],
      "rules": {
        // ...
   +    "react-hooks/rules-of-hooks": "error"
        // ...
      }
   ```


