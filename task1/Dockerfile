# Ubuntu latest version
FROM ubuntu:latest

# Update and upgrade && install python3 && pip3
RUN apt-get update && apt-get upgrade -y \
python3 \
python3-pip

# Remove EXTERNALLY-MANAGED to avoid errors with pip
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# install flask
RUN pip3 install flask

# set working directory
WORKDIR /app

# copy api.py in working directory
COPY ./api.py /app/

# run Flask app
CMD ["python3", "api.py"]
