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
RUN git clone https://aur.archlinux.org/yay.git
RUN cd yay
RUN makepkg -si
RUN yay -S mods
WORKDIR /workspaces
