### Projeto

Mini "YouTube" que possibilitará fazermos o gerenciamento, upload, conversão e playback dos vídeos

- Comunicação assíncrona entre microsserviços
- Conversor de vídeo multithreading
- Python com Django
- Frontend utilizando Next.js
- Containers com Docker

**Área administrativa** - Django

**Vídeo Transcoder** - Go

**Mensageria** - RabbitMQ

**Frontend / Vídeo Playback** - Next.js

**Docker**

#### Intalando o gerenciador de versão Python

```bash
sudo apt update

sudo apt-get install build-essential zlib1g-dev libffi-dev libssl-dev libbz2-dev libreadline-dev libsqlite3-dev liblzma-dev

asdf plugin add python
asdf install python 3.12.6
asdf global python 3.12.6
```

#### Rodar a aplicação

Coloque a variável PIPENV_VENV_IN_PROJECT no seu .bashrc ou .zshrc:

```bash
export PIPENV_VENV_IN_PROJECT=1
```

comando para usar python localmente
```bash
asdf local python 3.12.6
pip install pipenv
pipenv install django
pipenv shell
django-admin startproject videos
```

Levante os containers do PostgreSQL e PGAdmin:

```bash
docker-compose up -d
```

Instale o Pipenv:

```bash
pip install pipenv
```

Instale as dependências:

```bash
pipenv install
```

A partir daqui, precisamos sempre rodar os comandos dentro do ambiente virtual do Pipenv:

```bash
pipenv shell
```

Rode as migrações do Django:

```bash
python manage.py migrate
```

Crie um superusuário:

```bash
python manage.py createsuperuser
```

Rode o servidor:

```bash
python manage.py runserver
```

Acesse o admin em http://localhost:8000/admin.
