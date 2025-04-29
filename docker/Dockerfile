# Dockerfile
FROM codercom/code-server:latest

USER root
RUN apt-get update && \
    apt-get install -y python3 python3-pip git && \
    apt-get clean

# Instala la extensión de Python y GitLens para code-server
RUN code-server --install-extension ms-python.python
RUN code-server --install-extension eamodio.gitlens

# Cambia a usuario normal
USER coder

WORKDIR /home/coder/project

RUN git clone https://github.com/kenchic/PythonMCP.git .
