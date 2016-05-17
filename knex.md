Resources:
http://knexjs.org/
http://www.sql-join.com/

$ createdb databaseName
$ cd server
$ npm install --save knex pg
$ knex init

module.exports = {

  development: {
    client: 'postgresql',
    connection: 'postgresql://localhost/galvanize-reads'
  },

  production: {
    client: 'postgresql',
    connection: process.env.DATABASE_URL
  }

};

$ knex migrate:make migrationName

exports.up = function(knex, Promise) {
  return knex.schema.createTable('tableName', function (table) {
    table.increments();
    table.string('example');
    table.boolean('example');
    table.timestamps();
  })
};

exports.down = function(knex, Promise) {
  return knex.schema.dropTable('tableName');
};

$ knex migrate:latest

$ knex migrate:rollback

$ knex seed:make seed_name

$ knex seed:run

in api.js >> var knex = require('knex')(require('../knexfile')['development']);
