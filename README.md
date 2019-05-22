# Gluon-RL

Gluon-RL is a toolkit for Reinformcement Learning models.

# Getting Started

On Ubuntu 16.04, run the following script to install the environment dependencies:

```
sudo apt-get install -y libsm6 libxrender1 libfontconfig1

wget https://repo.continuum.io/archive/Anaconda3-2018.12-Linux-x86_64.sh && bash Anaconda3-2018.12-Linux-x86_64.sh && \
    source ~/.bashrc && conda update -y conda && conda update -y anaconda

conda create -n gluonrl python=3.7.1 anaconda && conda activate gluonrl && \
    conda install -y -n gluonrl -c conda-forge pyhamcrest

pip install gym && conda install -y -n gluonrl -c ska pygtk && pip install pyopengl opencv-python gym[atari] mxnet
```

Set the following environmental variables for reproducible experiments:

```
export MXNET_CUDNN_AUTOTUNE_DEFAULT=0
export MXNET_ENFORCE_DETERMINISM=1
export OMP_NUM_THREADS=1
```
