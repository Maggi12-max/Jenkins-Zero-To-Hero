FROM python:3

RUN python -m ensurepip --upgrade
RUN pip install setuptools==65.5.0  # brings distutils back
RUN pip install django==3.2

WORKDIR /app
COPY . .
RUN python manage.py migrate
EXPOSE 8000
CMD ["python","manage.py","runserver","0.0.0.0:8000"]


