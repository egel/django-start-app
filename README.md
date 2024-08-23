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
cd myapp
pip install -r requirements.txt
python manage.py runserver  # open app in default localhost:8000
```

or build locally via Dockerfile:

```bash
docker build -t django-start-app -f Dockerfile-myapp .
docker run --rm -d -p 8000:8000 django-start-app:5.1 # or :latest
```

or pull the image from dockerhub:

```bash
docker run --rm -d -p 8000:8000 egel/django-start-app:latest
```

### rebuild images

macOS

```bash
cd myapp
docker buildx create --name my-builder
docker buildx use my-builder
docker buildx build --platform linux/amd64,linux/arm64,linux/arm/v7 -t egel/django-start-app:5.1 -f Dockerfile-myapp . --push
```

## License

BSD 3-Clause License
