FROM ubuntu:latest

WORKDIR /home

RUN mkdir /home/user

WORKDIR /home/user

RUN apt update && apt upgrade -y
 
RUN apt install -y software-properties-common \
    curl \
    libpulse0 \
    pulseaudio-utils \
    alsa-utils \
    wget \
    dotnet-runtime-8.0 \
    git \
    fonts-dejavu \
    sed \
    mpv \
    grep \
    ffmpeg \
    fzf \
    aria2 \
    yt-dlp \
    && rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/justchokingaround/lobster.git
WORKDIR /home/user/lobster
RUN chmod +x lobster.sh
RUN mv lobster.sh lobster
RUN cp lobster /usr/bin
WORKDIR /home/user

CMD ["/usr/bin/lobster"]
