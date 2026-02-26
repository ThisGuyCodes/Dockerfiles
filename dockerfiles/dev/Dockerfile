FROM ubuntu:jammy

ADD https://packagecloud.io/install/repositories/ookla/speedtest-cli/script.deb.sh /tmp/setup_speedtest.sh
RUN apt update \
    && chmod +x /tmp/setup_speedtest.sh \
    && /tmp/setup_speedtest.sh \
    && rm /tmp/setup_speedtest.sh \
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
