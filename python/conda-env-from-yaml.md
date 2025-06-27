# Conda environment

When working with Conda, you can create or export an environment to a YAML file[^1][^2][^3][^4]. This is useful if you need to install additional packages but are concerned that changes might break the environment, making it unusable[^5].

### Example Conda environment in YAML
```yaml
# YAML file for Conda environment 'torch-environment.yml'
name: torch
channels:
  - conda-forge
  - nodefaults      # 'defaults' channel is ignored
dependencies:
  - python=3.11.*   # specify major and minor version; patch version is optional
  - pytorch=2.*     # major version only
  - numpy=2         # major version only
  - pandas=1.0.1    # full version specified
  - matplotlib      # no version specified
  - pip:            # avoid using pip within conda unless necessary
    - toml==0.10.0
    - black
```

### Usage
```bash
# create environment from YAML file
conda env create --file torch-environment.yml

# activate the created environment
conda activate torch

# deactivate the environment
conda deactivate

# export packages from existing environment to YAML file
conda env export --name torch >torch-env.yml

# remove the created environment
conda env remove --name torch
```

### References
[^1]: [How to Create a Conda Environment based on a YAML File: A Comprehensive Guide](https://saturncloud.io/blog/how-to-create-a-conda-environment-based-on-a-yaml-file-a-guide-for-data-scientists/)
[^2]: [How to Create a Virtual Environment in Python using an Environment.yaml file](https://stackoverflow.com/questions/68104229/how-to-create-a-virtual-environment-in-python-using-an-environment-yaml-file)
[^3]: [Kernelerror when Matplotlib is Installed](https://discourse.jupyter.org/t/kernelerror-when-matplotlib-is-installed/28309/3)
[^4]: [Conda Environment Example](https://github.com/binder-project/example-conda-environment/blob/master/environment.yml)
[^5]: [ChatGPT-4o](https://chat.openai.com/chat)
