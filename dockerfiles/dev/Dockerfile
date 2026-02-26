FROM ubuntu:jammy

RUN apt-get update \
    && apt-get install -y curl \
    && curl -s https://packagecloud.io/install/repositories/ookla/speedtest-cli/script.deb.sh | bash \
    && sed -i s/noble/jammy/g /etc/apt/sources.list.d/ookla_speedtest-cli.list \
    && apt-get update \
    && apt-get install -y \
    speedtest \
    neovim \
    unzip \
    zstd \
    zsh \
    && apt-get upgrade -y

ENTRYPOINT ["/bin/zsh"]
CMD ["sleep", "infinity"]
