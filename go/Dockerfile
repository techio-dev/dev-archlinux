FROM ghcr.io/techio-dev/dev-archlinux:latest
RUN echo "dev ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
USER dev
RUN pacman -S --noconfirm \
  go \
  gopls \
  gofumpt \
  sqlfluff \
  pgformatter \
  yaml-language-server \
  vscode-json-languageserver
ENV PATH="/home/dev/go/bin:$PATH"
RUN yay -S --noconfirm \
  golines
RUN go install golang.org/x/tools/cmd/goimports@latest
WORKDIR /workspaces
