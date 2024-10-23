# [Choice] Ubuntu version (use jammy on local arm64/Apple Silicon): jammy, focal
ARG VARIANT="jammy"
FROM buildpack-deps:${VARIANT}-curl
LABEL dev.containers.features="common"

# Install Flatpak and add Flathub repository
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends flatpak flatpak-builder \
    && flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo