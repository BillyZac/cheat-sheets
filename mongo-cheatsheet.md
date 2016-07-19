# Mongo shell

In Mongo, a database is a series of "collections" of "documents". Documents are basically javascript objects.

## show current db
db

## use db
use cats

## Show all dbs
show dbs

## Show collections in db
show collections

## Show stuff in a collection
db.cats.find()

To make it pretty:

db.cats.find().pretty()

## Find
db.cats.find( { name: "Fritz" } )
