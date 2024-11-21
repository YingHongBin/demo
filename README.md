# Demo Project
This repo aim to build a demo spring project with java 21 for learning purpose. 

## Containerize It
Package this application first
```shell
mvn clean package
```
Then build the docker image
```shell
docker build -t demo .
```
Run the docker image
```shell
docker run  -e spring.datasource.url=yoururl \
            -e spring.datasource.username=yourusername \
            -e spring.datasource.password=yourpassword \
            -p 8080:8080 \
            --name demo \
            demo
```