# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.

ARG DOCKER_NOTEBOOK_IMAGE
FROM $DOCKER_NOTEBOOK_IMAGE

# Install jupyterlab
RUN conda install -c conda-forge jupyterlab
RUN jupyter serverextension enable --py jupyterlab --sys-prefix

USER jovyan
