<img height="100em" src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Docker_%28container_engine%29_logo.svg/1280px-Docker_%28container_engine%29_logo.svg.png" >

## Docker commands

### Alguns comandos básicos:

- `$ sudo service docker start` --- _Inicia o serviço Docker._
- `$ sudo service docker status` --- _Verifica o status do serviço Docker._
- `$ docker-compose up -d` --- _Inicia a aplicação em segundo plano._
- `$ docker-compose down` --- _Para e remove os containers da aplicação._
- `$ docker-compose stop` --- _Interrompe todos os containers em execução sem removê-los._
- `$ docker-compose exec CONTAINER_NAME sh` --- _Acessa o container dentro do Docker._
- `$ docker ps` --- _Exibe os containers em execução._
- `$ docker images` --- _Exibe as imagens Docker._
- `$ docker container list -a` --- _Lista todos os containers, incluindo os desligados._
- `$ docker stop CONTAINER_ID` --- _Interrompe um container em execução._
- `$ docker kill $(docker ps -q)` --- _Para todos os containers em execução._
- `$ docker rm CONTAINER_ID` --- _Remove um container._
- `$ docker rmi IMAGE_ID` --- _Remove uma imagem._
- `$ docker rmi IMAGE_ID -f` --- _Força a remoção de uma imagem._
- `$ docker rm $(docker ps -a -q)` --- _Remove todos os containers._
- `$ docker rmi $(docker images -q)` --- _Remove todas as imagens._
- `$ docker exec -it CONTAINER_ID bash` --- _Inicia um terminal Bash dentro de um container pelo ID._
- `$ docker exec -it CONTAINER_NAME bash` --- _Inicia um terminal Bash dentro de um container pelo nome._

### Para iniciar automaticamente o Docker e o Containerd na inicialização de outras distribuições, use os comandos abaixo:

- `$ sudo systemctl enable docker.service` --- _Habilita o serviço Docker para iniciar automaticamente._
- `$ sudo systemctl enable containerd.service` --- _Habilita o serviço Containerd para iniciar automaticamente._

### Dando permissão ao usuário para ler e gravar ao Docker:

- `$ sudo groupadd docker` --- _Adiciona e verifica o grupo Docker._
- `$ sudo usermod -aG docker $USER` --- _Adiciona o usuário ao grupo Docker._
- `$ newgrp docker` --- _Atualiza o grupo do usuário para Docker._
- `$ sudo chown -R $USER:$USER .` --- _Fornece permissões ao usuário para o diretório atual._
- `$ sudo chmod 666 /var/run/docker.sock` --- _Permissão de leitura e gravação no socket Docker._
