FROM ghcr.io/techio-dev/dev-archlinux:latest
USER dev
RUN pacman -S --noconfirm \
  nodejs-lts-jod \
  npm \
  svelte-language-server \
  vscode-json-languageserver
RUN yay -S --noconfirm \
  bun \
  prisma-language-server \
  vtsls
RUN bun install -g tailwindcss-language-server
WORKDIR /workspaces
