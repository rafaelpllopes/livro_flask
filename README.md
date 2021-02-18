# Livro Flask
Aplicação em python, feita com base no livro Flask de A a Z.

## Ambiente

### Python
- 3.8.2
- flask
- SQLAlchemy

### Banco de dados
Possuir docker instalado, criar um container para o MySQL

```sudo docker run --name mysqldb -h mysqldb -p 3306:3306 -e MYSQL_ROOT_PASSWORD=mysql -d mysql```
```sudo docker exec -it mysqldb /bin/bash```
```mysql -u root -p```
```CREATE DATABASE livro_flask CHARACTER SET UTF8 collate utf8_general_ci```

### Libs
```sudo apt-get install libmysqlclient-dev```
```sudo apt-get install gcc```
```apt-get install python3-pip```

### Configuração e execução
1. ```python -m venv .venv```
2. ```source .venv/bin/activate```
3. ```pip install -r requirements.txt```
4. ```flask run```

### Criar variavel de ambiente FLASK_ENV
```export FLASK_ENV=development``` para desenvolvimento
```export FLASK_ENV=testing``` para teste
```export FLASK_ENV=production``` para produção
