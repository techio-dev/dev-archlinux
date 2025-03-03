FROM ghcr.io/techio-dev/dev-archlinux:base
RUN pacman -S --noconfirm \
  go \
  gopls \
  gofumpt \
  sqlfluff \
  pgformatter \
  yaml-language-server \
  vscode-json-languageserver
RUN go install golang.org/x/tools/cmd/goimports@latest
ENV PATH="/root/go/bin:$PATH"
USER dev
RUN yay -S --noconfirm \
  golines
USER root
WORKDIR /workspaces
