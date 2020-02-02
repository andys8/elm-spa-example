FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:12

# User configured in Dockerfile
# <https://github.com/andys8/vscode-dev-containers/blob/cd4e2d538d15efc1f39c160bd106d83fbe28e8e3/containers/javascript-node-12/.devcontainer/Dockerfile#L15>
ARG USERNAME=node

# Elm 0.19.1
ARG ELM_VERSION=latest-0.19.1
ARG ELM_TEST_VERSION=latest-0.19.1
ARG ELM_FORMAT_VERSION=latest-0.19.1

# Avoid warnings by switching to noninteractive
ENV DEBIAN_FRONTEND=noninteractive

RUN sudo -u ${USERNAME} npm install --global \
    elm@${ELM_VERSION} \
    elm-test@${ELM_TEST_VERSION} \
    elm-format@${ELM_FORMAT_VERSION}

# Switch back to dialog for any ad-hoc use of apt-get
ENV DEBIAN_FRONTEND=dialog
