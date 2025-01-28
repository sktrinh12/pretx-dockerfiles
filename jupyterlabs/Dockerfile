FROM jupyter/datascience-notebook:latest

USER root

RUN apt-get update && \
    apt-get install -y vim cmake && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN conda install -y -c conda-forge r-rpostgres 
RUN Rscript -e "install.packages('DBI', repos='https://cran.r-project.org')"

USER ${NB_UID}

RUN Rscript -e "install.packages(c('FactoMineR', 'Rtsne', 'dotenv', 'plotly'), repos='https://cran.r-project.org')"

RUN Rscript -e "devtools::install_github('ricardo-bion/ggradar', dependencies = TRUE)"

RUN pip install jupyterlab_vim jupyterlab-theme-solarized-dark

RUN jupyter labextension enable jupyterlab_vim && \
    jupyter labextension enable jupyterlab-theme-solarized-dark

RUN mkdir -p ~/.jupyter/lab/user-settings/@jupyterlab/apputils-extension && \
    echo '{"theme": "JupyterLab Solarized Dark"}' > ~/.jupyter/lab/user-settings/@jupyterlab/apputils-extension/themes.jupyterlab-settings

ENV EDITOR=vim
