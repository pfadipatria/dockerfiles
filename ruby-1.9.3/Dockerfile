FROM melopos/docker-rvm-ruby-1.9.3

RUN apt-get update && \
  apt-get upgrade -y && \
  apt-get install libmysqlclient-dev -y
  
RUN gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 && \
  rvm get stable
