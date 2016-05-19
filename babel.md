$ cd into app
$ npm install --save-dev babel babel-cli babel-preset-es2015
$ ./node_modules/.bin/babel js/app.js (runs files)
$ echo '{ "presets": ["es2015"] }' > .babelrc
package.json >>  "scripts": {
    "start": "http-server -c-0 -o",
    "build": "babel js --out-file dist/main.js --watch"
  },
