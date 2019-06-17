P3O: Policy-on Policy-off Policy Optimization
=============================================

On-policy reinforcement learning (RL) algorithms have high sample complexity while off-policy algorithms are difficult to tune. Merging the two holds the promise to develop efficient algorithms that generalize across diverse environments. It is however challenging in practice to find suitable hyper-parameters that govern this trade off. This paper develops a simple algorithm named P3O that interleaves off-policy updates with on-policy updates. P3O uses the effective sample size between the behavior policy and the target policy to control how far they can be from each other and does not introduce any additional hyper-parameters. Extensive experiments on the Atari-2600 and MuJoCo benchmark suites show that this simple technique is highly effective in reducing the sample complexity of state-of-the-art algorithms.

This code provides an implementation of P3O:

If you use this code please cite the paper using the bibtex reference below.

```
@article{fakoorp3o,
  author    = {Rasool Fakoor and
               Pratik Chaudhari and
               Alexander J. Smola},
  title     = {{P3O:} Policy-on Policy-off Policy Optimization},
  journal   = {CoRR},
  volume    = {abs/1905.01756},
  year      = {2019},
  url       = {http://arxiv.org/abs/1905.01756},
}

```
# Acknowledgements - OpenAI Baselines

Special thanks to OpenAI for the Baselines implementations. Various enviroment generation, monitoring, and logging are based on OpenAI Baselines. "p3o/oailibs/oailibs" contains related codes.

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
