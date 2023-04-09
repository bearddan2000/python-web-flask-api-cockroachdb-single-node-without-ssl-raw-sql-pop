# python-web-flask-api-cockroachdb-single-node-without-ssl-raw-sql-pop

## Description
Creates an api CRUD of `pop` for a flask project, using raw sql.

A python flask build, that connects to single node cluster
cockroach database without ssl.

If path is not found, will default to 404 error.

Remotely tested with *testify*.

## Tech stack
- python
  - flask
  - sqlalchemy
  - testify
  - requests
- bootstrap
- jquery
- dataTable
- cockroachdb

## Docker stack
- python:latest
- cockroachdb/cockroach:v19.2.4

## To run
`sudo ./install.sh -u`
- Get all pops: http://localhost/pop
  - Schema id, name, and color
- CRUD opperations
  - Create: curl -i -X PUT localhost/pop/<id>
  - Read: http://localhost/pop/<id>
  - Update: curl -i -X POST localhost/pop/<id>/<name>/<color>
  - Delete: curl -i -X DELETE localhost/pop/<id>

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`
