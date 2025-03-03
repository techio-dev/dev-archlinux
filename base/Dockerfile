FROM archlinux:latest

RUN pacman -Syu --noconfirm
RUN pacman -S --noconfirm \
  base-devel \
  neovim \
  git \
  ripgrep \
  fzf \
  fd \
  unzip \
  curl \
  lazygit \
  go-task \
  jq
RUN useradd -m dev && echo "dev ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
USER dev
RUN mkdir -p /tmp/yay-build
RUN git clone https://aur.archlinux.org/yay.git /tmp/yay-build/yay
RUN cd /tmp/yay-build/yay && makepkg -si --noconfirm
RUN rm -rf /tmp/yay-build
RUN yay -S --noconfirm \
  mods
RUN echo "root ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
USER root
WORKDIR /workspaces
