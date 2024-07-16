FROM ubuntu:22.04

# Aktualisiere die Paketliste und installiere erforderliche Pakete
RUN apt-get update && \
    apt-get install -y \
    software-properties-common \
    wget \
    build-essential \
    libssl-dev \
    zlib1g-dev \
    libbz2-dev \
    libreadline-dev \
    libsqlite3-dev \
    libncurses5-dev \
    libncursesw5-dev \
    xz-utils \
    tk-dev \
    libffi-dev \
    liblzma-dev \
    curl \
    git && \
    apt-get clean

# Lade und installiere Python 3.12.4
RUN wget https://www.python.org/ftp/python/3.12.4/Python-3.12.4.tgz && \
    tar xzf Python-3.12.4.tgz && \
    cd Python-3.12.4 && \
    ./configure --enable-optimizations && \
    make -j$(nproc) && \
    make altinstall

# Aktualisiere pip
RUN python3.12 -m ensurepip && \
    python3.12 -m pip install --upgrade pip

# Setze den Arbeitsverzeichnis
WORKDIR /app

# Kopiere den Inhalt des aktuellen Verzeichnisses in das Container-Verzeichnis /app
COPY . /app