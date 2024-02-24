

# Instalando Docker 

    - curl -fsSL https://get.docker.com | bash
    - docker version

### Verificando  containers 
    - docker container ls
    - docker container ls -a

### Criando um container 
    - docker container run -ti debian 
    - docker container run -d nginx 

### Voltando ao container criado 
    - docker container attach "container id"

### Comandos uteis  container 
    - docker container stop "container id"
    - docker container start "container id"
    - docker container restart "container id"
    - docker container pause "container id"
    - docker container unpause "container id"
    - docker container remove "container id"
    - docker image ls
    - docker stop $(docker ps -a -q) (parando todas as intancias)
    - docker rm $(docker ps -a -q) (remove todas as instancias)
    - docker image rm $(docker image ls -a -q) (remove todas imagens)
    - docker volume prune (remove todos os volumes)

### Acessando o terminal do container 
    - docker container exec -it "contaiver id" /bin/sh

### Consumo do container 
    - docker container stats "container id"
    - docker container inspect "container id"


### Apagando container e volumes 

    - docker volume prune
    - docker container prune
### Criando container com limitação de recursos 

    - docker container run -d -memory 128 ngnix
    - docker container run -d -memory 128  --cpus 0.5 ngnix
    - docker container update --cpus 0.5 --memory 64M "container id"


































