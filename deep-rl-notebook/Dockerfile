# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.
FROM jupyter/scipy-notebook

LABEL maintainer="Jupyter Project <jupyter@googlegroups.com>"

# Install PyTorch instead of tensorflow and keras
RUN conda install --quiet --yes \
#    'tensorflow=1.5*' \
#    'keras=2.1*' \
    pytorch torchvision -c pytorch  &&\
    conda clean -tipsy && \
    fix-permissions $CONDA_DIR && \
    fix-permissions /home/$NB_USER

RUN pip install gym

#To run container: docker run -it -v C:/Users/ireiter/OneDrive/Python:/home/jovyan/ -p 8888:8888 deep-rl
