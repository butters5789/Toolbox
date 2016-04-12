Resources:
http://knexjs.org/
http://www.sql-join.com/

$ knex init

module.exports = {

  development: {
    client: 'postgresql',
    connection: 'postgresql://localhost/galvanize-reads'
  },
  seeds: {
    directory: './seeds/'
  },

  production: {
    client: 'postgresql',
    cconnection: process.env.DATABASE_URL,
    migrations: {
      tableName: 'knex_migrations'
    }
  },
  seeds: {
    directory: './seeds/'
  }

};

$ createdb databaseName
$ knex migrate:make databaseName

exports.up = function(knex, Promise) {
  return knex.schema.createTable('tableName', function (table) {
    table.increments();
    table.string('example');
    table.boolean('example');
    table.timestamps();
  })
};

exports.down = function(knex, Promise) {
  return knex.schema.dropTable('users');
};

$ knex migrate:latest

$ knex migrate:rollback

$ knex seed:make seed_name

$ knex seed:run

var knex = require('knex')(require('../knexfile')['development']);
