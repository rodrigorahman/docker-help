##Docker Help

##Mostra todos os dados do container criado
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
