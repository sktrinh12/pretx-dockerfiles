FROM jupyter/datascience-notebook:latest

USER root

RUN apt-get update && apt-get install -y vim && apt-get clean && rm -rf /var/lib/apt/lists/*

USER ${NB_UID}

RUN pip install jupyterlab_vim

RUN pip install jupyterlab-theme-solarized-dark

RUN jupyter labextension enable jupyterlab_vim && \
    jupyter labextension enable jupyterlab-theme-solarized-dark

RUN mkdir -p ~/.jupyter/lab/user-settings/@jupyterlab/apputils-extension && \
    echo '{"theme": "JupyterLab Solarized Dark"}' > ~/.jupyter/lab/user-settings/@jupyterlab/apputils-extension/themes.jupyterlab-settings

ENV EDITOR=vim
