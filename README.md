# Livro Flask
Aplicação em python, feita com base no livro Flask de A a Z.

## Ambiente

### Python
- 3.8.2
- flask
- SQLAlchemy

### Banco de dados
Possuir docker instalado, criar um container para o MySQL

1. ```sudo docker run --name mysqldb -h mysqldb -p 3306:3306 -e MYSQL_ROOT_PASSWORD=mysql -d mysql```
2. ```sudo docker exec -it mysqldb /bin/bash```
3. ```mysql -u root -p```
4. ```CREATE DATABASE livro_flask CHARACTER SET UTF8 collate utf8_general_ci;```

### Libs
1. ```sudo apt-get install libmysqlclient-dev```
2. ```sudo apt-get install gcc```
3. ```apt-get install python3-pip```

### Configuração e execução
1. ```python -m venv .venv```
2. ```source .venv/bin/activate```
3. ```pip install -r requirements.txt```
4. ```flask run```

### Executar o migrate
```python migrate.py db init``` comando é executado somente uma vez, caso não tenha nada na pasta migrations
```python migrate.py db migrate```
```python migrate.py db upgrade```

### Criar variavel de ambiente FLASK_ENV
```export FLASK_ENV=development``` para desenvolvimento
```export FLASK_ENV=testing``` para teste
```export FLASK_ENV=production``` para produção

## Estrutura

```
├── admin
│   ├── Admin.py
│   └── Views.py
├── app.py
├── config.py
├── controller
│   ├── Email.py
│   ├── Product.py
│   └── User.py
├── migrate.py
├── migrations
│   ├── alembic.ini
│   ├── env.py
│   ├── __pycache__
│   │   └── env.cpython-38.pyc
│   ├── README
│   ├── script.py.mako
│   └── versions
│       ├── 1a00c7b88846_.py
│       └── __pycache__
│           └── 1a00c7b88846_.cpython-38.pyc
├── model
│   ├── Category.py
│   ├── Product.py
│   ├── Role.py
│   └── User.py
├── __pycache__
│   ├── app.cpython-38.pyc
│   └── config.cpython-38.pyc
├── README.md
├── requirements.txt
├── run.py
├── static
│   └── css
│       ├── home.css
│       └── login.css
└── templates
    ├── home_admin.html
    ├── login.html
    ├── new_password.html
    └── recovery.html
```
