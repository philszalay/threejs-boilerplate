# Three.js Boilerplate
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

## Deployment to gh-pages
To deploy the app with gh-pages some prerequisites are necessary.

### Install gh-pages
``` bash
npm install gh-pages --save-dev
```

For more information see: https://www.npmjs.com/package/gh-pages

### Adjustments
To load images and other assets from the correct path some adjustments are necessary.

Change the homepage link (https://philszalay.github.io/threejs-boilerplate/) in package.json to your gh-pages link.

In webpack.common.js change output.publicPath (/threejs-boilerplate/) to your path fragment for production mode.

### Deployment
To deploy your changes use the predefined deploy script. 

``` bash
# Build for production int the dist/ directory and publish the folder's content to the "gh-pages" branch
npm run deploy
```

Running the script for the first time will set up everything and your project will be published automatically. The Gh-pages settings can be found Settings -> Pages