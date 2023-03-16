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

### Step 5:
  Create a Project in Crowdin.
  Use English as the source language, and French as the target language.
  
### Step 6:
  Add the following code in crowdin.yml file.
  ```js title=crowdin.yml
  project_id: '123456' //your project id here. You can find the project id in project dashboard of Crowdin
  api_token_env: CROWDIN_PERSONAL_TOKEN  // Create .env file. Add this parameter and add the Api token value. You can create this api token in Account setting-->API     tab-->You can create a token for your project.
  preserve_hierarchy: true
  files:
    # JSON translation files
    - source: /i18n/en/**/*
      translation: /i18n/%two_letters_code%/**/%original_file_name%
    # Docs Markdown files
    - source: /docs/**/*
      translation: /i18n/%two_letters_code%/docusaurus-plugin-content-docs/current/**/%original_file_name%
    # Blog Markdown files
    - source: /blog/**/*
      translation: /i18n/%two_letters_code%/docusaurus-plugin-content-blog/**/%original_file_name%
  ```
  
### Step 7: 
  Check whether your machine has Java installed. If not, install java into your machine. This step is insist by crowdin in their docs.
  Download link: https://www.java.com/en/
    
### Step 8:
  Add this script to package.json file
  ```js title=package.json
  "scripta":{
  "crowdin": "crowdin"
  }
  ```
    
### Step 9:
  Try executing the crowdin command in terminal. You should not get any error. If you getting any error try to install the crowdin.exe file.
  If necessary, just change the Execution policy in Powershell terminal.
  I am not explaining those here.
    
### Step 10: 
  if there is no error, that means we are good to go.
  Run the following command,
  ```
  npm run write-translation
  ```
  then,
  ```
  npm run crowdin upload
  ```
  
### Step 11: 
    Now your files would be uploaded to the crowdin site. Just go there, In Project Dashboard, Click on Pre-Translation. In that dropdown choose MT, choose the target language and choose all files if you want.
    
### Step 12:
  Now again change the scripts in package.json
  ```js title=package.json
  {
    "scripts": {
      "crowdin:sync": "docusaurus write-translations && crowdin upload && crowdin download"
    }
  }
  ```
  
### Step 13:
  Run the following code in terminal to translate the files.
  ```
  npm run crodwin:sync
  ```
### Step 14:
  You can find the files in i18n folder of your docusuarus project.
### Step 15:
  Try building your application and run build.
  ```
  npm run build
  ```
  then,
  ```
  npm run serve
  ```
  
That's it all set. Your docusaurus application translation will work. 
    
