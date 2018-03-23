## Docker Help

## Mostra todos os dados do container criado
```
docker inspect <nome do conteiner>
```

##Criar uma imagem nomeando
```
docker build -t <nome imagem> <caminho do Dockerfile>
```

## Remover todas os conteiners exited
```
docker rm $( docker ps -q -f status=exited)
```

## Remover Imagens sem TAG
```
docker rmi $( docker images -q -f dangling=true)
```

## Registrando um repositorio remoto
Basta logar e digitar o login e senha

** Caso você esteja utilizando no MAC ou Windows vá em settings do docker e adicione o repositorio lá

```
docker login cvcregistry01.xyz.com.br:5000
```

## Adicionando certificado no MacOSX
***Crie um diretório em ~/.boot2docker/certs/ ex:***

```
mkdir ~/.boot2docker/certs/cvcregistry01.xyz.com.br:5000
```

***Crie um o certificado***
```
touch ~/.boot2docker/certs/cvcregistry01.xyz.com.br:5000/ca.crt
```
Adicione o dados do certificado e pronto está funcionando

# Mudando o IP da docker0

Crie o arquivo /etc/docker/daemon.json

```json
{
   "bip": "172.18.12.1/24"
}
```
 Restart do daemon: systemctl restart docker

# Atualizando Docker no Linux

```
sudo apt-get upgrade docker-engine
```

