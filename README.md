## Docker

- `$ sudo service docker start` --- _inicia o serviço docker_
- `$ docker-compose up -d` --- _sobe a aplicação_
- `$ docker-compose down` --- _derruba a aplicação_
- `$ docker ps` --- _exibe containeres em execução_
- `$ docker images` --- _exibe imagens em execução_
- `$ docker container list -a` --- _lista todos os containeres, inclusive os desligados_
- `$ docker stop _CONTAINER ID` --- _interrompe um container em execução_
- `$ docker-compose stop` --- _interrompe todos containeres em execução sem remover_
- `$ docker kill $(docker ps -q) `--- _para todos os containers e imagens_
- `$ docker rm _CONTAINER ID` --- _remove container_
- `$ docker rmi _IMAGE ID` --- _remove imagem_
- `$ docker rmi _IMAGE ID -f` --- _força remover imagem_
- `$ docker rm $(docker ps -a -q) `--- _finaliza todos os containeres_
- `$ docker rmi $(docker images -q) `--- _finaliza todas as imagens_

#### Para iniciar automaticamente o Docker e o Containerd na inicialização de outras distribuições, use os comandos abaixo:
- `$ sudo systemctl enable docker.service` --- _habilita serviço docker_
- `$ sudo systemctl enable containerd.service` --- _habilita serviço containerd_
