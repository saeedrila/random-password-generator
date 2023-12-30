# Random Password Generator
This project is a random password generator app created using ReactJS and Material UI.
### Features:
This app helps users to create a random password of required length. Length range hardcoded is from 6 to 40 charectors.
The password can consist of symbols, numbers, lower case charectors, and upper case charectors.
Range of symbols: !@#$%^&*()
Range of numbers: 0123456789
Range of lower case charectors: abcdefghijklmnopqrstuvwxyz
Range of upper case charectors: ABCDEFGHIJKLMNOPQRSTUVWXYZ

### Default values:
Password length: 15
Use of symbols: True
Use of numbers: True
Use of lower case charectors: True
Use of upper case charectors: True

### Working:
When ever the customer click the 'Generate Password' button, a newly generated password will appear on a text field able the 'Generate Password' button.
The 'Copy' button can be clicked to copy the newly generated password to the clipboard. When ever the customer click on the 'Copy' button, it will change to 'Copied'.
When ever the customer change any of the password generation parameter, the 'Password' text field and 'Copy' button will disappear.
The customer has to switch-on atleast one of the non-length parameters. If the customer switch-off three parameters, the remaining switch will be automatically disabled.


## Steps followed
Create a new react app
```
npx create-react-app
```
Install Material UI (MUI)
```
npm install @mui/material @emotion/react @emotion/styled @mui/icons-material
```

## To run the app in development mode
```
npm start
```
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

## To host the page using gh-pages
```
npm install gh-pages --save-dev
```
Open package.json file in text editor

add a homepage property in the following format https://{username}.github.io/{repo-name}
```
{
  "name": "random-password-generator",
  "version": "0.1.0",
  "homepage": "https://github.com/saeedrila/Random-password-generator",
  "private": true,
```
in my case.

Add deployment script to the package.json file
```
  "scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build",
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  },
```
in my case.

Add a 'remote' that points to the GitHub repository
```
git remote add origin git@github.com:saeedrila/Random-password-generator.git
```
in my case. Since I already using SSH connection with github.

Push the react app to the GitHub repository.
```
npm run deploy
```
```
npm run deploy -- -m "Deploy React app to GitHub Pages"
```
At this moment, a new branch 'gh-pages' will be created on the github.

Configure GitHub pages.
1.  Navigate to the GitHub Pages
i.  In your web browser, navigate to the GitHub repository
ii. Above the code browser, click on the tab labeled "Settings"
iii.In the sidebar, in the "Code and automation" section, click on "Pages"

2.  Configure the "Build and deployment" settings like this:
i.  Source: Deploy from a branch
ii. Branch: gh-pages
iii.Folder: / (root)

3.  Click on the "Save" button