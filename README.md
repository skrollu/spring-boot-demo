# Spring boot api demo tutorial

This project follow the youtube tutorial found here: 
	
	https://www.youtube.com/watch?v=vtPkZShrvXQ&t=3592s

The fake part run an API with the Tomcat embeded server memories (data aren't stored)
But the second part of the tutorial use a docker image of postgres to store data:

	docker run --name postgres-springboot-demo -e POSTGRES_PASSWORD=password -d -p 5432:5432 postgres:alpine
	
Project is using Docker to run a postgres DB in brackground.

	docker ps
	docker exec -it [container id]
	CREATE DATABASE spring_boot_postgres_demo_db;
	\l
	\c spring_boot_postgres_demo_db
	\d
	\dt
	\d person
	CREATE extension "uuid-ossp"
	select uuid_generate_v4();
	INSERT INTO person(id, name) VALUES(uuid_generate_v4(), "James Bond");
	
Endpoints: 

	http://localhost:8181/api/v1/person/
	http://localhost:8181/api/v1/person/ee7c5172-5d3e-4ea8-a804-5f6077182518
	
Also POST PUT and DELTE endpoints are availables.

Using Flyway for migration database.
Hikari for DB manager.
