FROM pfadipatria/ruby-1.9.3-jenkins-slave

RUN apt-get update && \
 apt-get install openssh-server -y && \
 mkdir /var/run/sshd && \
 adduser jenkins -m && \
 echo "jenkins:jenkins" | chpasswd
 
EXPOSE 22

ENTRYPOINT ["/usr/bin/sshd", "-D"]
