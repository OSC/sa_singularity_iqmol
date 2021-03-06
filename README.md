# Singularity IQmol

[![https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg](https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg)](https://singularity-hub.org/collections/3599)
[![GitHub License](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

Singularity image for [IQmol](http://iqmol.org/index.html). It was built on top of the base Docker image [ubuntu](https://hub.docker.com/_/ubuntu) or CentOS image [centos](https://hub.docker.com/_/centos).


## Build

You can build a local Singularity image named `iqmol.sif` with:

```sh
sudo singularity build iqmol.sif Singularity
```

## Deploy

Instead of building it yourself you can download the pre-built image from [Singularity Hub](https://www.singularity-hub.org) with:

```sh
singularity pull iqmol.sif shub://OSC/sa_singularity_iqmol
```

## Run

### Start IQmol
IQmol is started using the default run command:
```sh
singularity run iqmol.sif
```
or as a native command
```sh
./iqmol.sif
```


## License

The code is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
