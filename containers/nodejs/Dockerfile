FROM ghcr.io/techio-dev/dev-archlinux:base

RUN pacman -S --noconfirm \
  nodejs-lts-jod \
  npm \
  svelte-language-server \
  vscode-json-languageserver
RUN npm install -g bun
ENV PATH="/root/.bun/bin:$PATH"
RUN bun install -g tailwindcss-language-server
RUN bun install -g @prisma/language-server
RUN bun install -g @vtsls/language-server
WORKDIR /workspaces
