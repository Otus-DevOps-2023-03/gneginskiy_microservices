# gneginskiy_microservices
gneginskiy microservices repository

Created a bunch of containers to collect and process the logs from the test application: 

- fluentd - log collector
- elasticsearch - db and full text search engine
- kibana - sort of a dashboard to query log data
- zipkin - UI for tracing requests. 

---
created a bunch of docker images: 
https://hub.docker.com/repository/docker/gneginskiy/prometheus/general
https://hub.docker.com/repository/docker/gneginskiy/post/general
https://hub.docker.com/repository/docker/gneginskiy/comment/general
https://hub.docker.com/repository/docker/gneginskiy/ui/general

to name a docker-compose project, we can use the following command syntax:
> docker-compose -p mycustombeautifulproject up -d
