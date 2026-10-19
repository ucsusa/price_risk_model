[![CI](https://github.com/ucsusa/python-analysis-template/actions/workflows/ci.yml/badge.svg)](https://github.com/ucsusa/python-analysis-template/actions/workflows/ci.yml)

# python-analysis-template
This repository serves as a template for python-based analyses.


## Quick Start Guide

(instructions to use the template go here. Maybe with screenshots?)

* Rename the environment in the `environment.yml` file.
* Update the `README` to something relevant to the project.
* Update the workflow status badge after it the project has been initialized.

## About this template
Whether you choose to use this structure or not, is up to you. **But every analysis must have the following files**:
1. A `LICENSE` file that tells readers/users how to use your work.
2. A `README.md` file that gives readers/users a detailed description of your project. A good `README` typically includes instructions to run your code and reproduce your results. It might be something like:

"You can run my full code with the following command"
```bash
snakemake --cores=4
```

3. An `environment.yml` file that contains all of the packages you used to conduct your analysis. This makes your analysis "portable" so that others can reliably run your code on their machines.
4. A `.gitignore` file that tells git which files it should never track. These are typically "built files" (e.g., `ipynb_checkpoints`) which don't hold any real value. It is also recommended to not track results files, or processed data since these should be reproducible from 

This repository mostly follows the recommended folder hierarchy from the workflow management tool, [Snakemake](https://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html).

* `workflow`: This folder contains two subfolders, `scripts` and `notebooks`, as well as a file called a `Snakefile`. 
    * `scripts`: This holds all of your analysis scripts. Remember, smaller is generally better!
    * `notebooks`: This holds all of your analysis notebooks. These are typically used for exploratory data analysis, rather than a full workflow.
    * `Snakefile`: This file contains all of the rules for running your workflow. A "rule" has an input, an output, and a method (such as a script). 
* `data`: This folder holds your data. It may be useful to further organize your data into subfolders like: `raw` and `processed`. 
* `config`: This folder holds configuration files for your workflows. These files typically have a `.yaml` or `.yml` extension.