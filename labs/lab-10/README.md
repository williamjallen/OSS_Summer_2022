# Lab 10

## Checkpoint 0
My weekly blog post may be found [here](https://github.com/williamjallen/OSS_Summer_2022/wiki/Project-update-August-1).

## Checkpoint 1

CouchDB was successfully run by following the CouchDB Docker installation directions.  The following command creates and runs the relevant docker container with a default account and port forwarding: `docker run -d --name my-couchdb -p 5984:5984 -e COUCHDB_USER=admin -e COUCHDB_PASSWORD=password couchdb`.  The following screenshot shows the CouchDB welcome message printed once setup was completed:
![A welcome message](welcome-message.png)

## Checkpoint 2

For Checkpoint 2, the CouchDB [tutorial](https://docs.couchdb.org/en/stable/intro/tour.html) was followed.

The command `curl -X GET http://admin:password@127.0.0.1:5984/_all_dbs` is used to display a list of databases.  The following default databases were listed:
![default databases](initial-all-dbs.png)

A "baseball" database was created.
![creating a baseball database](create-baseball-db.png)

An attempt was made to make a second "baseball" database, which failed.  A "plankton" database was created instead.
![Oops, you can't make two identical DBs](cannot-make-duplicate-db.png)

Fauxton was then loaded and the database configuration was verified.
![It works!](couch-db-verified.png)

A new "hello-world" database was created in Fauxton.
![A new database](a-new-hello-world-db.png)

A document was created in the "hello-world" database.
![A new document](a-new-document.png)

A new index was created in the "hello-world" database to allow us to effectively query the database in the next steps.
![Added an index](index-created.png)

The database was then queried for any items with a year of 1988.
![A successful query](run-a-query.png)

A range-based query was then run, which selected two elements from the database.
![A range-based query](range-based-query.png)

The "hello-world" database was then replicated into a new "hello-replication" database.
![Replicating a database](successful-replication.png)

## Checkpoint 3

For checkpoint 3, the CouchDB [API tutorial](https://docs.couchdb.org/en/stable/intro/api.html) was completed.

For the initial setup of this part, an "albums" database was created.  Like in Checkpoint 2, a command was run to create an identical database and an error was returned.  An "albums-backup" database was created and then deleted via the command line.  Additionally, the `curl -vX` option was used to provide verbose output.
![Using the CLI for CouchDB](create-albums-db.png)

The CouchDB CLI was used to create and get a new document with a UUID.
![Creating a document](cli-create-and-get-document.png)

The previous document was then edited with the following commands.
![Revising a document](revise-document.png)

A new document containing information for another song was added and the HTTP request and response were analyzed.
![Adding another song](cli-add-new-song.png)

After some effort to achieve the correct revision number, an attachment was successfully added to one of the documents.
![A new attachment](attachment-added.png)

A new database, "albums-replica", was created and "albums" was replicated into it successfully.
![Replication of a database via the CLI](cli-replication.png)

## Checkpoint 4

1. A query was run via the CLI, using an index created during the earlier portion of the lab.  The following results were returned:
![Query results](checkpoint-4-1.png)

2. The query run in the previous part of the lab was modified to select titles starting with a letter after "L".  The following results were returned:
![Query results](checkpoint-4-2.png)

3. An index was created to resolve the warning at the bottom of the previous screenshot as per the instructions.  The results follow:
![Creating an index via the CLI](checkpoint-4-3.png)

4. The query from item 2 was re-run and no warnings were printed:
![Re-running the query from item 2](checkpoint-4-4.png)