FROM ghcr.io/techio-dev/dev-archlinux:latest

RUN pacman -S --noconfirm \
  go \
  gopls \
  gofumpt \
  sqlfluff \
  pgformatter \
  yaml-language-server \
  vscode-json-languageserver
RUN go install golang.org/x/tools/cmd/goimports@latest
WORKDIR /workspaces
