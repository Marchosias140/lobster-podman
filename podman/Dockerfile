FROM ubuntu:latest

WORKDIR /home

RUN mkdir /home/user

WORKDIR /home/user

RUN apt update && apt upgrade -y
RUN apt install -y software-properties-common \
    findutils \
    coreutils \
    bash \
    fish \
    gawk \
    apt-transport-https \
    ca-certificates \
    gnupg \
    curl \
    wget \
    dotnet-runtime-8.0 \
    libgtk-4-1 \
    libadwaita-1-0 \
    libwebkit2gtk-4.1-0 \
    libgl1 \
    libpulse0 \
    pulseaudio-utils \
    alsa-utils \
    libgl1-mesa-dri \
    at-spi2-core \
    dbus-x11 \
    adwaita-icon-theme \
    fonts-dejavu \
    libwebkitgtk-6.0-4 \
    libnotify4 \
    libnss3 \
    libxss1 \
    xdg-utils \
    git \
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
