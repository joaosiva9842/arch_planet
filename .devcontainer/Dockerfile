FROM archlinux:latest

RUN pacman -Syu --noconfirm \
    base-devel \
    git \
    sudo \
    curl \
    wget \
    nodejs \
    npm \
    && pacman -Scc --noconfirm

ARG USERNAME=codespace
RUN useradd -m -s /bin/bash "$USERNAME" \
    && echo "$USERNAME ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/$USERNAME

USER codespace
WORKDIR /workspaces/${localWorkspaceFolderBasename}
