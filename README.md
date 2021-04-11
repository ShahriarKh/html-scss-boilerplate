# html-scss-boilerplate
A simple boilerplate for HTML5 + Minified SCSS, plus Hot Reload

## Note for Beginners
You should have [Node.js](https://nodejs.org/en/download/) installed to use commands.

## First Step
To begin coding, put your `html` files inside `src/` folder and your scss files in `src/styles`.

## :fire: Hot Reload!
To use the hot reload feature and preview your changes as you save your code, open your root folder (not `src`) in a terminal/cmd and type `npm start`. This will open your `html` files with automatic `scss` compiling in `localhost`. If everything is okay, you will see something like this in your terminal:
```
[Browsersync] Access URLs:
 -------------------------------------
       Local: http://localhost:3000
    External: http://192.168.1.10:3000
 -------------------------------------
          UI: http://localhost:3001
 UI External: http://localhost:3001
 -------------------------------------
```
Localhost will be opened automatically for you. In case it didn't, manually enter the URL after `Local: `.
You can stop the server with `ctrl + c` (in Windows).

## :iphone: Live Preview on Mobile and Other Devices
To access your development server from another device (for example, your mobile), open the `External` url, not the `Local` one.
Make sure the devices are connected to the same network and `port 3000` (or any other port you use) is not blocked by your firewall!

## Build
Ready to publish your work? Make sure server isn't running, then type `npm run build` in your terminal; this will create a folder called `build/` with minified css files and minified html files inside it. Tamam!

## Commands Explained
You can run any of these commands as you wish:
* `npm run css-scss:*` Generates `css` from `scss` using node-sass without minification. (replace * with `dev` or `build`)
* `npm run css-autoprefixer:*`: Automatically adds browser prefixes to css files (where needed) using PostCSS "autoprefixer" plugin. (replace * with `dev` or `build`)
* `npm run css-nano`: Minifies css code using PostCSS "nano" plugin. (only works in `build` folder)

To change server port, add `--port number` to the `server` command inside `package.json`.
Here is an example to change port from 3000 to 8080:
```
"server": "browser-sync start --server src --serveStatic temp --files temp, \"src/**/*.html\" --port 8080",
```

