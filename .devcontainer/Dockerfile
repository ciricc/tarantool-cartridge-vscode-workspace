FROM mcr.microsoft.com/devcontainers/base:jammy

RUN apt-get update

# Install dev dependencies
RUN apt-get install -y git build-essential curl

RUN curl -L https://tarantool.io/release/2/installer.sh | sudo -E bash -s -- --repo-only

# Install tarantool dependencies for development and running
RUN sudo apt-get install -y cartridge-cli tarantool

# Clone tarantool lua library for sumneko bindings
RUN git clone https://github.com/ochaton/vscode-tarantool.git /var/lib/vscode-tarantool