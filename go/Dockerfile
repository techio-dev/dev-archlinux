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
RUN go install github.com/segmentio/golines@latest
WORKDIR /workspaces
