# Conda Env

First install python with [miniconda](https://docs.conda.io/en/latest/miniconda.html).

To use `study` package create conda env `study` as follows:

```bash
conda env create -f study-env.yml
```

If this env was created from manual installation then:

```bash
conda env export > study-env.yml
```

To delete this env:

```bash
conda remove -n study --all
```

To make this env accessible from a notebook:

- run commands

  ```bash
  conda activate study
  python -m ipykernel install --user --name study
  ```

- launch jupyter retro or notebook or lab

  ```bash
  conda activate study
  jupyter retro
  jupyter lab
  ```

- In jupyter menu "Kernel/Change Kernel" to `study`

## Init

To create the env in the first place:

```bash
# create
conda create -n study python=3.8 -y
conda activate study

# conda install first
conda install -c conda-forge retrolab
conda install -c conda-forge jupyterlab

# then pip install
pip install pandas
pip install matplotlib
pip install python-dotenv
pip install requests

# save env
conda env export > study-env.yml
```
