FROM ghcr.io/techio-dev/dev-archlinux:base

RUN pacman -S --noconfirm \
  nodejs-lts-jod \
  npm \
  svelte-language-server \
  vscode-json-languageserver
RUN bun install -g tailwindcss-language-server
RUN echo "dev ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
USER dev
RUN yay -S --noconfirm \
  bun \
  prisma-language-server \
  vtsls
RUN echo "root ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
USER root
WORKDIR /workspaces
