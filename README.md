Name
----

mongodb-rest - REST server for MongoDB

Description
-----------

This is an attempt at creating a REST server for MongoDB using Node.
It uses the native node.js MongoDB driver.

Notes
-----

Supported REST requests:

* GET /db/collection - Returns all documents
* GET /db/collection?query=%7B%22isDone%22%3A%20false%7D - Returns all documents satisfying query
* GET /db/collection/_id - Returns document with _id
* POST /db/collection - Insert new document in collection (document in POST body)
* PUT /db/collection/_id - Update document with _id (updated document in PUT body)
* DELETE /db/collection/_id - Delete document with _id

Miscellaneous commands:

* POST /#connect - Connects to default database or database provided in post body

Flavors:

* Setup "sproutcore" as flavor, it will then change _id as returned by MongoDB into guid, as used by SproutCore. I'm not sure whether this will eventually be useful, though it does allow for simpler DataSources.

Todo
----

* REST - PUT /db/collection - Update collection with changes in PUT body
* Other useful commands (quit, reconnect, addUser, removeUser, etc)
* Error handling - It's not-implemented at all at the moment

See Also
--------

http://github.com/christkv/node-mongodb-native