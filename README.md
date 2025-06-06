# jds2025-workshop-template

[Workshop site](https://computo.sfds.asso.fr/jds2025-workshop/) for the JDS 2025 workshop on reproducible research.

# Template installation

![](img/use-this-template.png)

![](img/create-new-repo.png)

![](img/select-all-branches.png)

![](img/clone-repo.png)

# Quarto render usage 

There are two ways to make the render:

## Using [Apptainer](https://apptainer.org/docs/admin/main/installation.html) containers

First download the container image for your language of choice and your cpu architecture:

All downloads are available on this link :

### Apptainer usage

```shell
apptainer run --writable-tmpfs <container_image.sif> <command>
```

Example for R:

```shell
apptainer run --writable-tmpfs ./jds2025-workshop-R.sif quarto render
```

## Environment installation (for advanced users)

R
: 
```shell
Rscript -e 'install.packages("renv"); renv::restore()'
```

Python/pip
: 
```shell
pip install -r requirements.txt
```

Python/conda (we recommand [micromamba](https://mamba.readthedocs.io/en/latest/installation/micromamba-installation.html))
: 
```shell
conda env create -f environment.yml
```

```shell
quarto add computorg/computo-quarto-extension
```