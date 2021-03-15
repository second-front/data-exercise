# Getting Started

Requirements - You'll need docker installed

```
Tested and ran on
- Docker version 19.03.6, build 369ce74a3c
- docker-compose version 1.21.2, build a133471
```

To build and run: `docker-compose up --build`

To tunnel into the Neo4j container: `docker exec -it neo4j`

Once the container starts, you can access the Neo4j Browser via [http://localhost:7474/browser/](http://localhost:7474/browser/)

DB Connection Info
* Connect URL: `bolt://localhost:7687`
* Username: `neo4j`
* Password: `test`
* Active database: `graph.db`

> After you login once, your connection credentials are stored in your web browser

# The Exercise

1. Write a script to consume three or more realted open source APIs to populate the database
1. Provide the instructions to run your script

Here is a starting point for data [DATA.GOV Catalog](https://catalog.data.gov/dataset)