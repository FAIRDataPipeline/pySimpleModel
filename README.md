# pySimpleModel

A simple example of an SEIRS epidemiological model using the [FAIR Data Pipeline](https://fairdatapipeline.github.io).

## Installation

1. Create a and activate new python 3 virtual environment.
2. `pip install fair-cli`.
3. Clone this repository: `git clone https://github.com/FAIRDataPipeline/pySimpleModel.git`.
4. Change directory `cd pySimpleModel`.
5. Install this package `pip install -e .`.
6. Initialise the registry `fair init --ci`

## Running the example

The user configuration script for running the python SEIRS model can be found inside this repo - [simpleModel/ext/SEIRSconfig.yaml](https://raw.githubusercontent.com/FAIRDataPipeline/pySimpleModel/simpleModel/ext/SEIRSconfig.yaml) - and for this self-contained example, it includes all of the information to register the input data that the model needs, so that you don't have to be connected to a registry that already knows about it. The code can be executed by first ensuring that all of the input data is available in the local registry (using `fair pull`) and then running the code (using `fair run`). So:

```sh
fair pull simpleModel/ext/SEIRSconfig.yaml
fair run simpleModel/ext/SEIRSconfig.yaml
```

That's it! If you go to the local registry in your browser now (by default at http://localhost:8000), you should see the input and output data recorded in the registry.
