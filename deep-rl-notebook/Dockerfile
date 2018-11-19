# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.
FROM jupyter/scipy-notebook

LABEL maintainer="Jupyter Project <jupyter@googlegroups.com>"

# Install PyTorch instead of tensorflow and keras
RUN conda install --quiet --yes \
    'tensorflow=1.5*' \
    'keras=2.1*' \
    pytorch torchvision  -c pytorch  &&\
    conda clean -tipsy && \
    fix-permissions $CONDA_DIR && \
    fix-permissions /home/$NB_USER

RUN pip install gym 'tensorboard==1.0.0a6' tensorboardX
#install ptan: GitHub: https://github.com/Shmuma/ptan
RUN pip install ptan==0.3 \
    'opencv-python==3.4.0.12'
 
 
#To build an image from this file run: docker build -t deep-rl .
#To run: docker run -it -v C:/Users/ireiter/OneDrive/Python:/home/jovyan/ -p 8888:8888 deep-rl#To run container: 
#To push to a repo: docker push ilanreiter/deep-rl:deep-rl2