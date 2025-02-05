<img height="100em" src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Docker_%28container_engine%29_logo.svg/1280px-Docker_%28container_engine%29_logo.svg.png" >

## Docker commands

### Comandos básicos de serviço Docker:

- `$ sudo service docker start` --- _Inicia o serviço Docker._
- `$ sudo service docker status` --- _Verifica o status do serviço Docker._
- `$ sudo systemctl enable docker.service` --- _Habilita o serviço Docker para iniciar automaticamente._
- `$ sudo systemctl enable containerd.service` --- _Habilita o serviço Containerd para iniciar automaticamente._

### Comandos do Docker Compose:

- `$ docker-compose up -d` --- _Inicia a aplicação em segundo plano._
- `$ docker-compose down` --- _Para e remove os containers da aplicação._
- `$ docker-compose stop` --- _Interrompe todos os containers em execução sem removê-los._
- `$ docker-compose exec CONTAINER_NAME sh` --- _Acessa o container dentro do Docker._

### Comandos de containers:

- `$ docker ps` --- _Exibe os containers em execução._
- `$ docker container list -a` --- _Lista todos os containers, incluindo os desligados._
- `$ docker start CONTAINER_ID_||_CONTAINER_NAME` --- _Inicia um container._
- `$ docker run -d IMAGE_NAME` --- _Inicia um container em segundo plano._
- `$ docker run -it IMAGE_NAME` --- _Inicia um container interativo._
- `$ docker run --name CONTAINER_NAME IMAGE_NAME` --- _Inicia um container com um nome específico._
- `$ docker run -p HOST_PORT:CONTAINER_PORT IMAGE_NAME` --- _Mapeia uma porta do host para uma porta do container._
- `$ docker run -v HOST_DIR:CONTAINER_DIR IMAGE_NAME` --- _Monta um volume do host no container._
- `$ docker stop CONTAINER_ID_||_CONTAINER_NAME` --- _Interrompe um container em execução._
- `$ docker rm CONTAINER_ID_||_CONTAINER_NAME` --- _Remove um container._
- `$ docker kill $(docker ps -q)` --- _Para todos os containers em execução._
- `$ docker rm $(docker ps -a -q)` --- _Remove todos os containers._
- `$ docker exec -it CONTAINER_ID bash` --- _Inicia um terminal Bash dentro de um container pelo ID._
- `$ docker exec -it CONTAINER_NAME bash` --- _Inicia um terminal Bash dentro de um container pelo nome._
- `$ docker logs CONTAINER_ID_||_CONTAINER_NAME` --- _Exibe os logs de um container._
- `$ docker restart CONTAINER_ID_||_CONTAINER_NAME` --- _Reinicia um container._
- `$ docker pause CONTAINER_ID_||_CONTAINER_NAME` --- _Pausa todos os processos em execução em um container._
- `$ docker unpause CONTAINER_ID_||_CONTAINER_NAME` --- _Retoma todos os processos pausados em um container._
- `$ docker cp CONTAINER_ID:CONTAINER_PATH HOST_PATH` --- _Copia arquivos ou diretórios do container para o host._
- `$ docker cp HOST_PATH CONTAINER_ID:CONTAINER_PATH` --- _Copia arquivos ou diretórios do host para o container._
- `$ docker inspect CONTAINER_ID_||_CONTAINER_NAME` --- _Exibe informações detalhadas sobre um container._
- `$ docker stats CONTAINER_ID_||_CONTAINER_NAME` --- _Exibe estatísticas em tempo real sobre os recursos usados por um container._
- `$ docker top CONTAINER_ID_||_CONTAINER_NAME` --- _Exibe os processos em execução dentro de um container._
- `$ docker commit CONTAINER_ID_||_CONTAINER_NAME NEW_IMAGE_NAME` --- _Cria uma nova imagem a partir das alterações de um container._

### Comandos de imagens:

- `$ docker images` --- _Exibe as imagens Docker._
- `$ docker rmi IMAGE_ID` --- _Remove uma imagem._
- `$ docker rmi IMAGE_ID -f` --- _Força a remoção de uma imagem._
- `$ docker rmi $(docker images -q)` --- _Remove todas as imagens._
- `$ docker build -t IMAGE_NAME .` --- _Constrói uma nova imagem a partir de um Dockerfile no diretório atual._
- `$ docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]` --- _Marca uma imagem com uma nova tag._
- `$ docker pull IMAGE_NAME` --- _Baixa uma imagem do Docker Hub._
- `$ docker push IMAGE_NAME` --- _Envia uma imagem para um repositório remoto._
- `$ docker save -o IMAGE_NAME.tar IMAGE_NAME` --- _Salva uma imagem em um arquivo tar._
- `$ docker load -i IMAGE_NAME.tar` --- _Carrega uma imagem de um arquivo tar._
- `$ docker history IMAGE_NAME` --- _Exibe o histórico de camadas de uma imagem._

### Gerenciamento de volumes:

- `$ docker volume create VOLUME_NAME` --- _Cria um volume._
- `$ docker volume ls` --- _Lista todos os volumes._
- `$ docker volume rm VOLUME_NAME` --- _Remove um volume._
- `$ docker volume rm $(docker volume ls -q)` --- _Remove todos os volumes._
- `$ docker volume inspect VOLUME_NAME` --- _Exibe detalhes sobre um volume._
- `$ docker volume prune` --- _Remove todos os volumes não utilizados._

### Gerenciamento de networks:

- `$ docker network create NETWORK_NAME` --- _Cria uma rede._
- `$ docker network ls` --- _Lista todas as redes._
- `$ docker network rm NETWORK_NAME` --- _Remove uma rede._
- `$ docker network inspect NETWORK_NAME` --- _Exibe detalhes sobre uma rede._
- `$ docker network connect NETWORK_NAME CONTAINER_NAME` --- _Conecta um container a uma rede._
- `$ docker network disconnect NETWORK_NAME CONTAINER_NAME` --- _Desconecta um container de uma rede._
- `$ docker network prune` --- _Remove todas as redes não utilizadas._

### Configuração de permissões:

- `$ sudo groupadd docker` --- _Adiciona e verifica o grupo Docker._
- `$ sudo usermod -aG docker $USER` --- _Adiciona o usuário ao grupo Docker._
- `$ newgrp docker` --- _Atualiza o grupo do usuário para Docker._
- `$ sudo chown -R $USER:$USER .` --- _Fornece permissões ao usuário para o diretório atual._
- `$ sudo chmod 666 /var/run/docker.sock` --- _Permissão de leitura e gravação no socket Docker._

### Comandos de limpeza:

- `$ docker system prune` --- _Remove todos os containers, redes e volumes não utilizados._
- `$ docker image prune` --- _Remove todas as imagens não utilizadas._
- `$ docker container prune` --- _Remove todos os containers parados._
- `$ docker volume prune` --- _Remove todos os volumes não utilizados._
- `$ docker network prune` --- _Remove todas as redes não utilizadas._

### Outros comandos úteis:

- `$ docker system df` --- _Exibe a quantidade de espaço em disco usada por imagens, containers e volumes._
- `$ docker events` --- _Exibe eventos em tempo real do servidor Docker._
- `$ docker info` --- _Exibe informações detalhadas sobre o sistema Docker._
- `$ docker login` --- _Faz login em um repositório Docker._
- `$ docker logout` --- _Faz logout de um repositório Docker._
- `$ docker attach CONTAINER_ID_||_CONTAINER_NAME` --- _Anexa o terminal atual a um container em execução._
