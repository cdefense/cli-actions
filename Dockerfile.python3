FROM python:3.8-slim

RUN mkdir /app
RUN apt-get update && apt-get install curl -y
RUN curl https://raw.githubusercontent.com/CloudDefenseAI/cd/master/latest/cd-latest-linux-x64.tar.gz > /tmp/cd-latest-linux-x64.tar.gz \
        && tar -C /usr/local/bin -xzf /tmp/cd-latest-linux-x64.tar.gz \
        && chmod +x /usr/local/bin/cdefense
WORKDIR /app
VOLUME /app
ENV LANG=python

ENTRYPOINT ["cdefense"]
