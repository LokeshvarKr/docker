From ubuntu:20.04
LABEL name="Lokesh"
LABEL email="lokes@xyz.com"
ENV NAME lokesh
ENV PASS password@123
RUN mkdir -p /var/run/sshd
RUN apt-get update && apt-get install -y openssh-server
RUN useradd -d /home/lokesh -g root -G sudo -m -p $(echo "$PASS" | openssl passwd -1 -stdin) $NAME
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]