# React Boilerplate

**Steps to follow:**
1. Open the terminal and run **"npm init"** command. **(This will create your package.json file)**
2. Run **npm install react react-dom** in terminal, to install react dependencies in (package.json) file.
3. Now install webpack, webpack-dev-server, webpack-cli as a dev dependency.
   * Purpose of webpack is to bundle all the assets ( HTML, CSS, Javascript ) to one single file, ready for          production.
4.  Now we need to install babel dependencies: 
     ```javascript
        terminal: 
        npm i -save-dev babel-core babel-loader babel-preset-env babel-preset-react html-webpack-plugin
     ```
      * babel-core
      * babel-preset-react, babel-reset-env (babel-preset-es2015 )
      * which we use to use coz **babel-preset-env** does not only compilte ES6 version but also later
          and also it looks at the browser and compile based on that browser.
      * babel-loader ( Which compiles jsx templates, used by react )
    ### Purpose of babel is to transpile our ES6 or later version code to browser friendly code , so that it can run on older browsers as well.
5. Now we will install **HTML WEBPACK PLUGIN**, which helps in creating our production ready index.html file in       dist folder for us to use with the bundles file added to the body tag before close.

## Package.json file:

```javascript
 package.json:
    {
    "name": "my-react-boilerplate",
    "version": "1.0.0",
    "description": "React BoilerPlate",
    "main": "index.js",
    "scripts": {
        "start": "webpack-dev-server --mode development --open --hot",
        "build": "webpack --mode production"
    },
    "author": "Attamjot Singh Khurana ( AJ )",
    "license": "ISC",
    "dependencies": {
        "react": "^16.13.1",
        "react-dom": "^16.13.1"
    },
    "devDependencies": {
        "babel-core": "^6.26.3",
        "babel-loader": "^7.1.5",
        "babel-preset-env": "^1.7.0",
        "babel-preset-react": "^6.24.1",
        "html-webpack-plugin": "^4.2.0",
        "webpack": "^4.43.0",
        "webpack-cli": "^3.3.11",
        "webpack-dev-server": "^3.10.3"
    }
    }

```
