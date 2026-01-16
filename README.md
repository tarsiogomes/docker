# Docker 

<a id="volta_topo"></a>

# Sumario

- [Instalando e configurando o Docker](#ref_titulo_01)
    - [Containers](#ref_sub_01)
        - [Gerenciamento de Containers](#gerenciamento-de-containers)
    - [Images](#ref_sub_02)
    - [Network](#ref_sub_03)


# Instalando e configurando o Docker <a id="ref_titulo_01"></a>

> A versão do Docker Desktop está disponível para a plataforma Microsoft Windows 11 21H2 ou superior e Windows 10 21H1 (build 19043) ou supeior, segue link para documentação:

<https://docs.docker.com/desktop/install/windows-install/>


## Containers <a id="ref_sub_01"></a>

### Gerenciamento de containers <a id="gerenciamento-de-containers">

>Para criar container com base em alguma imagem do Docker Hub
~~~
docker run ubuntu bash
~~~
>Consultar containers em execução
~~~
docker ps
~~~
>Para consultar todos os containers criados
~~~
docker ps -a
~~~
>Para consultar o tamanho virtual e real de cada container:
~~~
docker ps -s
~~~
>Comando para remover um ou varios containers
~~~
docker rm <id_container>
~~~
>Comando para remover varios containers (utlize o argumento --force caso não queira parar cada container)
~~~
docker rm $(docker container ls -qa) --force
~~~
> Este comando serve para executar e reiniciar o container sempre que acontecer interrupção do host

Neste exemplo foi criado um container com uma image do Debian definido para reiniciar sempre, além do nome ctr-ansible-01:
~~~
docker run -dti --restart=always --name ctr-ansible-01 debian
~~~







## Images <a id="ref_sub_02"></a>

>Para consultar as images em seu repositório do Docker
~~~
docker images
~~~

## Network <a id="ref_sub_02"></a>

>Network entre os containers

[Voltar Topo](#volta_topo)