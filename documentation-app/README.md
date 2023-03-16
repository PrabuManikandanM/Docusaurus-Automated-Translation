# Docusaurus Automated Translation

## Using Crowdin Plugin 
### Step 1: 
  Create a docusaurus application.
  ```
  npx create-docusaurus@latest my-website classic
  ```
  
### Step 2:
  Add the following code to add internationalization.
  ``` js title="docusaurus.config.js"
  module.exports = {
  i18n: {
    defaultLocale: 'en',
    locales: ['en', 'fr']
    },
  };
  ```
### Step 3:
  Install Crowdin@cli 
  ```
  npm install @crowdin/cli@3
  ```
### Step 4:
  Create a account in Crowdin(https://crowdin.com) site.
