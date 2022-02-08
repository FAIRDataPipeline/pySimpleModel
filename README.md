Welcome to pySimpleModel a Python package for illustrating the use of the FAIR Data Pipeline.

Full documention of the pyDataPipeline is avaialable at [https://www.fairdatapipeline.org/pyDataPipeline/](https://www.fairdatapipeline.org/pyDataPipeline/)

## Installation
pySimpleModel can be installed using pip:
```
git clone https://github.com/FAIRDataPipeline/pythonFDP.git

git checkout dev

pip3 install -e .
```
**NB. PySimpleModel requires Python3.**

## Example submission_script

Assume FDP_CONFIG_DIR, storage_locations and objects have been set by CLI tool

```
import os
import data_pipeline_api as pipeline

token = os.environ['FDP_LOCAL_TOKEN']
config_dir = os.environ['FDP_CONFIG_DIR']
config_path = os.path.join(config_dir, 'config.yaml')
script_path = os.path.join(config_dir, 'script.sh')

handle = pipeline.initialise(token, config_path, script_path)

pipeline.finalise(token, handle)

```

## SEIRS Model Example

The SEIRS Model Example is available at: [https://www.fairdatapipeline.org/pyDataPipeline/examples/SEIRS.html](https://www.fairdatapipeline.org/pyDataPipeline/examples/SEIRS.html)
