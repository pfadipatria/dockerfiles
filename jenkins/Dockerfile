FROM jenkins


COPY plugins.txt /plugins.txt

RUN /usr/local/bin/plugins.sh /plugins.txt


COPY fstab /fstab.append

USER root

RUN apt-get update && \
  apt-get install bindfs -y && \
  apt-get clean && \
  cat /fstab.append >> /etc/fstab && \
  echo 'fuse' >> /etc/modules && \
  rm /fstab.append

USER jenkins
