# Advanced_Django_training
Django using a TDD approach, using containerization of it for agility, API documentation with Swagger, Github Actions for automated testing, etc...



![docker_compose_setup](docker_compose_setup.png)



<code>docker-compose run --rm app sh -c "python manage.py collectstatic"</code> <br>

```run``` will start a specific container defined in config, to remove the container once is finished running. Important to avoir having lots of containers running in the background. <br>
```--rm``` removes the container <br>
```sh -c``` passes in a shell command






```docker build .``` once one has the app folder created at root <br>



**How we'll handling Linting** <br>
```docker-compose run --rm app sh -c "flake8"```

<br>

**How we'll test** <br>
```docker-compose run --rm app sh -c "python manage.py test"```
<br>


**Django installation from within docker**<br>
```docker-compose run --rm app sh -c "django-admin startproject app ."```
<br>


**Run project with Docker Compose**<br>
```docker-compose up```
<br>


### Other commands:


**Stop all the containers**
```docker stop $(docker ps -a -q)```


**Remove all the containers**
```docker rm $(docker ps -a -q)```
