# create image based on Python 3.8
FROM python:3.8

# expose ports 
EXPOSE 5000

# tell Python not to generate .pyc
ENV PYTHONDONTWRITEBYTECODE 1

# turn off buffering
ENV PYTHONUNBUFFERED 1

# install requirements using pip
ADD requirements.txt .
RUN python -m pip install -r requirements.txt

# set working directoryand add the Flask API files 
WORKDIR /app
ADD . /app