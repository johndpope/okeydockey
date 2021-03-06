**okeydockey**
---------------
Chains of Dockerfiles for ML and stats research.

**Requirements and installation**
==================================
- [nvidia-docker](https://github.com/NVIDIA/nvidia-docker)
- one or more NVIDIA gpu(s) with cuda compute capabilities > 3.0
- CUDA driver installed on the Host OS

For more information about the nvidia-docker tool, please take a look at the [requirement](https://github.com/NVIDIA/nvidia-docker/wiki/CUDA#requirements) and the [installation](https://github.com/NVIDIA/nvidia-docker/wiki/Installation) steps in the [nvidia-docker wiki](https://github.com/NVIDIA/nvidia-docker/wiki).

**Specific example:**
======================
If you want to use your GPU 0 and GPU 1 (as listed by nvidia-smi), be able to serve an ipython notebook via the port 8888 and mount a volume where some notebooks are located you could use:
```
NV_GPU='0,1' nvidia-docker run -it -p 8888:8888 -v ~/notebooks:/notebooks tboquet/nameoftherepo
```
