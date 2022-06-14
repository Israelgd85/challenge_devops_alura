FROM python:3

ENV PYTHONDONTWRITEBYTECONDE=1
ENV PYTHONUNBUFFERED=1
RUN apt-get update
WORKDIR /code
COPY ./app/requirements.txt /code/
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt
COPY ./app/ /code/
EXPOSE 8000
ENTRYPOINT ["python", "manage.py", "runserver", "0.0.0.0:8000"]
