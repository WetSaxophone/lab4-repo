# setting base image to ubuntu
FROM ubuntu:latest

# update source list
RUN apt-get update

# python and pip
RUN apt-get install -y python3 python3-pip 
RUN pip3 install --upgrade pip

ADD /myapp /myapp

RUN pip3 install -r myapp/requirements.txt

# EXPOSE 5000
EXPOSE 5000

WORKDIR /myapp

CMD python3 app.py
