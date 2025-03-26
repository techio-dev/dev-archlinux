FROM ghcr.io/techio-dev/dev-archlinux:base
RUN pacman -S --noconfirm \
  go \
  gopls \
  gofumpt \
  sqlfluff \
  pgformatter \
  yaml-language-server \
  vscode-json-languageserver
ENV PATH="/root/go/bin:$PATH"
RUN go install golang.org/x/tools/cmd/goimports@latest
RUN go install github.com/segmentio/golines@latest
WORKDIR /workspaces
