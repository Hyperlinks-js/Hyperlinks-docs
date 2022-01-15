# Usage with Module-Bundlers 

The following module is a step-by-step guide to use the Hyperlinks package with module bundlers.

#### STEP-1 : 
- Import the package into a js file of your wish.  

?> The following assumes that you have already installed the package using the [previously](install?id=installtion) mentioned method(s).    

`index.js` :
```js
import * as Hyperlinks from '@hyperlinks-js/hyperlinks';
// Here the theme is set to 'mixed'. 
// More about themes will be discussed further in the documentation.
Hyperlinks.Init('mixed');
```

#### STEP-2 :
- A basic webpack configuration is required.

?> Webpack is used here to bundle the above imported package. You may use any module-bundler of your desire but the configuration may vary depending on the module-bundler being used.

`webpack.config.js` :
```js
const path = require('path');

module.exports = {
  entry: './index.js',
  output: {
    path: path.resolve(__dirname, 'dist'),
    publicPath: '',
    filename: 'index.bundle.js'
  },
  mode: 'development',
  devtool: 'source-map',
};
```

#### STEP-3 :
- Now, test out your setup using a browser.

!> Note : Please add the `/` in the end of the url in the `<a>` tag.  
✔️ ➙ `https://github.com/`  
❌ ➙ `https://github.com`
- To add more links to hyperlinks, just add more `<a>` tags with the same class name `hyperlinks`.

`index.html` :
```html
<!DOCTYPE html>
<html>
    <head>
        <script src="dist/index.bundle.js" type="module" defer></script>
    </head>
    <body>
        <a href="https://github.com/" class="hyperlinks">Hover me</a>
    </body>
</html>
```


Now go to your browser and open the `index.html` file and See the magic ✨
