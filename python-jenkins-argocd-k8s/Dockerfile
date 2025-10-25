FROM python:3.11-bullseye
RUN pip install django==3.2

WORKDIR /app
COPY python-jenkins-argocd-k8s/ .
RUN python manage.py migrate
EXPOSE 8000
CMD ["python","manage.py","runserver","0.0.0.0:8000"]


