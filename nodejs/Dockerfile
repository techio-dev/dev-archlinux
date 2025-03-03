FROM ghcr.io/techio-dev/dev-archlinux:latest

RUN pacman -S --noconfirm \
  nodejs-lts-jod \
  npm \
  svelte-language-server \
  vscode-json-languageserver
RUN npm install -g bun
RUN bun install -g tailwindcss-language-server
RUN bun install -g @prisma/language-server
RUN bun install -g @vtsls/language-server
WORKDIR /workspaces
