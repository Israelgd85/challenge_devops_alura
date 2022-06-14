FROM python:3.6

ENV PYTHONDONTWRITEBYTECONDE=1
ENV PYTHONUNBUFFERED=1
RUN apt-get update
WORKDIR /code
COPY requirements.txt /code/
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN pip install -r requirements.txt
COPY . /code/
EXPOSE 8000
#CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
