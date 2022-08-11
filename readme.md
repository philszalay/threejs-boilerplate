# Three.js Boilerplate

<img width="1280" alt="Screenshot 2022-08-08 at 23 06 55" src="https://user-images.githubusercontent.com/12916001/183514700-a881ec3f-4044-4e52-8277-c18817373f33.png">
https://philszalay.github.io/threejs-boilerplate/

## Setup
Download [Node.js 16](https://nodejs.org/en/download/).

``` bash
# Install dependencies (only the first time)
npm install

# Run the local server at localhost:8080
npm run dev

# Build for production in the dist/ directory
npm run build
```

## Deployment
To deploy the app with gh-pages some prerequisites are necessary.

### Install gh-pages
``` bash
npm install gh-pages --save-dev
```

For more information see: https://www.npmjs.com/package/gh-pages

### Adjustments
To load images and other assets after deploying some adjustments are necessary.

⋅ Change the homepage link (https://philszalay.github.io/threejs-boilerplate/) in your `package.json` to your gh-pages link.

⋅ In `webpack.common.js` change the `output.publicPath` property (/threejs-boilerplate/) to your path fragment for production mode.

### Deployment Script
To deploy your changes use the predefined deploy script. 

``` bash
# Build for production in the `dist` directory and publish the folder's content to the `gh-pages` branch
npm run deploy
```

Running the script for the first time will do the initial setup automatically and your project will be published automatically. The gh-pages settings can be found in your repository settings (`Settings -> Pages`).

## Formatting/Linting
Install https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint in your VS Code to use eslint for formatting and linting. A configuration file (`.eslintrc.js`) is already provided in the project.
