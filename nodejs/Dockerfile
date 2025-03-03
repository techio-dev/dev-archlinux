FROM ghcr.io/techio-dev/dev-archlinux:base

RUN pacman -S --noconfirm \
  nodejs-lts-jod \
  npm \
  svelte-language-server \
  vscode-json-languageserver
RUN bun install -g tailwindcss-language-server
USER dev
RUN yay -S --noconfirm \
  bun \
  prisma-language-server \
  vtsls
USER root
WORKDIR /workspaces
