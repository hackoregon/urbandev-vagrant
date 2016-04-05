FROM ubuntu:14.04
MAINTAINER HackOregon
COPY . /usr/src/app
RUN apt-get update && apt-get upgrade -y && apt-get install -y build-essential nodejs nodejs-legacy npm uwsgi
RUN cd /usr/src/app && npm install && npm install -g grunt-cli && grunt
# COPY nginx-default /etc/nginx/sites-enabled/default
ADD run.sh /
WORKDIR /usr/src/app
# ENTRYPOINT [ "/run.sh" ]
