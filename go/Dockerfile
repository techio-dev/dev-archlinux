FROM ghcr.io/techio-dev/dev-archlinux:latest

RUN pacman -S --noconfirm \
  go \
  gopls \
  gofumpt \
  sqlfluff \
  pgformatter \
  yaml-language-server \
  vscode-json-languageserver
ENV PATH="$HOME/go/bin:$PATH"
RUN yay -S --noconfirm \
  golines
RUN go install golang.org/x/tools/cmd/goimports@latest
WORKDIR /workspaces
