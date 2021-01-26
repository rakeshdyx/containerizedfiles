FROM debian:jessie-slim

RUN apt-get update                              &&\
apt-get install -y --no-install-recomendeds       \
cowsay                                            \
screenfetch                                     &&\
rm -rf /var/lib/apt/lists/*

ENV PATH "$PATH:/usr/games"

CMD cowsay "Yo, CMD !!"