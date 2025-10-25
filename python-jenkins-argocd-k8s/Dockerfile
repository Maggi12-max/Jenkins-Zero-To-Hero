FROM python:3.14-slim

# Install distutils and other build essentials
RUN apt-get update && apt-get install -y python3-distutils build-essential && rm -rf /var/lib/apt/lists/*
RUN pip install django==3.2
WORKDIR /app
COPY . .

RUN python manage.py migrate
EXPOSE 8000
CMD ["python","manage.py","runserver","0.0.0.0:8000"]


