FROM jenkins/jenkins:lts

USER root

RUN mkdir -p /tmp/download && \
curl -L https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz | tar zx -C /tmp/download && \
rm -rf /tmp/download/docker/dockerd && \
mv /tmp/download/docker/docker* /usr/local/bin/ && \
groupadd -g 995 docker && \
usermod -aG wheel,docker jenkins

