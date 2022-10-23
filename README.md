**Instruções para execução do desafio:**
Neste projeto o expert utilizou o ***Docker Compose*** para executar uma aplicação HTML em um Container Apache. Você poderá ir além e fazer alterações mais robustas ao seu projeto, estilizando sua página e utilizando seus conhecimentos em (HTML, CSS e JS). Você também pode buscar outras formas para executar seu arquivo HTML em outras Linguagens de Programação.<br>
<br>
**Execução**:
Numa máquina virtual Ubuntu, criada no Virtual Box:
- Criei a pasta: /compose/desafio2
- Criei a pasta: /compose/desafio2/website
- Na pasta /compose/desafio, criei o arquivo: docker-compose.yml com o conteúdo de exemplo do github do professor.

    version: '3.9'
    services:
      apache:
        image: httpd:latest
        container_name: my-apache-app
        ports:
        - '80:80'
        volumes:
        - ./website:/usr/local/apache2/htdocs

- Na pasta /compose/desafio/website, fiz o clone do meu repositório apeperia (do curso da alura): [https://github.com/szalbuque/apeperia](https://github.com/szalbuque/apeperia)


Voltei para a pasta /compose/desafio e rodei o comando:
> docker-compose up

Deu erro porque já tinha um container com o mesmo nome. 
Usei o comando 
> docker container prune

Parei o apache com  systemctl stop apache2
Rodei novamente o docker-compose up, sem erro.
Funcionou.

Criei um repositório no meu github: https://github.com/szalbuque/web_app_docker_compose

Fiz o push.# web_app_docker_compose
