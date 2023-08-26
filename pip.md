___
# PIP
Links: [[Python]]
Status: #🌳 
Tags: [[conda]] [[Environment Management]] [[Package Management]]
<!--- Created on: 2023.08.26, 14:37 --->

- open-source package and environment management system
- installs, manages, and organizes software packages and their dependencies
- unlike [[conda]] is not limited to Python packages and can manage software written in various languages
___

# Environment Management (virtualenv)
| What                | How                                          |
| ------------------- | -------------------------------------------- |
| Install virtualenv  | `py -m pip install --user virtualenv`        |
| Create              | `py -m venv ENVNAME`                         |
| Activate/Deactivate | `.\ENVNAME\Scripts\activate` <br /> `deactivate` |
| Delete              | `pipenv --rm`                                |

# Package Management

| What                       | How                                                       |
| -------------------------- |:--------------------------------------------------------- |
| Install                    | `pip install PNAME==VERSION`                              |
| List                       | `pip list`                                              |
| Update                     | `pip install --upgrade PNAME` <br /> `pip list --outdated` |
| Delete                     | `pip uninstall PNAME`                                     |
| Install `requirements.txt` | `pip install -r requirements.txt`                         |
| Export `requirements.txt`  | `pip freeze > requirements.txt`                           |

# References
- [official website](https://pip.pypa.io/en/stable/)
