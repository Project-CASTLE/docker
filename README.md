# docker

CASTLE's Project Docker stuff

---

## Requirements

* docker
* docker-compose

### Elastic Search requirements

#### Maximum map count check

https://www.elastic.co/guide/en/elasticsearch/reference/64/_maximum_map_count_check.html

With Docker Toolbox:

```shell
docker-machine ssh
sudo sysctl -w vm.max_map_count=262144
exit
```

---

## Build

```shell
git clone https://github.com/Project-CASTLE/docker.git
cd docker/docker-img-ansible
docker build -t castle-ansible:0.0.1 .
cd ..
docker-compose up
```

## Use

```shell

```
