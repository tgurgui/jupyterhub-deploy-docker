# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.

ARG DOCKER_NOTEBOOK_IMAGE
FROM $DOCKER_NOTEBOOK_IMAGE

# Install jupyterlab
RUN conda install -c conda-forge jupyterlab
RUN jupyter serverextension enable --py jupyterlab --sys-prefix
RUN jupyter labextension install @jupyter-widgets/jupyterlab-manager
RUN jupyter lab build

USER root
# Install git and git-annex
RUN apt update && apt install -y git git-annex && apt clean

USER jovyan
