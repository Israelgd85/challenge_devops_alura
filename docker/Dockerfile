FROM python:3.6


# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Create workdir and copy from you current dir to container workdir
WORKDIR /code
COPY . .

# Run commands
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt
RUN python manage.py makemigrations && python manage.py migrations

