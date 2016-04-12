$ cd public
$ mkdir sass
$ cd sass
$ touch style.scss
$ echo "@import 'components/base';" > style.scss
$ mkdir components
$ cd components
$ touch _base.scss

$ node-sass --watch public/sass/style.scss -o public/stylesheets/
