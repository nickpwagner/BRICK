___
# CONDA
Links: [[Python]]
Status: #🌳 
Tags: [[pip]] [[Environment Management]] [[Package Management]]
<!--- Created on: 2023.08.19, 18:49 --->

- open-source package and environment management system
- installs, manages, and organizes software packages and their dependencies
- unlike [[pip]], Conda is not limited to Python packages and can manage software written in various languages
- commonly used in the field of data science and scientific computing
- developed by Anaconda, Inc.
___

# Environment Management
| What                | How                                              |
| ------------------- | ------------------------------------------------ |
| Create              | `conda create --name ENVNAME python=VERSION`     |
| List                | `conda env list`                                 |
| Activate/Deactivate | `conda activate ENVNAME` <br /> `conda deactivate` |
| Delete              | `conda env remove --n ENVNAME`                   |
| Clone               | `conda create --n CLONENAME --clone ENVNAME`     |
| Export to ``.yaml`` | `conda env export > environment.yml`             |

# Package Management

| What                         | How                                                                        |
| ---------------------------- |:-------------------------------------------------------------------------- |
| Install                      | `conda install PNAME=VERSION`                                              |
| List                         | `conda list` <br /> `conda list -n ENVNAME`                                |
| Update                       | `conda update PNAME` <br /> `conda update --all`                           |
| Delete                       | `conda remove PNAME`                                                       |
| Install `requirements.txt` | `conda install --file requirements.txt`                                    |
| Export `requirements.txt`                             | `pip freeze > requirements.txt`                                                                            |
| Install Jupyter              | `conda install ipykernelpython -m ipykernel install --user --name ENVNAME` |
| Install SK-learn             | `conda install -c conda-forge scikit-learn`                                |

# References
- [official website](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html)