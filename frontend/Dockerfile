FROM ubuntu
MAINTAINER HackOregon
COPY . /usr/src/app
RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup | sudo bash -
RUN apt-get install -y build-essential nodejs nginx
RUN cd /usr/src/app && npm install && npm install -g grunt-cli && grunt && rm /etc/nginx/sites-enabled/default
COPY nginx-default /etc/nginx/sites-enabled/default
WORKDIR /usr/src/app
CMD ["nginx", "-g", "daemon off;"]
