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
  jq
WORKDIR /workspaces
