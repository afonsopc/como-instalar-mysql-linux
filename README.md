### Pré-requisitos:
Certifica-te de que tens o Docker instalado na tua máquina. Se ainda não o tens, podes seguir as instruções de instalação [aqui](https://docs.docker.com/get-docker/).

### Passos para criar um servidor MySQL com Docker:

1. **Criar um container MySQL:**
   Agora, cria um container MySQL com o seguinte comando:

   ```bash
   docker run -d --name meu-servidor-mysql -e MYSQL_ROOT_PASSWORD=minhapassword -p 3306:3306 mysql
   ```

   Este comando cria um container chamado "meu-servidor-mysql", define a senha do root como "minhapassword" e mapeia a porta 3306.

2. **Verificar o estado do container:**
   Podes verificar se o teu container está a correr usando o seguinte comando:

   ```bash
   docker ps
   ```

   Se tudo estiver correto, deverás ver o teu container listado com o estado "Up".

3. **Aceder ao MySQL:**
   Podes aceder ao servidor MySQL a partir do teu terminal ou através de uma ferramenta de gestão como o MySQL Workbench. Usa o seguinte comando para aceder ao MySQL:

   ```bash
   docker exec -it meu-servidor-mysql mysql -uroot -p
   ```

   Ser-te-á pedido a senha, que definiste como "minhapassword".

4. **Criar uma base de dados:**
   Dentro do terminal do MySQL, podes criar uma base de dados com o seguinte comando:

   ```sql
   CREATE DATABASE minha_base_de_dados;
   ```

   Substitui "minha_base_de_dados" pelo nome desejado.
