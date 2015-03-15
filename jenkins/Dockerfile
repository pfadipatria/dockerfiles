FROM jenkins


COPY plugins.txt /plugins.txt

RUN /usr/local/bin/plugins.sh /plugins.txt


COPY fstab /fstab.append

RUN apt-get install bindfs && \
  cat /fstab.append >> /etc/fstab && \
  echo 'fuse' >> /etc/modules && \
  rm /fstab.append

