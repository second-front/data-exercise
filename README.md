# Getting Started

You'll need Docker installed

```
Tested and ran on
- Docker version 19.03.6, build 369ce74a3c
- docker-compose version 1.21.2, build a133471
```

After you clone the repo, to build and run: `docker-compose up --build`

This starts two containers:
1. `exercise_neo4j`
    * You can access the Neo4j Browser via [http://localhost:7474/browser/](http://localhost:7474/browser/)
    * DB Connection Info
        * Username: `neo4j`
        * Password: `test`
        * Active database: `graph.db`    
        * Generated Connection URL: ~~`bolt://localhost:7687`~~
            * Since Neo4j is a running in a container, you can refernce the name (`exercise_neo4j`) as the Docker Connection URL from Juypter
                * `"bolt://neo4j:test@exercise_neo4j"`

1. `exercise_jupyter`
    * Will be available on [http://localhost:8888/tree](http://localhost:8888/tree)
        * A token is generated after this container starts. You can find this value in the console. It will look something like `http://localhost:8888/?token=c2c259d81a929ddd3340eafcce74f37f83e935c79fa17f9b` or `http://127.0.0.1:8888/?token=ec7bce946a64612b55ab25fe9e008198296fa6421bdb9926`
        * This container uses the [jupyter-pyspark-notebook Docker image from the distro](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#core-stacks)


You can tunnel into either container by running: `docker exec -it <CONTAINER NAME> bash`

> For each container, after you login once, your connection credentials are stored in your web browser

# The Exercise

The following instruction set is vague by design. This is your opportunity to put your technical chops as data engineer on display so have fun with this!

There are many ways to perform this exercise. Limit your time to four hours. Commit your code often. When you're complete, or when you've reached the time limit, push your final commit. The final commit message must contain the following string "FINAL-COMMIT," to mark the end of the exercise. Submit a link to your repo when you're complete. Be sure to include a detailed Readme File so we can run your submission.

You are free to modify any of the provided infrastructure to meet your needs.

Base Criteria
- [ ] Write a script to consume three or more realted open source APIs to populate a datastore
- [ ] Provide instructions on how to run your script
- [ ] Visually render the data inside of a notebook
- [ ] Provide some light data analytics

Here is a starting point for source data [DATA.GOV Catalog](https://catalog.data.gov/dataset).

Bonus
- [ ] Clean commit history
- [ ] Testing coverage
- [ ] Low reliance on third party dependencies
