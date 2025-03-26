FROM ghcr.io/techio-dev/dev-archlinux:base
RUN pacman -S --noconfirm \
  helm
RUN helm plugin install https://github.com/chartmuseum/helm-push
RUN helm repo add techio https://chartmuseum.fly.dev
WORKDIR /workspaces
