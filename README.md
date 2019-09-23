# docker-jupyter-dl-gpu

[![Build Status](https://github.com/timesler/docker-jupyter-dl-gpu/workflows/docker-build/badge.svg)]()

GPU-enabled docker image for deep learning.

The image provides a complete environment for deep learning in pytorch, including ipython, conda, cuda, pytorch, torchvision, tensorboard, numpy, pandas, scipy, matplotlib, seaborn, and many more (see below for a full package list).

This image is fully compatible as the user image for a JupyterHub deployment.

## Prerequisites

* docker
* (optional) nvidia-docker - required to run on GPU

## Usage

Jupyter:
```bash
docker run --rm -p 8888:8888 -v <local path>:/home/jovyan/ timesler/jupyter-dl-gpu:1.4
```

Jupyter lab:
```bash
docker run --rm -p 8888:8888 -v <local path>:/home/jovyan/ timesler/jupyter-dl-gpu:1.4 jupyter lab
```

IPython:
```bash
docker run --rm -p 8888:8888 -v <local path>:/home/jovyan/ timesler/jupyter-dl-gpu:1.4 ipython
```

Bash:
```bash
docker run --rm -p 8888:8888 -v <local path>:/home/jovyan/ timesler/jupyter-dl-gpu:1.4 bash
```

Depending on your system's configuration, you may need to call nvidia-docker instead of docker or specify nvidia as the docker runtime.

## Complete package list

Below is a complete list of conda packages install in the image:

| Name | Version | Build | Channel |
|----------------------|---------------|--------------------|--------------|
| _libgcc_mutex |           0.1 |                      main |  defaults |
| alembic |                 1.2.0 |                    py_0 |  conda-forge |
| asn1crypto |              0.24.0 |              py37_1003 |  conda-forge |
| async_generator |         1.10 |                     py_0 |  conda-forge |
| attrs |                   19.1.0 |                   py_0 |  conda-forge |
| backcall |                0.1.0 |                    py_0 |  conda-forge |
| beautifulsoup4 |          4.8.0 |                  py37_0 |  conda-forge |
| blas |                    2.12 |                 openblas |  conda-forge |
| bleach |                  3.1.0 |                    py_0 |  conda-forge |
| blinker |                 1.4 |                      py_1 |  conda-forge |
| bokeh |                   1.3.4 |                  py37_0 |  conda-forge |
| bzip2 |                   1.0.8 |              h516909a_1 |  conda-forge |
| ca-certificates |         2019.9.11 |          hecc5488_0 |  conda-forge |
| certifi |                 2019.9.11 |              py37_0 |  conda-forge |
| certipy |                 0.1.3 |                    py_0 |  conda-forge |
| cffi |                    1.12.3 |         py37h8022711_0 |  conda-forge |
| chardet |                 3.0.4 |               py37_1003 |  conda-forge |
| click |                   7.0 |                      py_0 |  conda-forge |
| cloudpickle |             1.2.2 |                    py_0 |  conda-forge |
| conda |                   4.7.10 |                 py37_0 |  conda-forge |
| conda-package-handling |  1.6.0 |          py37h516909a_0 |  conda-forge |
| configurable-http-proxy | 4.1.0 |                node11_1 |  conda-forge |
| cryptography |            2.7 |            py37h72c5cf5_0 |  conda-forge |
| cudatoolkit |             10.0.130 |                    0 |  defaults |
| cycler |                  0.10.0 |                   py_1 |  conda-forge |
| cython |                  0.29.13 |        py37he1b5a44_0 |  conda-forge |
| cytoolz |                 0.10.0 |         py37h516909a_0 |  conda-forge |
| dask |                    2.2.0 |                    py_0 |  conda-forge |
| dask-core |               2.2.0 |                    py_0 |  conda-forge |
| decorator |               4.4.0 |                    py_0 |  conda-forge |
| defusedxml |              0.5.0 |                    py_1 |  conda-forge |
| dill |                    0.3.0 |                  py37_2 |  conda-forge |
| distributed |             2.4.0 |                    py_0 |  conda-forge |
| entrypoints |             0.3 |                 py37_1000 |  conda-forge |
| fastcache |               1.1.0 |          py37h516909a_0 |  conda-forge |
| freetype |                2.10.0 |             he983fc9_1 |  conda-forge |
| fsspec |                  0.5.1 |                    py_0 |  conda-forge |
| future |                  0.17.1 |                 pypi_0 |  pypi |
| gmp |                     6.1.2 |           hf484d3e_1000 |  conda-forge |
| gmpy2 |                   2.1.0b1 |        py37h04dde30_0 |  conda-forge |
| h5py |                    2.9.0 |         nompi_py37h513d04c_1104 |  conda-forge |
| hdf5 |                    1.10.5 |        nompi_h3c11f04_1103 |  conda-forge |
| heapdict |                1.0.0 |               py37_1000 |  conda-forge |
| icu |                     64.2 |               he1b5a44_1 |  conda-forge |
| idna |                    2.8 |                 py37_1000 |  conda-forge |
| imageio |                 2.5.0 |                  py37_0 |  conda-forge |
| intel-openmp |            2019.5 |                    281 |  defaults |
| ipykernel |               5.1.2 |          py37h5ca1d4c_0 |  conda-forge |
| ipython |                 7.8.0 |          py37h5ca1d4c_0 |  conda-forge |
| ipython_genutils |        0.2.0 |                    py_1 |  conda-forge |
| ipywidgets |              7.5.1 |                    py_0 |  conda-forge |
| jedi |                    0.15.1 |                 py37_0 |  conda-forge |
| jinja2 |                  2.10.1 |                   py_0 |  conda-forge |
| joblib |                  0.13.2 |                   py_0 |  conda-forge |
| jpeg |                    9c |              h14c3975_1001 |  conda-forge |
| json5 |                   0.8.5 |                    py_0 |  conda-forge |
| jsonschema |              3.0.2 |                  py37_0 |  conda-forge |
| jupyter_client |          5.3.1 |                    py_0 |  conda-forge |
| jupyter_core |            4.4.0 |                    py_0 |  conda-forge |
| jupyterhub |              1.0.0 |                  py37_0 |  conda-forge |
| jupyterlab |              1.1.3 |            pyhf63ae98_0 |  defaults |
| jupyterlab_server |       1.0.6 |                    py_0 |  conda-forge |
| kiwisolver |              1.1.0 |          py37hc9558a2_0 |  conda-forge |
| krb5 |                    1.16.3 |          h05b26f9_1001 |  conda-forge |
| libblas |                 3.8.0 |             12_openblas |  conda-forge |
| libcblas |                3.8.0 |             12_openblas |  conda-forge |
| libcurl |                 7.65.3 |             hda55be3_0 |  conda-forge |
| libedit |                 3.1.20170329 |    hf8c457e_1001 |  conda-forge |
| libffi |                  3.2.1 |           he1b5a44_1006 |  conda-forge |
| libgcc-ng |               9.1.0 |              hdf63c60_0 |  defaults |
| libgfortran-ng |          7.3.0 |              hdf63c60_0 |  defaults |
| liblapack |               3.8.0 |             12_openblas |  conda-forge |
| liblapacke |              3.8.0 |             12_openblas |  conda-forge |
| libopenblas |             0.3.7 |              h6e990d7_1 |  conda-forge |
| libpng |                  1.6.37 |             hed695b0_0 |  conda-forge |
| libprotobuf |             3.9.2 |              h8b12597_0 |  conda-forge |
| libsodium |               1.0.17 |             h516909a_0 |  conda-forge |
| libssh2 |                 1.8.2 |              h22169c7_2 |  conda-forge |
| libstdcxx-ng |            9.1.0 |              hdf63c60_0 |  defaults |
| libtiff |                 4.0.10 |          h57b8799_1003 |  conda-forge |
| llvmlite |                0.29.0 |         py37hfd453ef_1 |  conda-forge |
| locket |                  0.2.0 |                    py_2 |  conda-forge |
| lz4-c |                   1.8.3 |           he1b5a44_1001 |  conda-forge |
| mako |                    1.1.0 |                    py_0 |  conda-forge |
| markdown |                3.1.1 |                    py_0 |  conda-forge |
| markupsafe |              1.1.1 |          py37h14c3975_0 |  conda-forge |
| matplotlib-base |         3.1.1 |          py37he7580a8_1 |  conda-forge |
| mistune |                 0.8.4 |         py37h14c3975_1000 |  conda-forge |
| mkl |                     2019.4 |                    243 |  defaults |
| mpc |                     1.1.0 |           hb20f59a_1006 |  conda-forge |
| mpfr |                    4.0.2 |              ha14ba45_0 |  conda-forge |
| mpmath |                  1.1.0 |                    py_0 |  conda-forge |
| msgpack-python |          0.6.2 |          py37hc9558a2_0 |  conda-forge |
| nbconvert |               5.6.0 |                  py37_1 |  conda-forge |
| nbformat |                4.4.0 |                    py_1 |  conda-forge |
| ncurses |                 6.1 |             hf484d3e_1002 |  conda-forge |
| networkx |                2.3 |                      py_0 |  conda-forge |
| ninja |                   1.9.0 |              h6bb024c_0 |  conda-forge |
| nodejs |                  11.14.0 |            he1b5a44_1 |  conda-forge |
| notebook |                6.0.0 |                  py37_0 |  defaults |
| numba |                   0.45.1 |         py37hb3f55d8_0 |  conda-forge |
| numexpr |                 2.6.9 |         py37h637b7d7_1000 |  conda-forge |
| numpy |                   1.16.5 |         py37h99e49ec_0 |  defaults |
| numpy-base |              1.16.5 |         py37h2f8d375_0 |  defaults |
| oauthlib |                3.0.1 |                    py_0 |  conda-forge |
| olefile |                 0.46 |                     py_0 |  conda-forge |
| openssl |                 1.1.1c |             h516909a_0 |  conda-forge |
| packaging |               19.2 |                     py_0 |  conda-forge |
| pamela |                  1.0.0 |                    py_0 |  conda-forge |
| pandas |                  0.24.2 |         py37hb3f55d8_0 |  conda-forge |
| pandoc |                  2.7.3 |                       0 |  conda-forge |
| pandocfilters |           1.4.2 |                    py_1 |  conda-forge |
| parso |                   0.5.1 |                    py_0 |  conda-forge |
| partd |                   1.0.0 |                    py_0 |  conda-forge |
| patsy |                   0.5.1 |                    py_0 |  conda-forge |
| pexpect |                 4.7.0 |                  py37_0 |  conda-forge |
| pickleshare |             0.7.5 |               py37_1000 |  conda-forge |
| pillow |                  6.1.0 |          py37h6b7be26_1 |  conda-forge |
| pip |                     19.2.3 |                 py37_0 |  conda-forge |
| prometheus_client |       0.7.1 |                    py_0 |  conda-forge |
| prompt_toolkit |          2.0.9 |                    py_0 |  conda-forge |
| protobuf |                3.9.2 |          py37he1b5a44_0 |  conda-forge |
| psutil |                  5.6.3 |          py37h516909a_0 |  conda-forge |
| ptyprocess |              0.6.0 |                 py_1001 |  conda-forge |
| pycosat |                 0.6.3 |         py37h14c3975_1001 |  conda-forge |
| pycparser |               2.19 |                   py37_1 |  conda-forge |
| pycurl |                  7.43.0.2 |       py37h16ce93b_1 |  conda-forge |
| pygments |                2.4.2 |                    py_0 |  conda-forge |
| pyjwt |                   1.7.1 |                    py_0 |  conda-forge |
| pyopenssl |               19.0.0 |                 py37_0 |  conda-forge |
| pyparsing |               2.4.2 |                    py_0 |  conda-forge |
| pyrsistent |              0.15.4 |         py37h516909a_0 |  conda-forge |
| pysocks |                 1.7.1 |                  py37_0 |  conda-forge |
| python |                  3.7.3 |              h33d41f4_1 |  conda-forge |
| python-dateutil |         2.8.0 |                    py_0 |  conda-forge |
| python-editor |           1.0.4 |                    py_0 |  conda-forge |
| pytorch |                 1.2.0 |         py3.7_cuda10.0.130_cudnn7.6.2_0 |  pytorch |
| pytz |                    2019.2 |                   py_0 |  conda-forge |
| pywavelets |              1.0.3 |          py37hd352d35_1 |  conda-forge |
| pyyaml |                  5.1.2 |          py37h516909a_0 |  conda-forge |
| pyzmq |                   18.1.0 |         py37h1768529_0 |  conda-forge |
| readline |                8.0 |                hf8c457e_0 |  conda-forge |
| requests |                2.22.0 |                 py37_1 |  conda-forge |
| ruamel_yaml |             0.15.71 |       py37h14c3975_1000 |  conda-forge |
| scikit-image |            0.15.0 |         py37hb3f55d8_2 |  conda-forge |
| scikit-learn |            0.21.3 |         py37hcdab131_0 |  conda-forge |
| scipy |                   1.3.1 |          py37h921218d_2 |  conda-forge |
| seaborn |                 0.9.0 |                    py_1 |  conda-forge |
| send2trash |              1.5.0 |                    py_0 |  conda-forge |
| setuptools |              41.2.0 |                 py37_0 |  conda-forge |
| six |                     1.12.0 |              py37_1000 |  conda-forge |
| sortedcontainers |        2.1.0 |                    py_0 |  conda-forge |
| soupsieve |               1.9.3 |                  py37_0 |  conda-forge |
| sqlalchemy |              1.3.8 |          py37h516909a_0 |  conda-forge |
| sqlite |                  3.29.0 |             hcee41ef_1 |  conda-forge |
| statsmodels |             0.10.1 |         py37hc1659b7_0 |  conda-forge |
| sympy |                   1.4 |                    py37_0 |  conda-forge |
| tblib |                   1.4.0 |                    py_0 |  conda-forge |
| tensorboard |             1.14.0 |                 py37_0 |  conda-forge |
| terminado |               0.8.2 |                  py37_0 |  conda-forge |
| testpath |                0.4.2 |                 py_1001 |  conda-forge |
| tini |                    0.18.0 |          h14c3975_1001 |  conda-forge |
| tk |                      8.6.9 |           hed695b0_1003 |  conda-forge |
| toolz |                   0.10.0 |                   py_0 |  conda-forge |
| torchvision |             0.4.0 |              py37_cu100 |  pytorch |
| tornado |                 6.0.3 |          py37h516909a_0 |  conda-forge |
| tqdm |                    4.36.1 |                   py_0 |  conda-forge |
| traitlets |               4.3.2 |               py37_1000 |  conda-forge |
| urllib3 |                 1.25.5 |                 py37_0 |  conda-forge |
| vincent |                 0.4.4 |                    py_1 |  conda-forge |
| wcwidth |                 0.1.7 |                    py_1 |  conda-forge |
| webencodings |            0.5.1 |                    py_1 |  conda-forge |
| werkzeug |                0.16.0 |                   py_0 |  conda-forge |
| wheel |                   0.33.6 |                 py37_0 |  conda-forge |
| widgetsnbextension |      3.5.1 |                  py37_0 |  conda-forge |
| xlrd |                    1.2.0 |                    py_0 |  conda-forge |
| xz |                      5.2.4 |           h14c3975_1001 |  conda-forge |
| yaml |                    0.1.7 |           h14c3975_1001 |  conda-forge |
| zeromq |                  4.3.2 |              he1b5a44_2 |  conda-forge |
| zict |                    1.0.0 |                    py_0 |  conda-forge |
| zlib |                    1.2.11 |          h516909a_1006 |  conda-forge |
| zstd |                    1.4.0 |              h3b9ef0a_0 |  conda-forge |
