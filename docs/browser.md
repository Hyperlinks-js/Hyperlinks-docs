# Usage with CDN 

The following module is a step-by-step guide to use the Hyperlinks package with CDN.

#### STEP-1 :
- Use the CDN of your desire, [jsdelivr](https://www.jsdelivr.com/package/npm/@hyperlinks-js/hyperlinks) is used here.

!> Note : Please add the `/` in the end of the url in the `<a>` tag.  
✔️ ➙ `https://github.com/`  
❌ ➙ `https://github.com`

#### STEP-2 :
- To add more links to hyperlinks, just add more `<a>` tags with the same class name `hyperlinks`.
`index.html` :
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <script src="https://cdn.jsdelivr.net/npm/@hyperlinks-js/hyperlinks@2.0.0/dist/index.bundle.js" type="module"></script>
</head>
<body>
    <a href="https://github.com/" class="hyperlinks">GitHub</a>
</body>
</html>
```

#### STEP-3 :
- Initialise a instance of Hyperlinks.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <script src="https://cdn.jsdelivr.net/npm/@hyperlinks-js/hyperlinks@2.0.0/dist/index.bundle.js" type="module"></script>
    <script type="module">
        Hyperlinks.Init("dark-horizontal") // You can substitute the theme name with any theme name you want.
    </script>
</head>
<body>
    <a href="https://github.com/" class="hyperlinks">GitHub</a>
</body>
</html>
```

Now go to your browser and open the `index.html` file and See the magic ✨
