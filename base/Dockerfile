FROM gcc

RUN apt update && apt upgrade -y && \
    apt install -y cmake

RUN useradd -ms /bin/bash chris

RUN mkdir /app

RUN chown chris:chris /app

WORKDIR /app

USER chris
