# django-start-app

A simple Django 5.1 app following good practices.

## Dev

```bash
# environment
pyenv install 3.12.5
pip install virtualenv
virtualenv venv
source venv/bin/activate

# app
pip install -r requirements.txt
python myapp/manage.py runserver  # open app in default localhost:8000
```

or build locally via Dockerfile:

```bash
docker build -t django-start-app .
docker run -d -p 8000:8000 django-start-app:latest # default localhost:8000
```

## License

BSD 3-Clause License
