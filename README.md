# Spring boot demo tutorial

This project followed the youtube tutorial found here: 
	
	https://www.youtube.com/watch?v=vtPkZShrvXQ&t=3592s

The fake part run an API with the Tomcat embeded server memories (data aren't stored)
But the second part of the tutorial use a docker image of postgres to store data:

	docker run --name postgres-springboot-demo -e POSTGRES_PASSWORD=password -d -p 5432:5432 postgres:alpine