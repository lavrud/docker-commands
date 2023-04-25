<img height="100em" src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Docker_%28container_engine%29_logo.svg/1280px-Docker_%28container_engine%29_logo.svg.png" >

## Docker WSL2

#### Alguns comandos básicos:
- `$ sudo service docker start` --- _inicia o serviço docker_
- `$ sudo service docker status` --- _verifica o status do serviço docker_
- `$ docker-compose up -d` --- _sobe a aplicação_
- `$ docker-compose down` --- _derruba a aplicação_
- `$ docker-compose stop` --- _interrompe todos containeres em execução sem remover_
- `$ docker-composer exec _CONTAINER NAME_ sh `--- _acessa o container dentro do docker_
- `$ docker ps` --- _exibe containeres em execução_
- `$ docker images` --- _exibe imagens em execução_
- `$ docker container list -a` --- _lista todos os containeres, inclusive os desligados_
- `$ docker stop _CONTAINER ID_` --- _interrompe um container em execução_
- `$ docker kill $(docker ps -q) `--- _para todos os containers e imagens_
- `$ docker rm _CONTAINER ID_` --- _remove container_
- `$ docker rmi _IMAGE ID_` --- _remove imagem_
- `$ docker rmi _IMAGE ID_ -f` --- _força remover imagem_
- `$ docker rm $(docker ps -a -q) `--- _remove todos os containeres_
- `$ docker rmi $(docker images -q) `--- _remove todas as imagens_
- `$ docker exec -it _CONTAINER ID_ `--- _inicia um terminal Bash dentro de um container_

#### Para iniciar automaticamente o Docker e o Containerd na inicialização de outras distribuições, use os comandos abaixo:
- `$ sudo service enable docker.service` --- _habilita serviço docker_
- `$ sudo service enable containerd.service` --- _habilita serviço containerd_

#### Dando permissão ao usuário para ler e gravar ao docker:
- `$ sudo newgroup docker` --- _Novo grupo Docker_
- `$ sudo groupadd docker` --- _Adiciona && Verifica grupo Docker_
- `$ sudo usermod -aG docker $USER` --- _Inserindo usuário ao grupo_
- `$ sudo chown -R $USER:$USER .` --- _Fornecendo permissões ao usuário
- `$ sudo chmod 666 /var/run/docker.sock` --- _Permissão de leitura e gravação_
