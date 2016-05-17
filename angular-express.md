1. Create repo on Github.
1. Clone to local machine.
1. $ cd [directory]

1. $ express --git server
1. $ cd server
1. $ npm install
1. $ npm install --save cors
1. add to app.js >> var cors = require('cors');
1. add cors below var app = express(); >> app.use(cors());
1. modify/clean-up app.js
1. delete views folder
1. delete public folder
1. delete routes/users.js
1. rename routes/index.js > api.js
1. $ nodemon > go to http://localhost:3000/api
1. install knex, follow knex.md steps

1. $ mkdir client
1. $ cd client
1. $ touch index.html
1. $ firebase init
1. $ mkdir app
1. $ touch app.module.js
