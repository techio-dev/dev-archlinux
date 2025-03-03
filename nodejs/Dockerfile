FROM ghcr.io/techio-dev/dev-archlinux:latest

RUN pacman -S --noconfirm \
  nodejs-lts-jod \
  npm \
  svelte-language-server \
  vscode-json-languageserver
RUN yay -S bun
RUN yay -S prisma-language-server
RUN yay -S vtsls
RUN bun install -g tailwindcss-language-server
WORKDIR /workspaces
