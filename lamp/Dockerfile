FROM ubuntu:18.04
ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt upgrade -y
RUN apt install htop apache2 php libapache2-mod-php php-mysql curl git nano -y
RUN apt install -y locales locales-all
RUN locale-gen --purge en_US.UTF-8
WORKDIR /var/lamp-lahtp
COPY ./data /var/lamp-lahtp/

EXPOSE 80
CMD ./script/entry.sh