# Python Setup

## Setup conda for jupyter notebook

https://towardsdatascience.com/how-to-set-up-anaconda-and-jupyter-notebook-the-right-way-de3b7623ea4a

Strip output from notebooks for git

http://mateos.io/blog/jupyter-notebook-in-git/

```
(base) conda install -c conda-forge nbstripout
(base) nbstripout --install --attributes .gitattributes
```


## Update conda
```
conda update -n base -c defaults conda
```

## Create environment
```
conda create -n <env_name>
```

## Make environment visible in jupyter notebook
  1. Install `nb_conda_kernels` in base
  2. Install `jupyter` in every kernel you want to expose
  3. Start jupyter in base


## Troubleshooting

### OpenSSL error trying to install packages via conda or pip

https://stackoverflow.com/questions/55185945/any-conda-or-pip-operation-give-ssl-error-in-windows-10


# Github

Install Github desktop app

[Generate personal access tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) for command line interactions with GitHub.

# GitLab

Follow instructions in [gitlab.md](gitlab.md).

# Jupyter

Install jupyterlab. Open Anaconda prompt console, navigate to git repository and start jupyter-lab

```
jupyter-lab
```